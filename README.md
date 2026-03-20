# CSCI335_Final_Project
Quick to Draw? More Like Quick to Classify!

Colab Link: [https://colab.research.google.com/drive/1dEu1YhPLtTfIHpNCZCcuIsI2v1MAIF1a?usp=sharing](https://colab.research.google.com/drive/1dEu1YhPLtTfIHpNCZCcuIsI2v1MAIF1a?usp=sharing)

# Data pre processing
The original dataset that is being worked with is simply too large for the scale of this project. The way we decided to handle this issue was to hand select classes that 
span a wide variety of everyday objects. With in the variety of classes that we picked we tried to select classes that "grouped" with one or two other classes and then switch
to a completely different type of object. (Ex  horses and zebras, so are clock and compass but horse and compass are not similar. 
The next step of pre processing was to convert the drawings to a binary 28x28 matrix, where 1 is a line and 0 is nothing space. We then print it to do a sanity check. The
final product is a matrix, that can be interpreted into an image.
