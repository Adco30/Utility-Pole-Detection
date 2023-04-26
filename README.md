#Utility Pole Detection using YOLOv8

This project demonstrates the detection of utility poles in images using YOLOv8, a state-of-the-art object detection model. The implementation showcases the training, validation, and prediction steps of the YOLOv8 model for utility pole detection.

#Overview

The project uses the ultralytics package (version 8.0.20) for training and evaluation. It includes code to generate performance metrics such as precision, recall, mAP50, and mAP50-95. The project also provides visualization of training loss (box loss, classification loss, and DFL loss) and model comparison plots.

The dataset used in this project is organized into training, validation, and test folders with the corresponding images and annotations. The model was trained with varying parameters, and the best model was selected based on its performance on the validation set.

#Results

The implementation of YOLOv8 in this project achieved satisfactory results in detecting utility poles in the given dataset. The performance metrics obtained for the trained models are as follows:

    Precision
    Recall
    mAP50
    mAP50-95

Training loss (box loss, classification loss, and DFL loss) and model comparison plots are also provided in the project to analyze the model's performance visually.

#Note

This project is for demonstration purposes only and is not intended to be a complete solution for utility pole detection. The file paths shown in the code will not be available to users, as they are specific to the developer's local setup.
