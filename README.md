## Overview
This project is the second project of udacity's deep learning nanodegree.

## What is This Project
The project is split into there parts:
- Face detector, that returns is there a human face or not.
- Dog detector, that returns is there a dog or not.
- Dog bread classifier, that return the bread of given dog image.
- A model that tells is there a human, dog or neither in an image (Not required from udacity)

## What I Did to Stand Out:
I decided it would be better if I use also NN to tell does this image contain human, dog neither instated of using opencv to this task.
So I took the following steps:
- Got a small set of imagenet, 8 classes to be exact. labled these images as none.
- Merged this dataset with existing human&dog images dataset
- The dog images dataset was labeled by bread, and the human was labled by person name, so I created a custom dataset that takes these images and also give them the following lables dog, none and human.
- Used pretrained vgg16, reset the weights of second to last fully connected layer and changed the output size of the last fully connected layer.
- Stoped the learning in the CNN part, and only trained the fc layers.

The result was 99% accuracy on the test set. Although this result sound amazing but I doubt that it will represent the real world, but it's good enough for the purposes of this project.

