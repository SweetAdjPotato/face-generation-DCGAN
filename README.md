# Face Generation using DCGAN

## Table of Contents

1. [Project Overview](#project_overview)
2. [Installation](#installation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Discussion](#discussion)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Project Overview <a name="project_overview"></a>

In this project, a deep convolutional generative advasarial network (DCGAN) is designed and trained on the [CelebFaces Attributes Dataset (CelebA)](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html). The goal is to train the generator to generate new images of faces that look as realistic as possible. The imput images are preprocessed and resized to 32 by 32 to reduce training time. Sample images are given below.

<img src="sample_images.png"/> 

## Installation <a name="installation"></a>

1. Python versions 3
2. Library and packages: pytorch, numpy, matplotlib, pickle

## File Descriptions <a name="files"></a>

* **dlnd_face_generation.ipynb:** the main notebook contains all the codes

* **dlnd_face_generation.html:** html format of dlnd_face_generation.ipynb

* **workspace_utils.py:** functions used in the notebooks

* **problem_unittests.py** unit test functions

* **sample_images.png** sample training faces

* **sample_result_epoch1.png** sample generated faces at epoch 1

* **sample_result_epoch20.png** sample generated faces at epoch 20

## Results<a name="results"></a>

Faces start to emerger with the increase of training epochs. Some sample results are given below.

Epoch 1:

<img src="sample_result_epoch1.png"/> 

Epoch 20:

<img src="sample_result_epoch20.png"/> 

## Discussion<a name="discussion"></a>

* The generated faces are mostly white as expected since the dataset is biased with mostly white celebrities, which makes it difficult for the model to generate some new faces other than that. One way to improve the model is to use a unbiased dataset with all kinds of faces.

* The iamge resolution is low as expected since the input images are resized to 32 by 32 as required to reduce training time. The image resolution can be improved through larger size input images (128 by 128). With larger images, more layers can then be added in the discriminator and generator to further improve the model.

* The generator has difficulty to generate some features such as sunglasses, genders. And some generated faces are very similar to each other. Possible reason might be that the network is not deep enough to capture all these features. Using larger image size as well as improving the model size might help learning these features better.

* In addition, training more epochs and/or implementing evolving learning rate to see if the model will be improved further.

## Licensing, Authors, and Acknowledgements<a name="licensing"></a>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Acknowledge to [Udacity](https://www.udacity.com/) for providing the starter codes.  
