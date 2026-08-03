# White-Bread-Mold-Checker



# What it does

This Ai model runs Image-net to find out if bread has mold in it. This model will helps people as it can identify mold very accuratly as it will stop people from accidentily eating moldy bread.

# The Data set

This model was trained based off of the images in this data set: https://data.mendeley.com/datasets/2cymbb4gt4/1
This dataset containes images of healthy and moldy bread through all angles, so no matter which angle the picture is taken, the Ai can tell.

# The Algorithm

After being trained, this model was tested and is very accurate.


# How to run

1. Insert your image into: jetson-infrence/python/training/classification/data/Bread_set/test/Test_Here

2. In terminal: Cd jetson-inference/python/training/classification

3. Run this command: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Test_Here/Image name.(Jpg,png, other image file) Save_name.jpg

4. Modify Image name and classification as well as what you want to save it under.

5. Click your new image and in the top left corner there will be the Ai's awnser 