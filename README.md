# SafeShop_Camera_MaskDetection
### Repository for Face Mask Detection made using OpenCV and TensorFlow Object Detection API.

In this pandemic season and lockdown, people are required to follow certain rules and regulations to reduce and prevent further spread of the virus. 
The goal of this camera project is to check if people are wearing masks or not.

The camera can be installed near the entrance of the restaurants(or shops) and the camera will be used for face mask detection. 
Furthermore, camera can be attached to another system (like speakers, screen or even auto-door) to notify the users and restrict their access if mask if not worn(or worn incorrectly)

This Machine Learning model consists of three classes:
  1. with_mask : if the mask is covering the face correctly
  2. without_mask : if the person is not wearing a mask
  3. mask_weared_incorrect : if the person is wearing a mask but it does not cover this face properly
The images used for training this model are taken from the [Kaggle Dataset](https://www.kaggle.com/andrewmvd/face-mask-detection).
There are a few more images used for testing the model which were scraped from the net.

We have used the faster_rcnn_inception_v2 model for training the Face Mask Detector.

The steps for building this model are:
  1. Installing tensorflow-gpu and Anaconda distribution.
  2. Labelling images gather using labelImg and saving the XML files.
  3. Use the XML files to extract the information of the bounding boxes to csv files.
  4. Use the csv files to generate the tf-records file.
  5. Generate a labelmap.pbtxt file according to your classes and configure your training.
  6. Train your object detector till the loss is < 0.05
  7. Save your inference graph and your Face Mask Detector is ready to launch!
  
  The resources used : [Resource](https://www.youtube.com/watch?v=Rgpfk6eYxJA)  (A great Tutorial from Edje Electronics)
