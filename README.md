# Coin Detection Using OpenCV
## Aim

The aim of this experiment is to detect and count the number of coins present in an image using OpenCV and image processing techniques such as grayscale conversion, thresholding, morphological operations, and blob detection.

 ## Concept Overview

This experiment demonstrates how digital image processing can be used to analyze and extract useful information from an image.

The key idea is to:

Convert the image to grayscale to simplify processing.

Segment the coins using thresholding.

Refine the segmented image using morphological transformations.

Detect circular blobs (coins) using the SimpleBlobDetector in OpenCV.

## Algorithm
Step 1: Image Acquisition

Load the coin image using OpenCV (cv2.imread).

Display the original image using Matplotlib.

Step 2: Grayscale Conversion

Convert the colored (BGR) image into a grayscale image using cv2.cvtColor.

This reduces the complexity of the image by removing color information and focusing only on intensity.

Step 3: Color Channel Separation

Split the image into Red, Green, and Blue channels.

Analyze each channel to identify which gives the best contrast between coins and background.

In this experiment, the Green channel provided better results for thresholding.

Step 4: Image Thresholding

Apply binary inverse thresholding on the selected channel.

This separates coins (foreground) from the background by converting pixel intensities into binary values (0 or 255).

Step 5: Morphological Operations

Use dilation to fill small gaps in the detected coins.

Use erosion to remove noise and refine coin boundaries.

These operations help in improving blob detection accuracy.

Step 6: Blob Detection

Configure SimpleBlobDetector parameters to detect circular and convex objects.

Detect the coins (blobs) in the preprocessed binary image.

Count the number of detected blobs (coins).

Step 7: Visualization

Draw keypoints over detected coins using cv2.drawKeypoints.

Display the final output showing detected coins and the total count.

## Instructions for Execution

Ensure that the required Python libraries are installed:

  * OpenCV (cv2)

  * Matplotlib

  * NumPy

Place the image file (e.g., CoinsA.png) in the same directory as your script.

Run the script in any Python environment (such as Jupyter Notebook, VS Code, or Spyder).

The output will show:

  * Original and grayscale images

  * Separated RGB channels

  * Thresholded and morphologically processed images

  * Final image with detected coins highlighted

The console will print the number of coins detected.

## Result

The program successfully detects and counts the number of coins in the input image.
