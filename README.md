# Face Sketch to Realistic Image Generation using GAN

This repository contains an image generation system using Generative Adversarial Networks (GANs) to convert face sketches into realistic photos. Follow the steps below to set up, train, and evaluate the model.

## Installation

### Step 1: Install Dependencies
Install the required packages by running:

```bash
pip install -r requirements.txt
```

### Step 2: Install Keras-Contrib
Keras-Contrib is needed for additional Keras functionalities. Follow these steps to install it:

```bash
git clone https://www.github.com/keras-team/keras-contrib.git
cd keras-contrib
python setup.py install
```

Alternatively, refer to [this Medium article](https://medium.com/@kegui/how-to-install-keras-contrib-7b75334ab742) for more installation options.

## Data Augmentation
Begin by performing data augmentation on the sketch dataset to enhance the training quality. Use the provided [notebook](https://github.com/gauthamnholla/Sketch-to-Image-via-Neural-Network-/blob/main/sketch/sketch-image/Data%20Augmentation.ipynb) to apply data transformations.

## Training the GAN Model
Use the provided notebook to start training the GAN model for face sketch-to-image transformation.

## Performance Evaluation
Measure the model’s performance by calculating:

1. **SSIM (Structural Similarity Index)**: Measures the similarity between the generated image and the ground truth.
2. **Verification Accuracy (L2-norm)**: Measures the verification accuracy of the generated images.

Refer to the performance measurement notebook for instructions on how to calculate these metrics.

## Testing
To generate a single image from a sketch, use the testing notebook.

## References
This project draws on key works in face photo-sketch synthesis and recognition:

1. **X. Wang and X. Tang** (2009). "Face Photo-Sketch Synthesis and Recognition." *IEEE Transactions on Pattern Analysis and Machine Intelligence (PAMI)*, 31(11), 1955-1967.
2. **W. Zhang, X. Wang, and X. Tang** (2011). "Coupled Information-Theoretic Encoding for Face Photo-Sketch Recognition." *Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)*.
