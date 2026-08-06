# White-Bread-Mold-Checker

             
            
# Overview

For my project, I decided to make an Ai model that runs Image-net to find out if white bread has mold in it. This model will help people as it can identify mold very accurately, and it will stop people from accidently eating moldy bread.

# The Data set

This model was trained based off of the images in this data set: https://data.mendeley.com/datasets/2cymbb4gt4/1
This dataset contains over 500 images of healthy and moldy white bread through all angles, so no matter which angle the picture is taken, the Ai can tell.

# Image Net

This model is trained with the neural network called image-net. This network allows the Ai to detect images and classify those images with certain labels- in my case good or bad bread. Example image: https://drive.google.com/file/d/1EvOuMW2v6XGsds1MxbbhdJrAOH3kgT6W/view?usp=sharing

# The Algorithm

Once the data set was imported, I ran a long python code to sort the images into 3 folders. Test, train, and validate. I then trained this model using this training script: python3 train.py --model-dir=models/bread_set data/bread_set. I ran this with the default epochs (image cycles), 35.


# File structure

Project Files

| models
| -Bread_set
| -------------tensorboard
| ---------------------------events.out.tfevents
| -checkpoint.pth.tar
| -labels.txt
| -model_best.pth.tar
| -resnet18.onnx

# How to run



    1. Insert your image (via drag and drop) into: jetson-infrence/python/training/classification/data/Bread_set/test/Test_Here

    2. In terminal run command: cd jetson-inference/python/training/classification

    3. Run command: NET=models/Bread_set DATASET=data/Bread_set

    4. Run command: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Test_Here/Image name.(Jpg,png, other image file) Save_name.jpg

    5. Modify Image name and classification as well as what you want to save it under.

    6. Click your new image and in the top left corner there will be the Ai's answer 

# Video Guide

https://drive.google.com/file/d/1hhyPMkI-9dEUJW663SWmjSz1AeRtl9Cv/view?usp=sharing

# Documentation
https://drive.google.com/drive/folders/1BIRU6vex8Otx-OYNA-jgABBV-Hp8XmuO?usp=sharing
