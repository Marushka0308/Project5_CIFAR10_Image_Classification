# Project5_CIFAR10_Image_Classification
Classifying images in CIFAR 10 dataset into 10 different classes using Pytorch

## DATASET 
CIFAR-10 dataset consists of 60k 32x32 px color imgs w/ 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. Each class contains 6k imgs, w/ 50k training images and 10k test images. Load the CIFAR 10 dataset, transform data to tensor and normalize becuase NNs are scale sensitive. Very clean dataset, no data preprocessing required. Create data loaders to load training and testing data in batch sizes of 32 and shuffle training data only.

## MODEL TRAINING: DEFINE CONVOLUTIONAL NEURAL NETWORKS
Define 2 d convolutional layers since we're working with images. Convolutional layer > ReLU as activation > Max pooling. Then repeat and finally flatten for NN. Create fully connected layer > ReLU activation function > Use dropout for regularization - to drop out 50 percent of neurons for better generalization > another fcl which outputs ten neurons (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck).

Define loss function as cross entropy loss and optimizer as Stochastic Gradient Descent to optimize model parameters. Start model training: for each epoch, for features and target in training set, reset the gradients to 0, get model output for given input, calculate loss using cross entropy loss, backpropagate loss, take a step with optimizer in right direction.

## MODEL EVALUATION
Evaluate model on unseen data. Disable gradient calculation because we're not doing training. Get predictions for test set, calculate the max arg from the predictions to find highest activation and find accuracy.

