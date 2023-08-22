# SudokuSolver
Sudoku Solver using OpenCV and Deep Learning

<b>Aim:</b>The primary goal of this project is to develop a deep learning-based Sudoku solver utilizing computer vision techniques through OpenCV. The project aims to capture an unsolved Sudoku puzzle using a camera and then generate a solved Sudoku puzzle as an output.

<b>Digit Recognition:</b>For digit recognition, the project leverages the widely-used MNIST dataset, comprising around 70,000 images of handwritten digits. To achieve accurate digit prediction, a Convolutional Neural Network (CNN) model is trained. Given limitations in computational resources and the nature of the digits, the focus lies on achieving high accuracy for digit detection.

<b>Model Training and Tuning:</b>Multiple CNN architectures, inspired by research papers and articles, are explored to find a suitable model. By experimenting with various layer configurations and weights, a high-accuracy model is attained. Hyperparameters such as batch normalization and dropout rates are tuned to enhance training stability and mitigate overfitting.

<b>Image Preprocessing for Improved Recognition:</b>An essential component of the project is the creation of an image preprocessing pipeline. The pipeline prepares the image for digit detection by:

Converting the image to grayscale to retain intensity variations required for edge and contour detection.
Applying thresholding and dilation to create a binary image that emphasizes the grid lines and digit boundaries.
Implementing Gaussian blur to reduce noise and enhance image quality.
Performing histogram equalization to improve pixel intensity contrast.
Detecting the largest contours using OpenCV, which corresponds to the outer Sudoku grid.
Cropping and resizing the image to ensure consistent input dimensions for digit recognition.
Digit Prediction and Sudoku Solving
The digit images resulting from the image processing pipeline are resized and segmented into smaller squares representing individual Sudoku digits. Each digit image is then passed through the trained CNN model for digit prediction. The resulting digit values are used to create a 2D Sudoku array. To ensure accuracy, a backtracking algorithm based on Depth-First Search (DFS) is developed to solve the Sudoku puzzle.

<b>Learnings and Technologies</b>
Through the development of this project, the team gained insights into various cutting-edge technologies and concepts, including:

Computer Vision techniques for image processing and contour detection.
Deep Learning, including CNN architecture design and model training.
Algorithm development, particularly the implementation of a DFS-based Sudoku solving algorithm.
This project serves as a comprehensive learning experience, merging Computer Vision, Deep Learning, Image Processing, and Algorithm design into a single, practical application.
