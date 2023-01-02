# fusion
Fusion project is attempted to carry out LIDAR and Camera Fusion in autonomous vehicle.

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


