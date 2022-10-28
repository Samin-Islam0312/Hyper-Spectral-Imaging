# Hyper-Spectral-Imaging
Hyperspectral imaging (HSI) classification using Deep Learning model. 

# Dataset 
Pavia University HSI, acquired by the ROSIS sensor during a flight campaign. It has 103 spectral bands, containing 610 * 340 pixels, but spectral samples of the image contain no information which is defined as Zero (0). Geometric resolution=1.3 meters.
Link - https://www.ehu.eus/ccwintco/index.php?title=Hyperspectral_Remote_Sensing_Scenes 

Labels of the classification task given below;

![image](https://user-images.githubusercontent.com/69072084/198587332-9c61dabb-a6ff-4832-b246-23be3468b7fb.png)

Dataset has been split into 80/20 for training and test.

![image](https://user-images.githubusercontent.com/69072084/198587572-5558ac40-0294-47a1-a285-84fae73726bc.png)

# Ground truth image
![image](https://user-images.githubusercontent.com/69072084/198587676-f99af267-39a4-4a5d-aa56-5e0460218d98.png)
 
# Model 

A deep learning model of 12 dense layers has been implemented for the classification task. In each layer non-linear function(ReLu) has been used. The first four layers have starts with 128 units. After three dropout layers(rate = 0.2) has been applied after every four layers. The output layer has 10 labels, using softmax function. Adam optimizer has also been added for optimizing the task. Early stopping technique along with model's checkpoint also also been used for computational efficiency, when model stops improving its accuracy and loss. Epoch = 50

# Result

Visualization of the whole classification task 

![image](https://user-images.githubusercontent.com/69072084/198589304-69b31fec-b0b5-4590-a4f2-3f99e4d755b6.png)

Classification Report

![image](https://user-images.githubusercontent.com/69072084/198589268-1b55a9df-6af8-498c-84ef-f2b5a1af793b.png)

Heatmap 

![image](https://user-images.githubusercontent.com/69072084/198589222-736918e0-1af3-452e-9883-69287ae9260b.png)
