# Traffic-Signs-Classifier-using-Deep-Learning-with-Python-Keras
<p>Traffic sign classification is the process of automatically recognizing traffic signs along the road, including speed limit signs, yield signs, merge signs, etc. Being able to automatically recognize traffic signs enables us to build “smarter cars”. <br>

Self-driving cars need traffic sign recognition in order to properly parse and understand the roadway. Similarly, “driver alert” systems inside cars need to understand the roadway around them to help aid and protect drivers. <br>

Traffic sign recognition is just one of the problems that computer vision and deep learning can solve. </p><br>
<h3>OBJECTIVES</h3>
1.	Understand the theory and intuition behind Deep Learning and Convolutional Neural Networks (CNNs). <br>
2.	Import Key python libraries, dataset and perform image visualization. <br>
3.	Perform image normalization and convert images from color-scaled to gray-scaled. <br>
4.	Build a Convolutional Neural Network using Keras with Tensorflow 2.0 as a back-end.<br>
5.	Compile and fit Deep Convolutional Neural Network model to training data.<br>
6.	Assess the performance of trained Convolutional Neural Network model and ensure its generalization using various KPIs.<br>

<h3>DATASET</h3>
The dataset we’ll be using to train our own custom traffic sign classifier is the German Traffic Sign Recognition Benchmark (GTSRB). <br>

The GTSRB dataset consists of 43 traffic sign classes and nearly 50,000 images.<br>

A sample of the dataset can be seen in Figure 2 above — notice how the traffic signs have been pre-cropped for us, implying that the dataset annotators/creators have manually labeled the signs in the images and extracted the traffic sign Region of Interest (ROI) for us, thereby simplifying the project. <br>

In the real-world, traffic sign recognition is a two-stage process: <br>

<b>Localization</b>: Detect and localize where in an input image/frame a traffic sign is. <br>
<b>Recognition</b>: Take the localized ROI and actually recognize and classify the traffic sign.

<h3>Challenges with the GTSRB dataset</h3>
There are a number of challenges in the GTSRB dataset, the first being that images are low resolution, and worse, have poor contrast. These images are pixelated, and in some cases, it’s extremely challenging, if not impossible, for the human eye and brain to recognize the sign.<br>

The second challenge with the dataset is handling class skew:<br>

The top class (Speed limit 50km/h) has over 2,000 examples while the least represented class (Speed limit 20km/h) has under 200 examples — that’s an order of magnitude difference!<br>

In order to successfully train an accurate traffic sign classifier we’ll need to devise an experiment that can:<br>

1. Preprocess our input images to improve contrast.<br>
2. Account for class label skew.<br>
