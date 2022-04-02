## Notes

1.The main code for the project is stored in the "A_Microchip_Object_Detection_System_Based_On_Tensorflow2_EfficientDet_model.ipynb" file.

2.The project was carried out as early as 2020, and some of the tools may not be compatible with today's Python toolkit versions. The code can be run on Jupyter Notebook, but due to version issues, there is no guarantee that each step will be successfully completed.

3.But you can still click the orange button "open in colab" before the contents of the "A_Microchip_Object_Detection_System_Based_On_Tensorflow2_EfficientDet_model.ipynb" file to see the process details and results saved while the project was running.

# MengxueTao/A-Microchip-Object-Detection-System-Based-On-TensorFlow2-EfficientDet-Model
![image](https://user-images.githubusercontent.com/100255548/161363176-b08ac68e-ec5f-4ab1-aa5c-9215648c12d7.png)
[View source in GitHub](https://github.com/MengxueTao/a-microchip-object-detection-system-based-on-TensorFlow2-EfficientDet-model.git)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![image](https://user-images.githubusercontent.com/100255548/161363282-fb8cc01f-af89-4c6f-b249-8abeeacfdb68.png)
[Open in Google colab](https://colab.research.google.com/github/MengxueTao/a-microchip-object-detection-system-based-on-TensorFlow2-EfficientDet-model/blob/main/A_Microchip_Object_Detection_System_Based_On_Tensorflow2_EfficientDet_model.ipynb)

This project uses TensorFlow2.6 to construct microchip object detection based on EfficentDet network model. The effect is shown in figure 1. 
![1](https://user-images.githubusercontent.com/100255548/161363651-b8a83d9d-1610-4317-81a6-ce253629133b.png)

The model construction process is as follows: 

1. First, prepare 149 microchip data sets and sorted them into four types: Raspberry_Pi_3, 
Arduino_Nano, ESP8266, Heltec_ESP32_Lora. 

2. Then, utilize LabelImg software to annotate the images and split the data into two parts: a 
training set and a test set. Each image is paired with an XML file (including chip type, and x and Y coordinates in the image). 

3. Implement the EfficentNet network model based on TensorFlow for training. 
![image](https://user-images.githubusercontent.com/100255548/161363664-5af0b6c7-c50c-4a22-a445-8f366ff29be4.png)

4. Images were read for training, epoch=8000, bach_size=16, and tensorboard was used to observe the training accuracy and save the model as ‘saved_model.pb’using‘tf.saved_model.save’. 

5. Apply the exported model for object detection of microchip images. Use‘TF.saved_model.load’ 
to load the model, perform object detection on the input picture, and mark the rectangular box on 
the object image, as well as classification and precision.
