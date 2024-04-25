Process:
- Make sure you have a Anaconda Downloaded 
- Open the anaconda terminal 
- Navigate to the folder your project is present 

For Using the face detection on an image run:
python face_detection_image.py --image sample1.png --prototxt deploy.prototxt.txt --model res10_300x300_ssd_iter_140000.caffemodel

For Using the face detection on an Camera (LiveFootage):
python face_detection_video.py --prototxt deploy.prototxt.txt --model res10_300x300_ssd_iter_140000.caffemodel


Models Used:

1. ** deploy.prototxt.txt **:

It is a configuration file used for deploying a neural network model with the Caffe deep learning framework. It defines the architecture of the model, specifying each layer's type, parameters, and connections. This file is crucial for setting up the network to perform predictions without involving any training processes. It includes information such as:
- The types of layers used (e.g., Convolution, ReLU, Pooling, etc.)
- Parameters for each layer like number of outputs, kernel size, stride, etc.
- The connections between layers or how data flows from one layer to another.

This type of file is typically used to implement the model directly on a production environment where inference is performed, after the model has been trained using a separate training configuration.

2. ** res10_300x300_ssd_iter_140000.caffemodel **:

It is a pre-trained model file used with the Caffe deep learning framework. This particular file contains the weights of a neural network model that has been trained for a specific task. The name suggests it's likely configured for an object detection task using a Single Shot MultiBox Detector (SSD) architecture, and it's specifically optimized for processing images at a resolution of 300x300 pixels.
Here’s what this file essentially includes and how it functions:
- Pre-trained Weights: It holds the learned weights and biases of the neural network from the training process on a dataset, likely for detecting objects within images.
- Usage in Object Detection: When combined with a corresponding configuration file (like a deploy.prototxt), this model can be used to detect objects in new images. It evaluates the presence and location of objects in an image by outputting a set of bounding boxes and associated confidence scores.
- Performance and Efficiency: The 'iter_140000' part of the filename indicates the number of iterations the network was trained, suggesting a mature model likely to yield reliable detection results.

This type of model is typically used in applications requiring real-time object detection, such as video surveillance, autonomous driving, or advanced photo editing software.
