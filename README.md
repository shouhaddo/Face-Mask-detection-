# Face-Mask-detection-
In the COVID-19 crisis wearing masks is absolutely necessary for public health and controlling the spread of the pandemic. What if we had a system that could monitor whether people around us are complying with these safety measures?

<b>libraries needed</b><br>
  <br> tensorflow
  <br> Keras
  <br> cv2
  <br> Numpy
  <br>sklearn
  <br> matplotlib
  <br>Pillow PIl
  <br>
  
I have made use of Transfer Learning and thanks to the tensorflow applications api this is a very simple task. The MobileNetV2 model was used to build my classifier network.By using Transfer Learning I am making use of the feature detection capabilities of the pre-trained MobileNetV2 and applying it to our rather simple model. The MobileNetV2 is followed by our DNN composed of GlobalAveragePooling, Dense and Dropout layers. As ours is a binary classification problem final layer has 2 neurons and softmax activation.
A general Adam optimizer along with Categorical_crossentropy loss works well to converge on the most optimum weights for my network.
Here, I have used the popular OpenCV library to take my webcam feed and run it through my model.for face detection cvlib library is used along with method "Detect_face".
The OpenCV implementation is simply a continuous cycle of:
Detect Face
Slice Face Image
Pass through Classifier
Get and Display Prediction

<b>Results : </b>
Accuracry : 99%<br>
Val_Accuracy : 98.6<br>
loss: 0.0166<br>
val_loss: 0.0222<br>


<p align="center">
  <img src="/face mask detection-@code.it29/accuracy.JPG" width="350" title="Accuracy">
  <img src="/face mask detection-@code.it29/loss.JPG" width="350" alt="loss">
</p>

