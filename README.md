MNIST Handwritten Digit Classifier - CNN
This part of the project consists of a Convolutional Neural Network (CNN) working function built with PyTorch in order to classify handwritten digits from the MNIST dataset. Here I implemented this as my first computer vision project, built to optimize my technical portfolio for future AI engineering internships.

Project Overview
The main function part here is to build a CNN model that can accurately identify handwritten digits (0-9) from 28x28 grayscale images. Here I implemented 60,000 images for the training part and 10,000 images for the testing part, loaded directly from the standard MNIST benchmark dataset.

Model Architecture
This part of code section consists of multiple working layers in order to process the image data:
-Conv Layer 1: holding 1 input channel and store into 32 filters, using a 3x3 kernel.
-Conv Layer 2: holding 32 input channels and store into 64 filters, using a 3x3 kernel.
-MaxPooling: implemented 2x2 kernel after each conv layer.
-Fully Connected Layer 1: holding 3136 inputs and store 128 outputs.
-Fully Connected Layer 2: holding 128 inputs and store 10 outputs to match the digits.
-Dropout: implemented 0.25 rate to ensure it retain the integrity and prevent overfitting.
-Activation: ReLU function used throughout the process.

Training Configuration
Then with these it starts making the training process using:
-Optimizer: Adam (lr=0.001)
-Loss Function: CrossEntropyLoss
-Epochs: 5
-Batch Size: 64

RESULTS
Metric,Value
Test Accuracy,99.15%
Macro Precision,0.99
Macro Recall,0.99
Macro F1-Score,0.99

Training Loss Progress
Epoch,Loss
1,0.1961
2,0.0599
3,0.0453
4,0.0350
5,0.0292

Key Findings
After it starts making comparisons on the test set, here are the results:
-The model successfully achieved 99.15% accuracy on the test set after only looping 5 epochs of training.
-Digit 7 was the hardest to classify, with 12 samples jumping to the wrong conclusion as digit 2 due to similar visual structure.
-Digit 5 had 10 samples misclassified as digit 3 due to similar curves.
-If it is digits 0 and 1, they achieved perfect F1-scores of 1.00.
-Then lastly the training loss curve showed a steep drop after epoch 1, indicating the model fully matches and learned core digit features quickly.

Libraries Used
-PyTorch
-torchvision
-matplotlib
-numpy
-scikit-learn
-seaborn

How to Run
Clone this repo
install dependencies:
pip install torch torchvision matplotlib numpy scikit-learn seaborn

THANK YOU FOR VIEWING!!
