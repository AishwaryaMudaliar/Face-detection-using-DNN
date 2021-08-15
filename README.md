# Face-detection-using-DNN
This model(DNN) was included in OpenCV from version 3.3. It is based on Single-Shot-Multibox detector and uses ResNet-10 Architecture as backbone.
The model was trained using images available from the web, but the source is not disclosed. OpenCV provides 2 models for this face detector.

1)Floating point 16 version of the original caffe implementation ( 5.4 MB )
2)8 bit quantized version using Tensorflow ( 2.7 MB )

In the code, the image is converted to a blob and passed through the network using the forward() function. The output detections is a 4-D matrix, where

The 3rd dimension iterates over the detected faces. (i is the iterator over the number of faces)
The fourth dimension contains information about the bounding box and score for each face. For example, detections[0,0,0,2] gives the confidence score for the first face, and detections[0,0,0,3:6] give the bounding box.
The output coordinates of the bounding box are normalized between [0,1]. Thus the coordinates should be multiplied by the height and width of the original image to get the correct bounding box on the image.
