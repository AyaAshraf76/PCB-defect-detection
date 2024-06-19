![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/105e1b48-4c0a-43d3-83ec-bd3303b8947f)# PCB_defect_detection
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

### 1. Confusion matrix 
A confusion matrix in YOLO summarizes the performance of the object detection model by showing the counts of true positives, false positives, true negatives, and false negatives as shown below in the figure.
https://blog.roboflow.com/content/images/size/w2000/2022/11/confussion-matrix-2.png
It helps in understanding how well the model is detecting objects (precision and recall) and where it might be making mistakes (confusion between classes).
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/da26f714-2adb-446b-9d57-54692efeeddb)

### 2. F1 Confidence Curve
The F1 score is a measure of a model's accuracy that considers both precision and recall.
The confidence curve helps you choose the right threshold for your application. For example, in some cases, you might prioritize higher precision (fewer false positives), while in others, you might need to detect as many objects as possible (higher recall), even if it means accepting more false positives.
In brief, A higher F1 score indicates better performance, and the confidence threshold at which the F1 score is maximized is often considered the optimal threshold for making predictions.
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/c5f496a7-933e-40c9-a3e5-30aa289df4b0)

### 3. Precision-Recall Curve

The Precision-Recall Curve is a plot that shows the trade-off between precision and recall for different threshold values.
Precision: How many of the items identified as positive are actually positive.
Recall: How many of the actual positives were identified correctly.
https://lh3.googleusercontent.com/X3iU9gn6QFMV-rMWevV2W_w562vdbdr9n-lBlVJxFDyv-XcIwR_s1ZAkZMqnmfsIjXviKKT4KoYb4HI7rp8upFUpCN7DZv39Ys5Bv-o-_RsWFT-nP-ecjqm3UxEJr98cwhhDKijvOy5obdkEekIBMLnFjQzZ5y6b-zwMOwo72L5PLUmLcdPwhl5PVcI5dw

The area under the curve (AUC) is a measure of how well the model is able to distinguish between classes. The closer the curve follows the top-right corner, the more accurate the model is.
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/402cef16-5f7c-497f-9e85-657f818714cd)


## 3. Validate the model
The trained model is evaluated on a separate validation dataset to assess its performance and identify areas for improvement.
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/a448b393-bf9e-4801-89a6-19b4107426be)
The above table shows that with 50% confidence, we are getting an accuracy of 87.5%.

## 4. Prediction phase
Once trained and validated, the model can be used to make predictions on new, unseen data, detecting and localizing PCB defects.
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/7bc62745-c51d-4a26-9158-0975fa73e404)
![image](https://github.com/Lenovo76/PCB-defect-detection/assets/143762427/475a1889-d541-408d-acab-8e416de9f9da)


