# Face-Mask-Detection

### Description:
The project aims to detect whether a person is wearing a face mask or not using a saved file or in real-time using PyTorch. A pre-trained **ResNet50 model** is used in this project. The system captures video frames from a webcam, applies face detection to locate faces in the frames, and then utilizes a deep learning model to classify each detected face as either wearing a mask or not.

### Requirements:
torch==2.0.1+cu118 <br>
torchvision==0.9.1+cu118 <br>
mtcnn==0.1.1 <br>
numpy==1.23.5 <br>
opencv-python==4.7.0.72 <br>
Pillow==9.4.0 <br>
matplotlib==3.6.3 <br>
tensorflow==2.12.0
<br>
### For downloading the Dataset and Trained model (.pt file) :- <br>
https://www.kaggle.com/datasets/raghavanvaidhyaraman/face-mask-detection-project
<br>
## Two parts of the project:

### Training the Face Mask Detection Model:
   - The project starts with training a face mask detection model using a pre-trained ResNet model.
   - A dataset of 530 images is used for training, validating, and testing the model.
   - The pre-trained ResNet model, specifically ResNet-50, is employed as a feature extractor, and the final fully connected layer is modified to have two output neurons representing mask and no-mask classes.
   - The model is trained using the dataset, and the training process involves optimizing the model's parameters using an Adam optimizer and and the metric used is cross-entropy loss.
   - After training, the model is saved to as a .pt file for later use during real-time face mask detection.

### Face Mask Detection either using File Path or Real Time Detection (Front Camera):
   - Once the model is trained and saved we can use it for face mask detection.
   - This project can do facemask detection on a saved image just by giving the file path as input.
   - The project mainly focuses on real-time face mask detection using OpenCV.
   - The system captures video frames from the webcam and applies face detection using the Haar cascade classifier provided by OpenCV.
   - For each detected face, the model is utilized to classify whether the person is wearing a mask or not by passing the face through the trained model.
   - The result is then displayed on the screen by drawing a rectangle around the face and adding a label indicating whether the person is wearing a mask or not.
   - The process continues in real-time, detecting faces and updating the display accordingly.
   - The system allows the user to exit the application by pressing the 'q' key.

The project combines deep learning techniques with computer vision to address the important task of face mask detection. It can be applied in various settings, such as public spaces, workplaces, and healthcare facilities, to help ensure adherence to face mask policies and promote public health and safety.

## Output Screenshots:
### Face Mask Detection either using File Path:
**Path with mask:** <br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/path1.png)
<br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/path2.png)
<br> <br>
**Path without mask:** <br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/path3.png)
<br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/path4.png)
<br> <br> <br>
### Real Time Face Mask Detection (Front Camera):
**With mask:** <br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/Screenshot2.png)
<br> <br>
**Without mask:** <br>
![alt text](https://github.com/raghavan93513/Face-Mask-Detection/blob/main/SampleImages/Screenshot1.png)
