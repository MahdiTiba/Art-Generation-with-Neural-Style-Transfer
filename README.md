# Art Generation with Neural Style Transfer

This project implements the Neural Style Transfer (NST) algorithm to generate novel artistic images by combining the content of one image with the style of another.

## Overview

Neural Style Transfer, introduced by Gatys et al. (2015), is a technique that uses convolutional neural networks to blend the content of a source image with the style of another image, producing a new image that appears as if the content is painted in the style of the second image.

## Methodology

The project follows these key steps:

- **Content and Style Representation**: Utilizes a pre-trained VGG19 network to extract feature representations of the content and style images.
- **Cost Functions**:
  - **Content Cost**: Measures the difference between the content image and the generated image in terms of high-level feature representations.
  - **Style Cost**: Computes the difference between the style image and the generated image using the Gram matrix of feature activations to capture style information.
- **Total Cost**: Combines the content and style costs to form the total cost function.
- **Optimization**: Uses gradient-based optimization to minimize the total cost, updating the generated image iteratively to blend content and style.

## Repository Structure

- `Art_Generation_with_Neural_Style_Transfer.ipynb`: Jupyter Notebook implementing the NST algorithm.
- `images/`: Contains example content and style images.
- `output/`: Stores generated images resulting from the NST process.
- `pretrained-model/`: Includes the pre-trained VGG19 model used for feature extraction.
- `nst_utils.py`: Utility functions supporting the NST implementation.
- `LICENSE`: MIT License for the project.
- `Pretrained_Model_LICENSE.txt`: License for the pre-trained VGG19 model.

## Requirements

To run the code, ensure you have the following Python packages installed:

- `numpy`
- `tensorflow`
- `PIL`
- `scipy`

Install the required packages using:

```bash
pip install -r requirements.txt

