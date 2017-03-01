# Your First Neural Network
## Introduction
In this project, you'll get to build a neural network from scratch to carry out a prediction problem on a real dataset! By building a neural network from the ground up, you'll have a much better understanding of gradient descent, backpropagation, and other concepts that are important to know before we move to higher level tools such as Tensorflow. You'll also get to see how to apply these networks solve real prediction problems!

The data comes from the UCI Machine Learning Database.

## Instructions
1. `git clone https://github.com/mantelsolutions/nd101.git`
2. cd into the dlnd-your-first-network folder that you just cloned.
3. Download anaconda or miniconda based on the instructions in the Anaconda lesson.
4. Create a new conda environment:
    `conda create --name dlnd python=3`
    `source activate dlnd`
5. Ensure you have numpy, matplotlib, pandas, and jupyter notebook installed by doing the following:
    `conda install numpy matplotlib pandas jupyter notebook`
6. Run the following to open up the notebook:
    `jupyter notebook dlnd-your-first-neural-network.ipynb`

## Activation functions

### Rectified Linear Units

f(x) = max(x,0)

A rectified linear unit has output 0 if the input is less than 0, and raw output otherwise

#### Drawbacks

It's possible that a large gradient can set the weights such that a ReLU unit will always be 0. These "dead" units will always be 0 and a lot of computation will be wasted in training.

This will happen if the learning rate was too high.

### Softmax

The softmax function squashes the outputs of each unit to be between 0 and 1, just like a sigmoid. It also divides each output such that the total sum of the outputs is equal to 1.