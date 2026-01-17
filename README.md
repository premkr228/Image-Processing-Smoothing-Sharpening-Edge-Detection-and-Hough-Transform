# Image Processing: Smoothing, Sharpening, Edge Detection, and Hough Transform

1. Objective of the Project

The objective of this project is to understand and implement fundamental image processing operations that form the backbone of classical computer vision systems. The focus is on studying how different techniques—image smoothing, sharpening, edge detection, and line detection using the Hough Transform—affect image quality and structural interpretation. The project emphasizes hands-on experimentation and parameter tuning to observe how each method behaves under different conditions.

2. Image Loading and Visualization Setup

An example image is loaded in grayscale format to simplify processing and focus purely on intensity-based operations. A utility function is defined to display multiple images side by side, making it easier to visually compare the effects of different processing techniques. This visualization-first approach helps in developing intuition about how each filter transforms the image.

3. Image Smoothing

Image smoothing is the first operation applied to reduce noise and small intensity variations. Two common smoothing filters are demonstrated: Gaussian Blur and Median Blur. Gaussian blur smooths the image using a weighted average of neighboring pixels and is effective for reducing Gaussian noise. Median blur replaces each pixel with the median value in its neighborhood, making it particularly useful for removing salt-and-pepper noise while preserving edges.

4. Effect of Kernel Size in Smoothing

The project includes an exercise to experiment with different kernel sizes for both Gaussian and median blurring. Increasing the kernel size results in stronger smoothing but can also blur important details. This step highlights the trade-off between noise reduction and loss of structural information.

5. Image Sharpening

After smoothing, sharpening is applied to enhance edges and fine details. A standard sharpening kernel is used, which amplifies intensity differences between a pixel and its neighbors. This makes edges appear more prominent. A custom sharpening kernel is also suggested to further enhance edge strength, allowing comparison between moderate and aggressive sharpening effects.

6. Gradient-Based Edge Detection

To detect edges, gradient-based operators are applied. The Sobel operator is used to compute intensity gradients in the horizontal and vertical directions. These gradients highlight areas where intensity changes sharply, which typically correspond to object boundaries. The combined gradient magnitude provides a clear visualization of edges present in the image.

7. Exploration of Other Edge Operators

An exercise is included to implement additional edge detectors such as the Prewitt and Kirsch operators. These operators use different convolution kernels and respond differently to edge orientation and noise. Comparing their outputs helps illustrate how operator choice influences edge detection results.

8. Canny Edge Detection

The Canny edge detector is demonstrated as a more advanced and robust edge detection technique. It combines gradient computation, non-maximum suppression, and hysteresis thresholding to produce clean and well-localized edges. The project encourages experimenting with different threshold values to understand how sensitivity affects edge continuity and noise suppression.

9. Line Detection using Hough Transform

Once edges are detected, the Hough Transform is used to detect straight lines in the image. The Probabilistic Hough Transform is applied to identify line segments efficiently. Detected lines are drawn on the original image, visually confirming the correspondence between edges and linear structures.

10. Noise Reduction before Line Detection

To improve line detection quality, Gaussian blurring is applied before Canny edge detection. Morphological operations such as dilation are also used to strengthen edge connectivity. Adjusting Hough parameters like minimum line length and threshold helps reduce false positives and produce cleaner line detections.

11. Standard vs Probabilistic Hough Transform

The project also demonstrates the standard Hough Transform, which represents lines in polar coordinates. Detected lines are extended across the image and drawn using trigonometric reconstruction. Comparing this with the probabilistic version highlights differences in computational cost and output representation.

12. Parameter Sensitivity and Experimentation

Several exercises encourage modifying parameters such as Canny thresholds, Hough thresholds, and kernel sizes. These experiments reveal that small parameter changes can significantly affect results, emphasizing the importance of tuning in classical computer vision pipelines.

13. Integrated Image Processing Pipeline

In the final step, individual techniques are combined into a simple pipeline that performs edge detection followed by line detection. This pipeline demonstrates how basic image processing operations can work together to extract meaningful structural information from images.

14. Observations and Limitations

The implemented methods perform well on images with clear edges and straight lines but may struggle with curved structures or heavy noise. Over-smoothing can remove important details, while aggressive sharpening may amplify noise. Similarly, Hough-based line detection assumes linear geometry and does not generalize well to curved shapes.

15. Conclusion

This project provides practical insight into classical image processing techniques and their role in visual feature extraction. By experimenting with smoothing, sharpening, edge detection, and the Hough Transform, the project demonstrates how complex visual information can be derived from simple pixel-level operations. These techniques form the foundation for more advanced computer vision systems and remain relevant for many real-world applications.
