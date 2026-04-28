# CSCI335 Final Project
## Quick to Draw? More Like Quick to Classify!

Google Colab Notebook Link: [https://colab.research.google.com/drive/1dEu1YhPLtTfIHpNCZCcuIsI2v1MAIF1a?usp=sharing](https://colab.research.google.com/drive/1dEu1YhPLtTfIHpNCZCcuIsI2v1MAIF1a?usp=sharing)

## Abstract
This project looks at how well different machine learning models can classify simple hand-drawn images from Google’s "Quick, Draw!" dataset. These sketches are noisy, abstract, and have a lot of variation, which can make them difficult to classify. We compare CNN, SVM, and Vision Transformer (ViT) models based on their accuracy and their ability to distinguish visually similar classes. We hypothesize that models perform better on distinct classes and struggle with similar ones.

## Developers
- Dylan Shaffer
- Michael Reizenstein
- Sam Moll

## Dataset
Google Quick, Draw! Dataset:  
[https://github.com/googlecreativelab/quickdraw-dataset](https://github.com/googlecreativelab/quickdraw-dataset)

The original dataset that is being worked with is simply too large for the scale of this project. The way we decided to handle this issue was to hand select classes that  span a wide variety of everyday objects. With in the variety of classes that we picked we tried to select classes that "grouped" with one or two other classes and then switch to a completely different type of object. (Ex  horses and zebras, so are clock and compass but horse and compass are not similar.) 

We use a subset of 26 classes:
`Horse, Zebra, Shoe, Rollerskate, Cat, Dog, Panda,
Laptop, Computer, Camera, Television, Mushroom, Strawberry, Bread, Bandage, Baseball, Bat, Crab, Clock, Compass, Fan, Lollipop, Soccer ball, Basketball, Stop Sign, Octagon`

We are using the "simplified drawing files" data provided, in which the images are saved in simplified vector strokes where the timing information is removed, and the data has been scaled and positioned into a 256x256 region. The data is in ndjson format with the same metadata as the raw format.

The next step of pre processing was to convert the drawings to a binary 28x28 matrix, where 1 is a line and 0 is nothing space. The final product is a matrix, that can be interpreted into an image.

## How to Run the Project

All code for this project can be run directly in the provided Google Colab notebook labelled "Final Project Code.ipynb" in the `/code` folder or linked above.

There is already a preprocessed version of the dataset included in the repository in the `/data` folder, with a subset of 1,000 images for each of the 26 classes (26,000 images):

- `/data/X_sampled_1000.npy`
- `/data/y_sampled_1000.npy`

To use them:
1. Open the notebook in Google Colab
2. Upload the two files in the `/data` folder to the Colab Notebook Files
3. **Skip to Section 4b** in the Data Preprocessing section of the the notebook
4. Run the Colab Notebook from there to train and evaluate the three models

This avoids the preprocessing step. Otherwise, the Colab Notebook can be run from the start to preprocess the original dataset.

## Models Used
- CNN
- SVM with RBF kernel
- Vision Transformer (ViT)
