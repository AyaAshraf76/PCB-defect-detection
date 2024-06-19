# PCB_defect_detection
This project demonstrates the use of the object detection model YOLOv8 for the task of detecting surface defects on Printed Circuit Boards (PCBs) as shown below. The defects detected include missing holes, mouse bites, open and short circuits.
<p align="center"> 
  <img src="https://www.mdpi.com/electronics/electronics-12-02821/article_deploy/html/images/electronics-12-02821-g001.png" width="350" title="PCB defects"> 
</p> 
<p align="center">
  <em>Six types of common PCB surface defects</em>
</p>

## 1. Dataset
The dataset used in this project is the "PCB Dataset Defect" dataset, which is available on Roboflow. The dataset contains 693 open-source PCB defect images.

You can access the dataset using the following link and download into different formats:
https://universe.roboflow.com/object-detection-dt-wzpc6/pcb-dataset-defect

Original Credit:
https://github.com/Ironbrotherstyle/PCB-DATASET

The dataset is split into three folders: train, test, and validation.

## 2. Train the model
The model is trained on a dataset to learn the PCB defects and patterns necessary for accurate object detection.
![Screenshot 2024-06-19 003143](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/5f68f667-e820-43cc-8793-67ccb174ba1e)
Training the YOLOv8 model for a greater number of epochs can lead to enhanced accuracy. During an epoch, the model iterates through the entire training dataset, learning from the examples and updating its internal parameters to improve its performance. Extending the training process by increasing the number of epochs gives the model more opportunities to learn and optimize its defect detection capabilities on printed circuit boards.

## 3. Validate the model
The trained model is evaluated on a separate validation dataset to assess its performance and identify areas for improvement.

## 4. Prediction phase
Once trained and validated, the model can be used to make predictions on new, unseen data, detecting and localizing PCB defects.

