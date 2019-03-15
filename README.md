# Follow-Me #
#### Robotics Software Engineering ####
#### Term 1 ####
#### Project 4 ####

_Concepts/Skills Learned:_
  * Proportional Integral Derivative (PID) controllers: for SISO and MIMO systems
  * Classification Neural Networks (logistic classifers)
  * Deep Neural Networks: convolutional, fully convolutional
  * Semantic Segmentation
  * TensorFlow
  * Keras
  * Amazon Web Services (AWS): Cloud GPU usage

---

_Project Description:_

The Follow-Me project involved the integration of multiple concepts into a single task. To begin, the fundamentals of a PID controller were discussed, detailing why each of the the three components is beneficial to errors within closed-loop systems (both simple and complex). 

Next, the fundamentals of Quadrotor kinematics and dynamics were discussed, followed by the implementation of PID controllers in the accurate control of simple quadrotors.

Continuing, a deep dive into neural networks was undertaken. The basics of neural networks were first discussed, followed by a natural progression to the development of deep neural networks, convolutional networks, and, finally, fully convolutional networks. These concepts were developed and tested using TensorFlow, with the addition of its Keras application for simpler neural network modeling. 

For this project, a virtual quadrotor was modeled in a Unity environment (mimicking a city). Within this city, a mobile population of pedestrians could be initialized, along with a slighlty different person of interest. The quadrotor, outfitted with an RGB camera, would be tasked with flying along pre-designated routes, collecting thousands of images for neural network training. These images would be separated into a large training set, smaller validation set, and a miniscule test set. Within the training and validation sets, each image was partnered with appropriate masks (each color channel designated for a specific classification: red - background, green - person, but not one of interest, blue - person of interest). This was done to not only allow for the training of a classification network, but also perform semantic segmentation (allowing each pixel in a provided image to be assigned one of the three provided color channels).

Using a Jupyter notebook, a fully convolutional neural network was created, containing encoder and decoder components. This network was trained with aforementioned data, with the final task being the tuning of hyperparameters for at least 40% successful IoU (Input over Output) score.
     
   For a full report of how this was accomplished, see the included write-up: 
   
   [Follow-Me Write-Up](https://github.com/akompaniyets/Follow-Me-Deep-Learning/blob/master/Follow-Me%20Write-Up.pdf)
