# White-Bread-Mold-Checker



# What it does

This Ai model runs Image-net to find out if white bread has mold in it. This model will help people as it can identify mold very accuratly, and it will stop people from accidentily eating moldy bread.

# The Data set

This model was trained based off of the images in this data set: https://data.mendeley.com/datasets/2cymbb4gt4/1
This dataset containes over 500 images of healthy and moldy white bread through all angles, so no matter which angle the picture is taken, the Ai can tell.

# Image Net

This model is trained with the neral network called image-net. This network allows the Ai to detect images and classify those images with certain labels- in my case good or bad bread. Example image: https://drive.google.com/file/d/1EvOuMW2v6XGsds1MxbbhdJrAOH3kgT6W/view?usp=sharing

# The Algorithm

Once the data set was imported, I ran a long python code to sort the images into 3 folders. Test, train, and validate. I then trained this model using this training script: python3 train.py --model-dir=models/bread_set data/bread_set. I ran this with the default epochs (image cycles), 35.


# How to run


    1. Insert your image (via drag and drop) into: jetson-infrence/python/training/classification/data/Bread_set/test/Test_Here

    2. In terminal: Cd jetson-inference/python/training/classification

    3. Then run: NET=models/Bread_set DATASET=data/Bread_set

    4. Run this command: imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Test_Here/Image name.(Jpg,png, other image file) Save_name.jpg

    5. Modify Image name and classification as well as what you want to save it under.

    6. Click your new image and in the top left corner there will be the Ai's awnser 
