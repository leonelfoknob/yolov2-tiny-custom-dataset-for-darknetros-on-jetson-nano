# yolov2-tiny-custom-dataset-for-darknetros-on-jetson-nano

## Proje Goal

The objective of this project was to leverage a camera to detect objects and navigate between them. Specifically, the focus was on detecting plants and maneuvering through them autonomously. Given our limited budget, we utilized a Jetson Nano Development Kit to run an AI model for object detection.

Using ROS1 as the robotics framework, we integrated the darknet_ros package, which facilitates the use of YOLO models for object recognition with high accuracy. The Jetson Nano 4GB, while efficient, has limited resources, which led us to carefully select the most suitable YOLO model for our application.

We chose YOLOv2-tiny, a lightweight and efficient version of the YOLO object detection model, as it strikes a balance between speed and accuracy. To achieve the desired performance, we created a custom dataset tailored to our needs and trained a model that could detect plants and obstacles effectively, enabling smooth navigation for our robot.

With the project goal clearly defined and the choice of YOLOv2-tiny established, the next crucial step was to train the custom model and seamlessly integrate it with ROS for real-time object detection and navigation. Below is a detailed explanation of the steps involved in training the model and implementing it on the Jetson Nano using ROS.

*************************************************************************************************
## Step to train custom dataset with yolov2-tiny

This project was executed on Google Colab, with all files saved in Google Drive for training YOLOv2-tiny. Follow these steps to set up your environment and train the model:

1. Create a Directory Structure
First, create a new, empty folder and name it yolov2_tiny_custom (or a name of your choice). Inside this folder, create the following four empty subdirectories:

 - pt-weight: This will contain the pre-trained weights of the model for training.
 - images: Store your dataset images and their respective labels here. For this project, the images were labeled using Roboflow.
 - cfg: This will contain the configuration files that will be used to train the YOLOv2-tiny model.
 - backup: After the training is complete, this folder will store the trained models and their various checkpoints.
Additionally, once you clone the darknet repository, a new folder named darknet will be created inside the parent directory.

2. Add Essential Files
In addition to the above folders, you'll need to add several important files from this repository to your project:

 - process.py: This Python script helps you split your dataset into training and validation sets. Make sure to modify the file paths to match your dataset locations before running the script.
 - custom.names: This file contains the names of the objects/classes you want to detect with your model.
 - detector.data: This file stores the paths to your dataset's images and labels, and it helps link them to the training process.

3. Run process.py
Execute the process.py script after configuring it with the correct dataset paths. This script will generate two text files:

 - train.txt: A file containing the paths of images to be used for training.
 - test.txt: A file containing the paths of images to be used for validation.

4. Proceed with Training
Now that the folder structure and required files are in place, you can proceed by following the instructions in the Colab notebook shared in this repository. The notebook will guide you through the process of compiling darknet, loading the dataset, and starting the training process.

## Implementation of the model in darknet_ros package (ROS1)
 -prediction make with difernt train model
 
![predictions_4](https://github.com/user-attachments/assets/c390dfa5-8399-4fd7-bf4b-ba8fb610dfd2)
![predictions_3](https://github.com/user-attachments/assets/91d9623d-ee4c-4ce1-b80a-26a20380871a)
![predictions_2](https://github.com/user-attachments/assets/6d9e36ad-b28d-41cb-b5ba-ac78b1f80e48)
![predictions_1](https://github.com/user-attachments/assets/62306df2-1b55-4e93-8225-777c0317e754)
![predictions_0](https://github.com/user-attachments/assets/73242d7e-e686-4be2-a091-cafed466318e)
