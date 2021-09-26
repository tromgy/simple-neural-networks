# simple-neural-networks

This repository is a "loose" fork of Michael Nielsen's https://github.com/mnielsen/neural-networks-and-deep-learning

The code is mostly the same, however I converted it to use Python 3, and it is in the Jupyter notebook format. This allowed me to add extensive annotations with detailed explanations (and some proofs) of the math involved.

## Pre-requisites

The code was tested with Python 3.6.8 (Anaconda distribution). It requires the following packages (use `pip install` in your virtual environment):

- dataclasses (this should not be required with Python 3.7 and up)
- pickleshare
- numpy
- Pillow

## Notebooks

There are two notebooks in this repository:

- **neural_network.ipynb** -- implements the network from **Chapters [1](http://neuralnetworksanddeeplearning.com/chap1.html) and [2](http://neuralnetworksanddeeplearning.com/chap2.html)**

- **one-fell-swoop.ipynb** -- implements the same network, but with the fully matrix-based approach (there's no looping over the mini-batch). This was given as a [problem](http://neuralnetworksanddeeplearning.com/chap2.html#problem_269962) in **Chapter 2**.

However, I only saw about 10-20% performance increase with the fully matrix-based approach, not 100% as Michael Nielsen stated in the book. So if you find a problem with my implementation, make a pull request!

## HTML

The folder _html_ contains standalone interactive web pages for these notebooks. These pages use [SageCell](https://sagecell.sagemath.org/) for executing the code. They have been converted from the notebook versions in this folder using [Ingo Dahn's Notebook Player](https://dahn-research.eu/nbplayer). They can be also accessed on [this site](https://dahn-research.eu/nbsite/?path=https%3A%2F%2Fdahn-research.eu%2Fnielsen).

## Images

There are two sets of images, one is the canonical MNIST digits in **mnist.pkl.gz**, and the other is in the **non-MNIST-digits** directory.

The latter ones are my own handwriting scanned and scaled to 28x28 pixel size. They are used for "real-life" tests in addition to the validation set from MNIST.

## Running in VS Code

VS Code can now run Jupyter notebooks. However I've found that markdown parsing of MathJax expressions has slight problems. I use a lot of exressions like this: `$L$th`, but in VS Code it doesn't work properly, as it seems to require a whitespace after the closing `$`. In Jupyter (distributed with Anaconda) and interactive HTML it renders properly, and adding the space doesn't look good there. So I decided not to change any markdown to appease VS Code.
