# yolov2-tiny-custom-dataset-for-darknetros-on-jetson-nano

Proje Goal

The objective of this project was to leverage a camera to detect objects and navigate between them. Specifically, the focus was on detecting plants and maneuvering through them autonomously. Given our limited budget, we utilized a Jetson Nano Development Kit to run an AI model for object detection.

Using ROS1 as the robotics framework, we integrated the darknet_ros package, which facilitates the use of YOLO models for object recognition with high accuracy. The Jetson Nano 4GB, while efficient, has limited resources, which led us to carefully select the most suitable YOLO model for our application.

We chose YOLOv2-tiny, a lightweight and efficient version of the YOLO object detection model, as it strikes a balance between speed and accuracy. To achieve the desired performance, we created a custom dataset tailored to our needs and trained a model that could detect plants and obstacles effectively, enabling smooth navigation for our robot.

With the project goal clearly defined and the choice of YOLOv2-tiny established, the next crucial step was to train the custom model and seamlessly integrate it with ROS for real-time object detection and navigation. Below is a detailed explanation of the steps involved in training the model and implementing it on the Jetson Nano using ROS.

*************************************************************************************************
 - Step to train custom dataset with yolov2-tiny
*************************************************************************************************
 -prediction make with difernt train model
 
![predictions_4](https://github.com/user-attachments/assets/c390dfa5-8399-4fd7-bf4b-ba8fb610dfd2)
![predictions_3](https://github.com/user-attachments/assets/91d9623d-ee4c-4ce1-b80a-26a20380871a)
![predictions_2](https://github.com/user-attachments/assets/6d9e36ad-b28d-41cb-b5ba-ac78b1f80e48)
![predictions_1](https://github.com/user-attachments/assets/62306df2-1b55-4e93-8225-777c0317e754)
![predictions_0](https://github.com/user-attachments/assets/73242d7e-e686-4be2-a091-cafed466318e)
