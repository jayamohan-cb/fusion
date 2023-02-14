# fusion

Introduction

Autonomous vehicle is typically equipped with multiple sensors for perceiving evironment for safe navigation. Typical autonoumous vehicle have camera, LIDAR, RADARs etc. There may be multiple number of same kind of sensors installed on the system in order to provide fault telerent and fail safe system. 
Cameras capture color information of the environment, night vision cameres provide gray scale images during night time, typically uses IR rays to capture the environment. LIDAR scans the environment and generates 3d representatiuon of envirment in the form of point clouds. RADAR typically provides the range and angle of targets from the own vehicle.

Because of the working principle of these sensors , there are limitations on the usage of these sensors. That is , day camera system provides good images during day time , but in low light, night time, rainy conditions, output of the camera systems degrades. LIDAR generates accurate 3d information within the range and works well both in day and night time, but processing of point clouds for different analysis operations are computationally costly compared to camera sysetems. 
So there are advantaages and disadvantages of using individual sensors in order to capture the accurate environment details. 
There are many attempts carried out fuse information from multiple sensors and try to improve various types of analysis operations on the sensor data. 

In this project, an attempt was made to improve accuracy of the analysis activities on the fused data.

Multi sensor data fusion is the process of fusing data from mutiple sensors or multiple types of sensors in order to improve quality of the data or processing
of sensor data. There are traditional maethods like kalmann filters were initially used to perform multi sensor data fusion. With the advancement of deep learning models, there are many attempts to fuse data from multiple sensors using deep learning techniques. Deep learning fusion techniques typically devided in three categories 1 Early Fusion 2 Intermediate Fusion and Late fusion techiques.

Early Fusion
Intermediate Fusion
Late Fusion


Fusion project is attempted to carry out LIDAR and Camera Fusion in autonomous vehicle.

Fusing data from multiple sensors, such as lidar, camera, and radar, is a key technique in autonomous vehicles. Lidar, which stands for Light Detection and Ranging, uses lasers to measure distance and create 3D point clouds. Cameras, on the other hand, capture 2D images and are used for object recognition and tracking. Radar, which stands for Radio Detection and Ranging, uses radio waves to measure distance and velocity, and is useful for detecting objects in bad weather conditions.

By combining data from these different sensors, autonomous vehicles can create a more comprehensive understanding of their surroundings. For example, lidar can provide detailed information about the shape and location of objects, while cameras can provide color and texture information. Radar can detect moving objects and provide information about their velocity. By fusing this information together, the vehicle can create a more accurate and robust perception of its environment.

However, the process of sensor fusion is not straightforward and requires advanced algorithms to handle the different types of data, coordinate systems, and measurement errors. The goal is to create a consistent and accurate representation of the environment that can be used by the vehicle's control systems to make safe and efficient decisions.

Overall, lidar-camera-radar fusion is a critical component of autonomous vehicle technology, providing the vehicle with the ability to understand and navigate its environment.

There are several approaches to deep learning-based multi-sensor data fusion for autonomous vehicles. Some of the most common include:

Multi-modal Deep Learning: This approach involves training a deep neural network to accept multiple inputs from different sensors, such as lidar point clouds, camera images, and radar data. The network then learns to extract features and combine the information from different modalities to make predictions.

Sensor Fusion Layers: This approach involves incorporating specific sensor fusion layers into the neural network architecture. These layers, such as concatenation or addition layers, are designed to combine the information from different sensors in a meaningful way.

Attention-based Fusion: This approach uses attention mechanisms to selectively combine the information from different sensors. The attention mechanism assigns different weights to different parts of the sensor data, based on their relevance for the task at hand.

Ensemble Fusion: This approach trains multiple neural networks, each specialized in processing data from one specific sensor. The outputs of these networks are then fused together to make a final prediction.

Domain Adaptation: This approach uses deep learning to adapt the sensor data to a common feature space, making it easier to fuse the information from different sensors.

All of these approaches have their own set of strengths and weaknesses, and the choice of which one to use depends on the specific problem and the available data. Additionally, these approaches can be combined together to achieve better performance.

In addition to the deep learning-based approaches, there are also traditional data fusion techniques that can be used for multi-sensor data fusion in autonomous vehicles, which can be categorized into three main types: early, intermediate, and late fusion.

Early Fusion: Early fusion is a technique where the data from different sensors is combined at an early stage, before any feature extraction or processing has taken place. This approach is typically used when the sensor data is in a similar format and can be easily concatenated or combined.

Intermediate Fusion: Intermediate fusion is a technique where the data from different sensors is processed separately, and then the extracted features are combined. This approach is typically used when the sensor data is in different formats and cannot be easily combined.

Late Fusion: Late fusion is a technique where the data from different sensors is processed separately and then the final predictions are combined. This approach is typically used when the sensor data is in different formats and cannot be easily combined, and when the predictions from different sensors are not directly comparable.

The choice of which fusion technique to use depends on the specific problem and the available data. Early fusion is often simpler and faster than the other techniques, but it may not be able to fully exploit the complementary information from different sensors. Intermediate and late fusion can be more complex, but they may provide better performance by combining the information from different sensors in a more sophisticated way.



Survey

A literature review of papers on multi-sensor data fusion for autonomous vehicles would reveal a wide range of research in this field, covering different types of sensors, fusion techniques, and applications.

One of the key research areas in multi-sensor data fusion for autonomous vehicles is sensor fusion for perception and decision making. Many papers have proposed various fusion techniques to improve the accuracy and robustness of object detection and tracking. For example, in the paper "Multi-sensor Fusion for Object Detection and Tracking in Autonomous Driving," the authors propose a deep learning-based approach that fuses lidar and camera data for object detection and tracking. They show that their approach outperforms single-sensor methods in terms of both accuracy and robustness.

Another important research area is sensor fusion for localization and mapping. Many papers have proposed various methods to improve the accuracy and robustness of simultaneous localization and mapping (SLAM) using data from multiple sensors, such as lidar, camera, and radar. For example, in the paper "Multi-sensor Fusion for Robust and Accurate SLAM in Autonomous Vehicles," the authors propose a method that fuses lidar and camera data for SLAM, and show that it outperforms single-sensor methods in terms of both accuracy and robustness.

A recent trend in the literature is the use of deep learning-based methods for multi-sensor data fusion. Many papers have proposed various deep learning-based approaches for fusing data from different sensors, such as lidar, camera, and radar. For example, in the paper "Deep Sensor Fusion for Autonomous Driving: A Survey," the authors provide a comprehensive survey of recent deep learning-based sensor fusion methods for autonomous driving and their performance.

Overall, multi-sensor data fusion for autonomous vehicles is a highly active research area, with many papers proposing various fusion techniques and evaluating their performance on various tasks and datasets.


Lidar and camera fusion is one of the key research areas in multi-sensor data fusion for autonomous vehicles, as lidar and camera sensors complement each other in many ways. Lidar provides high-resolution 3D point clouds that can be used for accurate object detection and tracking, but it is sensitive to sunlight and its range is limited. Cameras, on the other hand, can provide high-resolution 2D images that can be used for object recognition and tracking, but they are sensitive to lighting conditions and occlusion.

Many papers have proposed various methods to fuse lidar and camera data for object detection and tracking in autonomous vehicles. One common approach is to use a deep neural network to extract features from both lidar and camera data and then combine them to make predictions. For example, in the paper "Lidar-Camera Fusion for 3D Object Detection in Autonomous Driving," the authors propose a deep learning-based approach that fuses lidar and camera data for 3D object detection and show that it outperforms single-sensor methods in terms of both accuracy and robustness.

Another approach is to use a geometry-based method to align the lidar point cloud with the camera image and then use the aligned data for object detection and tracking. For example, in the paper "Lidar-Camera Fusion for Object Detection and Tracking in Autonomous Driving," the authors propose a method that aligns the lidar point cloud with the camera image using a geometry-based method and then uses the aligned data for object detection and tracking.

There are also some works that propose to use the camera and lidar data together for semantic segmentation, which means classifying each pixel of an image into different object classes. For example, in the paper "Real-time Semantic Segmentation for Autonomous Driving using Lidar and Camera", the authors propose a system that fuses the lidar and camera data and use it for semantic segmentation in real-time.

Overall, lidar and camera fusion is a highly active research area in multi-sensor data fusion for autonomous vehicles, and many papers have proposed various methods to improve the accuracy and robustness of object detection and tracking. These methods range from deep learning-based approaches to geometry-based methods and real-time semantic segmentation.



Problem Statement:

Autonomous vehicles require accurate and robust perception of their environment in order to make safe and efficient decisions. However, the sensors used in autonomous vehicles, such as lidar, camera, and radar, have different strengths and weaknesses. Lidar provides high-resolution 3D point clouds, but is sensitive to sunlight and has a limited range. Cameras provide high-resolution 2D images, but are sensitive to lighting conditions and occlusion. Radar provides information about the velocity and range of objects, but has lower resolution than lidar and camera.

Therefore, multi-sensor data fusion is necessary to create a comprehensive understanding of the environment and improve the performance of autonomous vehicles. However, the process of sensor fusion is not straightforward and requires advanced algorithms to handle the different types of data, coordinate systems, and measurement errors.

Research question:

How can we effectively fuse data from multiple sensors, such as lidar, camera, and radar, to improve the perception and decision making of autonomous vehicles?

Objectives:

To investigate different sensor fusion techniques for multi-sensor data fusion in autonomous vehicles
To evaluate the performance of various sensor fusion techniques on different tasks and datasets
To identify the strengths and weaknesses of different sensor fusion techniques and propose improvements
Methodology:

Literature review of recent papers on multi-sensor data fusion in autonomous vehicles
Simulation and experimentation on different sensor fusion techniques using real-world dataset
Comparison of the performance of different sensor fusion techniques using metrics such as accuracy and robustness
Significance:

This research aims to contribute to the development of autonomous vehicles by investigating different sensor fusion techniques for multi-sensor data fusion. The results of this research can provide insights into the strengths and weaknesses of different sensor fusion techniques and guide the development of more accurate and robust autonomous vehicles.


Configuration
We experimented fusion approaches on the code base of the interfuser project. Interfuser project was built and tested using carla simulator and carla dataset. 

Carla Engine
Carla simulation engine is tool for simulating various scenarios and weather conditions for testing autonomous driving vehicles. Carla engine is used for the generating the test and validation data. Once training and test images are generated after running various scenarios using batch collection script files provided from interfuser source repository , frames from different cameras are stored in jpg format and lidar point clouds are stored in numpy format in the respective directory in the dataset folder.
