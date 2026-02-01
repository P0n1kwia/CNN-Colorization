\# Image Colorization: TensorFlow vs. PyTorch



This project focuses on the task of \*\*automatic image colorization\*\* using Deep Learning. The goal is to transform grayscale images (L channel) into full-color images (predicting AB channels) using the \*\*LHQ-1024\*\* dataset. 



A key feature of this repository is the comparative implementation of the model in two major frameworks: \*\*TensorFlow/Keras\*\* and \*\*PyTorch\*\*.



\##  Dataset: LHQ-1024

The project utilizes the \*\*LHQ-1024 (Landscape High Quality)\*\* dataset, which contains high-resolution nature and landscape photography.

\* \*\*Source:\*\* \[Kaggle - LHQ-1024](https://www.kaggle.com/datasets/dimensi0n/lhq-1024)

\* \*\*Pre-processing:\*\* Images are converted from RGB to the \*\*CIE Lab\*\* color space. 

&nbsp;   \* \*\*Input:\*\* `L` channel (Lightness).

&nbsp;   \* \*\*Target:\*\* `a` and `b` channels (Color dimensions).



\## Model Architecture

The core model is an \*\*Autoencoder\*\* designed with:

1\. \*\*Encoder:\*\* Downsamples the image using Convolutional layers to extract spatial features.

2\. \*\*Bottleneck:\*\* Captures the most compressed representation of the landscape.

3\. \*\*Decoder:\*\* Uses UpSampling and Convolutional layers to reconstruct the color channels.



\### Loss Functions

In the upgraded TensorFlow version, we experiment with:

\* \*\*MSE (Mean Squared Error)\*\*

\* \*\*Huber Loss\*\* (to reduce sensitivity to outliers and improve color consistency).



