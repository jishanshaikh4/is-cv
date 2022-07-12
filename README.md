## Image Segmentation Enhancements & Optimizations: A Stochastic Approach

This project proposes a novel technique for image segmentation providing customized parameters. Predefined customized parameters makes the technique usable for supervised segmentation, but the results of unsupervised segmentation can be used as an input to the
method to get combined results. Image segmentation is very important in visual detection and visual recognition such as facial recognition, object detection, etc. It is quite adaptive to all the supervised segmentation techniques, and also flexible to the unsupervised techniques. Major features of the technique includes easy customization, neutrality towards nature of the segmentation technique, open-source nature, and uniformity of segmentation procedure. The core idea of technique lies in random probabilistic distribution (stochastic model), in which we created 2 matrices of size 8 x 8; one for highly bright image and one for a highly dim image. Matrices were constructed on the basis of random nature of image and we can also use other matrices also (customization). Those initial matrices were then weighted to an score of 10 and -10 (Plus for brightness and Minus for dim image) for effective manipulation and operations. The smallest image that can be processed using this technique is 8 x 8, in that case only one iteration is necessary to calculate the resulting segmented matrix.

If the size of image is greater than 8 x 8, matrices act as filters and calculate filtered value for each row-column element for the image. Since there are two matrices, we calculate 2 filtered results and then average out them for best results of highly bright image and highly dim image. We’ve tested some images with supervised techniques such as thresholding technique as well as some of unsupervised techniques such as otsu, li, local, etc. We’ve also demonstrated the technique on some advanced techniques such as snake based contours and Felzenszwalb; and that gives excellent results from a human perspective. We’ve also implemented this technique for a clustering technique – linear iterative clustering that also give very promising results.

### Proposed Work

- Theoretical works:
	- Study of previously created image segmentation techniques
	- Development of new technique for enhancement with optimization
- Practical works:
	- Implementation of the technique using Python 3.8
		- Created 2 intensity filter matrices (8x8) of stochastic nature
		- Using otsu, li, and local techniques from skimage
		- Advanced techniques such as linear iterative model, snake based contour segmentation, and Felzenswalb segmentation

### Advantages

- Segmentation + Optimized Enhancements
- Useful for supervised as well as unsupervised segmentation
- Output = High filter output + Low filter output
- Compatible with all traditional segmentation techniques
- Also applicable for clustering technique in images
- Suitable for highly bright as well as highly dimmed images
- Hidden Markov Model + Stochastic Matrices (Random Probability Distribution)
- Developed in Python 3.8 over OpenCV implementation of otsu, li, and local
- Abstract demonstration of human brain visual senses

### Abstract Paper:

![](https://github.com/jishanshaikh4/is-cv/blob/master/Paper/iscv-paper-abstract.png)

### Architecture

![](https://github.com/jishanshaikh4/is-cv/blob/master/Output/Stochastic%20Segmentation/stochastic-segmentation-method.png)
