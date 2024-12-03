# Hybrid Image Generation Using Neural Style Transfer

This repository demonstrates how to use Neural Style Transfer (NST) for generating hybrid images by blending the content of one image with the style of another. The notebook showcases the application of deep learning models, particularly VGG19, for extracting image features and using them to produce aesthetically interesting results.

## Project Overview

In this project, we apply the concept of **Neural Style Transfer (NST)** to create hybrid images by combining:
- **Content Image**: An image whose content is preserved.
- **Style Image**: An image whose artistic style is transferred onto the content image.

By leveraging pre-trained deep learning models such as VGG19, we extract content and style features, and then optimize a target image to blend both images' content and style in a visually appealing manner.

## Paper Reference

The concept of **Neural Style Transfer** was introduced by **Leon A. Gatys**, **Alexander S. Ecker**, and **Matthias Bethge** in their paper titled:

**"A Neural Algorithm of Artistic Style"**  
Published in *arXiv:1508.06576*.

Link to the paper: [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)

This paper forms the basis of the techniques applied in this notebook.

## Steps in the Notebook

1. **Preprocessing**:  
   - Resize images to a consistent size.
   - Normalize images to match the expected input for VGG19.
   - Add necessary dimensions for batch processing in PyTorch.

2. **Feature Extraction**:  
   - Extract features from both the style and content images using a pre-trained VGG19 model.
   - Compute the **Gram Matrix** for style features to capture the correlations between different feature maps.

3. **Optimization**:  
   - Initialize a target image from the content image.
   - Use a loss function that combines content loss and style loss to iteratively update the target image, minimizing the difference between the extracted features and the target.

4. **Postprocessing**:  
   - Convert the processed image back to a displayable format.
   - De-normalize and clamp pixel values to ensure they lie within the range [0, 1].

5. **Visualization**:  
   - Display the original content, style, and the resulting hybrid image.
   - Analyze the impact of preprocessing and postprocessing transformations on the image data.

## Requirements

To run this notebook, you need to have the following Python packages installed:

- `numpy`
- `requests`
- `pandas`
- `IPython`
- `matplotlib`
- `torch`
- `torchvision`
- `Pillow`
- `tqdm`

You can install the required packages using the following:

```bash
pip install torch torchvision matplotlib numpy pandas pillow