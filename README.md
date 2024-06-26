# Image Colorization: Autoencoder

Image colorization using autoencoders is an innovative approach that infuses grayscale images with vibrant hues. Autoencoders, a type of neural network, learn to encode and decode images, forming an internal representation of input data. The aim of this project is to automatically add color to grayscale images using an autoencoder architecture. The process involves several steps, including data preparation, defining the model architecture, training the model, and deploying it for practical use.

## Data Preparation

![training dataset](https://drive.google.com/drive/folders/1aewbl5oAPLR37WTl-1Iadn9PbDklAnoC?usp=drive_link)

For this project, a suitable dataset of grayscale images and their corresponding color versions is required. The dataset should be preprocessed to ensure compatibility with the model architecture. This process may include resizing, normalization, and splitting into training and validation sets.

## Model Architecture

<img src="https://github.com/pooranjoyb/Autoencoder-Colorization/blob/master/data/images/architecture.png" width="50%" alt="Architecture"></img>

- **The Encoder architecture** is a convolutional neural network segment designed for image feature extraction.
- It begins with an input layer accommodating (160*160) and scaled to a range of [-1,1] images. Each convolutional layer is accompanied by batch normalization and max pooling.
- Sequentially, the number of filters increases (64, 128, 256), enabling hierarchical feature capture.
- This architecture progressively abstracts image features for image colorization, providing efficient information encapsulation through its layers.
- Then, **Decoder**, a pivotal component of the Autoencoder, reconstructs images from a compact  representation. Initiated by an input layer shaped to match the Encoder's output, the architecture 
unfolds with batch normalization. Conv2DTranspose layers reverse convolution, expanding the representation with strides of 2 and batch normalization.

## Model Training
The training phase involves optimizing the model's parameters to minimize the difference between the predicted colorized images and the ground truth color images. This is achieved by feeding the grayscale images into the autoencoder and adjusting the weights. 

The model was trained with an optimal 35 epochs and with 160 x 160 grayscale and color landscape image sets.



## Dependencies

- Python 3.10.6
- Tensorflow
- NumPy
- cv2
- seaborn

Install the required packages using `pip`:
