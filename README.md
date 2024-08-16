# Medical Image Registration Project

This is the final project for the Computer Vision Course Summer 2024 at University of Cologne.
The goal of the project was to implement a non-rigid image registration network.

## Single- vs Multiorgan Image Registration

In this project we experimented with the AbdomenCTCT dataset from
the [Learn2Reg 2020 Task Challenge](https://learn2reg.grand-challenge.org/Learn2Reg2020/).
We explored if splitting the image using a predefined segmentation and learning individual models for each segmentation
could improve registration performance.

For this we used the Registration Framework [VoxelMorph](http://voxelmorph.mit.edu/) to train models for each organ
segmented in the AbdomenCTCT
dataset and combined these individual registrations to a final registration. We then compared this registration to a
VoxelMorph model that uses all organs as input instead of single organs, and to a registration performed using the
ANTsPy framework.

## Folder structure

The AbdomenCTCT directory contains all notebooks relevant for the final project.

- The ..._train.ipynb notebooks contain the code used to train the VoxelMorph models.
- The ...:test.ipynb notebooks contain the code used to evaluate the various models.
- The AbdomenCTCT_ANTsPy.ipynb notebook contains the code that was used to evaluate the ANTsPy registration
- The models/ directory contains the weights of the trained models.

The others/ directory contains notebooks that were created to explore other models or datasets but were not relevant for
the final project Hand In

## Requirements

We used the [VoxelMorph](http://voxelmorph.mit.edu/) Framework at version 0.2. which requires TensorFlow Version <2.15.
We therefore used Python
Version 3.9.19 or 3.10 with TensorFlow Version 2.15.

The ANTsPy Notebook uses [AntsPy](https://github.com/ANTsX/ANTsPy) version 0.5.3 and was run on Python Version 3.12. as
it wouldn't work with Python 3.10.
The ANTsPy Evaluation takes quite a bit of time when Run on Colab using the CPU, we therefore recommend running this
Notebook either on your local machine or using the T4 Runtime of Colab.

Other libraries used in the AbdomenCTCT directory included:

- [jupyter](https://jupyter.org/)
- [neurite](https://github.com/adalca/neurite)
- [nibabel](https://nipy.org/nibabel/)
- [matplotlib](https://matplotlib.org/)
- [numpy](https://numpy.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [tqdm](https://tqdm.github.io/)

To install all libraries/frameworks you can run the following command

``` pip install jupyter voxelmorph neurite tensorflow==2.15 nibabel matplotlib numpy scikit-learn tqdm antspyx```

For the notebooks contained in the others/ directory it might be necessary to install further libraries e.g. torch or
natsort