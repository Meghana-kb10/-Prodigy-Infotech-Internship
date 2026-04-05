Neural Style Transfer using PyTorch
Prodigy InfoTech Internship – Task

◆ PROJECT OVERVIEW

This project implements Neural Style Transfer using a pre-trained VGG19 model in PyTorch.

The goal is to combine two images:
◻ A content image (structure)
◻ A style image (artistic appearance)

to generate a new image that preserves the structure of the content while adopting the artistic style of the reference image.

◆ OBJECTIVES

◻ Understand the concept of Neural Style Transfer
◻ Use a pre-trained convolutional neural network (VGG19)
◻ Extract content and style features from images
◻ Generate a stylized image through optimization
◻ Learn how loss functions guide image transformation

◆ TECHNOLOGIES USED

◻ Python
◻ PyTorch
◻ Torchvision
◻ PIL (Python Imaging Library)
◻ Matplotlib
◻ Google Colab

◆ WORKFLOW EXPLANATION

◻ ENVIRONMENT SETUP:

◻ Required libraries such as PyTorch, Torchvision, and Matplotlib are installed
◻ GPU availability is checked and used for faster computation

◻ IMAGE LOADING:

◻ Content and style images are uploaded
◻ Images are resized and converted into tensors
◻ Data is moved to the selected device (CPU/GPU)

◻ MODEL LOADING (VGG19):

◻ A pre-trained VGG19 model is used
◻ Only feature extraction layers are utilized
◻ The model is set to evaluation mode to prevent training updates

◻ FEATURE EXTRACTION:

◻ Specific convolutional layers are selected
◻ Features from these layers represent different levels of abstraction
◻ Content and style features are extracted separately

◻ GRAM MATRIX COMPUTATION:

◻ Style representation is computed using Gram matrices
◻ This captures texture and patterns rather than structure
◻ Gram matrices are calculated for all selected style layers

◻ INITIALIZATION OF GENERATED IMAGE:

◻ The generated image is initialized using the content image
◻ It is set as a trainable variable for optimization

◆ LOSS FUNCTIONS

CONTENT LOSS

◻ Measures difference between generated image and content image
◻ Ensures structural similarity is maintained

STYLE LOSS

◻ Measures difference between Gram matrices
◻ Ensures artistic style is transferred

TOTAL LOSS

◻ Combination of content and style loss
◻ Controlled using weighting factors

◻ OPTIMIZATION PROCESS:

◻ The generated image is optimized using the Adam optimizer
◻ The model updates the image iteratively
◻ Loss is reduced over multiple steps

◻ TRAINING PROCESS:

◻ The optimization runs for several iterations (e.g., 300 steps)
◻ Loss decreases progressively
◻ The image gradually transforms to match the desired style

◆ FINAL OUTPUT

◻ The final stylized image combines content and style
◻ The result is displayed and saved locally

◆ KEY CONCEPTS

◻ NEURAL STYLE TRANSFER

◻ A technique that blends content and artistic style using deep learning

◻ VGG19 MODEL

◻ A convolutional neural network used for feature extraction
◻ Helps capture both low-level and high-level image features

◻ GRAM MATRIX

◻ Represents correlations between feature maps
◻ Used to capture texture and artistic patterns

◻ OPTIMIZATION-BASED GENERATION

◻ Instead of generating from scratch, the image is gradually modified
◻ The model learns by minimizing loss functions

◆ RESULTS

◻ Successfully generated a stylized image
◻ Preserved content structure while applying artistic style
◻ Observed gradual improvement during optimization

◆ CHALLENGES FACED

◻ High computational cost
◻ Longer processing time for better quality
◻ Balancing content and style weights

◆ LEARNINGS

◻ Deep understanding of CNN feature extraction
◻ Practical experience with PyTorch
◻ Importance of loss functions in generative tasks
◻ Insight into how AI can blend artistic styles

◆ PROJECT STRUCTURE
Neural-Style-Transfer
 ┣ main.ipynb
 ┣ content.jpg
 ┣ style.jpg
 ┣ styled_output.jpg
 ┗ README.md
◆ ACKNOWLEDGEMENT

This project was completed as part of the Prodigy InfoTech Internship, focusing on practical applications of Generative AI and deep learning.

◆ CONCLUSION

This project demonstrates how deep learning can be used creatively to merge artistic styles with real-world images. Neural Style Transfer highlights the intersection of AI and creativity, with applications in art, design, and digital media.
