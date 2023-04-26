
## Utility Pole Detection using YOLOv8 

This repository contains the implementation of a utility pole detection system using YOLOv8. 

## Overview

The YOLOv8 object detection model was used along with data mining techniques for analysis and comparison. The study involved collecting a dataset of Google Street View images containing utility poles, preprocessing the images using Roboflow, training multiple YOLOv8 models with different hyperparameters, and evaluating their performance.

## Methodology

   - Dataset collection: Google Street View images containing utility poles were collected, resulting in a dataset of 198 training images, 19 validation images, and 10 test images. The images were then manually annotated to indicate the locations of utility poles:
   ![Picture1](https://user-images.githubusercontent.com/97653144/234645553-e93fa035-0550-4aa3-ae8f-a15769a3faa9.png)

   - Data preprocessing and augmentation: Roboflow was used to convert annotations into the YOLOv8 format and preprocess the images. Additionally, the dataset was augmented using techniques like auto-orientation, resizing, and rotation to increase diversity and reduce overfitting.

   - Model selection and training: The YOLOv8 object detection model was implemented using PyTorch. The dataset was split into training, validation, and test sets, and the models were trained with different hyperparameter configurations, such as varying the number of epochs and adjusting image size.

    Model evaluation: Models were evaluated on a validation set during the training process. Performance metrics, including precision, recall, and F1-score, were computed, and the model weights resulting in the highest mean Average Precision (mAP) were saved as the best model.

## Results
Model 1 achieved an F1-score of 0.18, precision of 0.3429, and recall of 0.2052. The relatively high precision indicates that this model has a low false positive rate, suggesting that the majority of the detected objects are indeed utility poles. However, the low recall signifies that Model 1 fails to detect a significant portion of utility poles present in the dataset:
 
Model 2 demonstrated an improvement in F1-score (0.27) and recall (0.2257) compared to Model 1, but its precision (0.298) is slightly lower. The increase in recall suggests that Model 2 is more successful in detecting positive instances. The reduced precision, however, indicates that the model also predicts more false positives:

Model 3 achieved an F1-score of 0.22, precision of 0.3377, and recall of 0.1637. Among the three models, Model 3 had the lowest recall, implying that it detects fewer utility poles than the other models.

The results indicate that the models performed reasonably well, but there is still room for improvement. The comparison of different configurations and the use of data mining concepts for analysis provided valuable insights into the performance and limitations of the models.
- Predictions:

Model 1:
<img width="173" alt="m1" src="https://user-images.githubusercontent.com/97653144/234647227-be1bc257-adc2-4238-858b-7bff89513ab3.png">

Model 2:
<img width="160" alt="m2" src="https://user-images.githubusercontent.com/97653144/234647316-59f74c03-37d1-4706-90d4-f358b7b2d480.png">

Model 3:
<img width="162" alt="m3" src="https://user-images.githubusercontent.com/97653144/234647371-a5f2660f-1846-4a7d-b622-deaefba0a82b.png">


The performance of the models was analyzed using 
- Confusion matrices:
![losses](https://user-images.githubusercontent.com/97653144/234645839-ca12c4fc-f26c-4cb7-86c5-fa141baeb1d1.jpg)

- Training losses:
![lossrs](https://user-images.githubusercontent.com/97653144/234646018-6bfeb6ac-99be-4982-9f3e-f01ee7d3784d.png)

- F1-scores, precission and recall: 
![f1scores](https://user-images.githubusercontent.com/97653144/234646410-381f95f2-02aa-4fe8-874b-b4aaa466db40.png)


