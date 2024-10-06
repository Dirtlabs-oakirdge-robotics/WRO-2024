# WRO-2024


# Content
t-photos contains 2 photos of the team
v-photos contains 6 photos of the vehicle
video contains the video.md file
schemes contains a schematic diagram
src contains code of control software for all components
models is for the files for models used by 3D printers

WRO Engineering Documentation: 
Mobility Management 
Why is movement management important? 
At the center of any performance robotics-based device is the way in which it manages its own mobility and movement to make sure that the vehicle is able to maintain its pace through obstacles and maneuver itself into tight parking spaces. 
What motor is being used to power the mobility of our vehicle? 
https://www.amazon.in/Robodo-Electronics-Johnson-Geared-Robotics/dp/B00N4O7GU6/ref=sr_1_1?dib=eyJ2IjoiMSJ9.54jvCgJbNCIySEug8rbzD2XTkBaLnxZE6AVz8ScrW7G-NsCDuHGHBm1v6tLAmHECQjVT_2qbFieDrjN-qnDCsFtOfkt1va6oegGmF84iTmvKSUt9mPi-g_iBlYk1AcRHwRMkvG4_vvR_nbVD4S6ik4DflAKno9mIwi6iWaIX7N4KF9OIH8eUn_fU28Lz2P6JB4LPI7UqmYkqSviW5gdSy1_Sw6ee5bZw3rbWE2H98Kgs9Iu96SSj0FAI5uzsDTDZAuA6bx6O1yUu6Za_WhEdcVdv4nI-MV-4CALRgj6oovg.8ebr1T7pzYHR3zQOnUg3vbGdP7-3FMe_OPzPmBFckGo&dib_tag=se&keywords=johnson+geared+motor&nsdOptOutParam=true&qid=1727958316&sr=8-1 
For this vehicle, we have opted for the use of a Johnson 500 RPM DC Geared Motor, and there are a few reasons why we believe that this motor is a good fit for this project 
	•	The 500 RPM Geared Motor has a good balance between speed and torque, which in the case of this self-driving artificially intelligent motor vehicle, this balance is important to ensure that the speed of the vehicle is moderate in which it remains controllable while waiting on the single-board computer and microcontrollers to make a decision on where to move next, however the motor does provide enough torque for the motor to be able to handle sharper turns around objects to compensate for a theoretical delay in output from the computers. 
 
	•	The Johnson Motor is also Compatible with many common robotics motor drivers, meaning that it will be easier for the motor to interface with our SBC and microcontroller of choice for this vehicle, which are the Raspberry Pi 5 and Arduino Uno. 
 
	•	Also being geared, the Johnson Motor does not require as much calculation for the gear ratio, meaning that it will be easier for calculation, meaning that the AI algorithm on the SBC will not have to work as hard, saving both energy and calculation time. 
 
	•	However, I believe that if implemented correctly, a Brushless Direct Current (BLDC) motor may be a better fit for this kind of vehicle, however due to the complexity of control and price constraints, we have decided to go with the geared motor. 
 


 
Chassis and Implementation of Motor. 
However, there is no point of having the right motor for the job if the motor itself is not implemented in the right way, hence why we have decided after trying many different options, that the best one for our use case was to use a custom-made 3D printed chassis, and there are also multiple reasons that we have decided to make this decision instead of the use of other types of carriages for the vehicle: 
	•	3D Printed chassis such as the one we have opted for in the case of this application is comparatively better considering other options due to the fact that it allows for rapid prototyping and iteration from the designs that we have already made to find a perfect version for our specific use case in the case of World Robot Olympiad Future Engineers. 
 
	•	Also, with the use of a custom 3D printed chassis we can have more freedom in the selection of other parts to be used due to the fact that we do not have to follow any specific instruction set related to other types of chassis, so we can pick exact parts we need for the specifications 
 
	•	A custom 3D printed chassis also allows for more efficient use of space in order to make sure that there is more space for the parts to fit into the size limitations of the World Robot Olympiad Specifications mentioned in the general rules for the Future Engineers category. 
 
	•	For the software in terms of the chassis and custom 3D printed parts, we have decided to use Fusion 360 to make these, and there are many reasons for this including the fact that fusion 360 allows for easy collaboration, which is crucial, it is important to have everyone that is a part of the team work on the CAD files for the project  
 
	•	Another reason for this is that fusion 360 has a user-friendly UI design especially in comparison to other high end modelling software, allowing for ease of use and a smaller learning curve than other high end CAD software. 
 
	•	One more reason is that Fusion 360 has generative design features that allow users to iterate upon their own design and creativity and make more efficient and reliable designs that allow for better working robots. 
 
	•	The final and most important reason that we decided to use fusion 360 for the creation of our vehicle is that fusion 360 is available for free to students, which means that it is the most affordable and powerful option for World Robotics Olympiad India 2024. 
 
	•	However, it can be noted that using higher quality resin based 3D print filament can lead to more lightweight, strong, and higher quality prints, although our team refrained from this due to cost restraints.	  
Specifications of Chassis: 
For this chassis, we decided to use a PLA material filament which was extruded through the use of either a Bambu Lab P1S and Anycubic Kobra 2 Neo 3D printers to ensure maximum print quality. 
For CAD files, you can simply refer to the DIRT-LABS GitHub Repo for World Robot Olympiad Future Engineers in order to 3D print your own version. 


 
Integration of Motor and Chassis for Mobility Management 
For the integration of the motor and chassis of the vehicle, decided to a per-gear transmissional ratio conversion system in order to transfer power more smoothly and linearly at a ratio of 0.6:1. 
This also allows for a reliable and consistent design for a more streamlined experience, so we don’t face as many problems during the Future Engineers exhibition. 
We also used custom motor holders as a part of the chassis that we 3D printed, again for your reference the CAD files can be found in the WRO Future Engineers GitHub for DIRT-LABS, as well as the wheel mounts, we used mounts for sensors in order to fit our choice of sensor, which is the Intel RealSense D455 Depth Camera. 
Steering of Vehicle 
For the steering of the vehicle, we have decided to use the MG996R servo motor, and this also has many reasons for which our team decided to use it. 
https://www.amazon.in/Robodo-Electronics-MG995-TowerPro-Servo/dp/B00MTH0RMI/ref=sr_1_5?crid=15Q0EGJCEIQED&dib=eyJ2IjoiMSJ9.XfP7z4NvdaAdS8bWPp6r8Sj4X8ygE3-F5ZDZkZ-sxUcmdgV-N22797zEeJbvsgCXUSQSSaU9zdsAfXVBkO4USlu2xSZbS8wHfX96jAvUdQNR31cnBzRJs-9zMV_ALTGqTwG1wxrmNY_1zE3DyvH0inzS1fRiE0wHB7Fat6vpeuRsv6URLIDH2GP9nxwpym8-_LbRGVCT-bQhXzPdT0K-b-BQfwgvfiQfD9yOYYGhWhMjst4d8BRW0FzTyMykMBKOVvt0V4LZrHsE2b5is_2PP_jaNfyi4Lix6KpMeVp6oyo.Xn-TsUF_MNrwDN8M3aQK9kyYgALzm7aaE7RUgWPkXnc&dib_tag=se&keywords=mg995+servo&qid=1727984925&sprefix=mg995+servo%2Caps%2C187&sr=8-5 
	•	Servo motors are used in the steering of these type of robotic vehicles regularly due to the fact that servo motors provide more precise control over the steering of the vehicle, even while following complex data given to it from the sensor. 
 
	•	Servo Motors also use PWM (Pulse Width Modulation) signals, which are easily generated with the use of most microcontrollers, such as the Arduino and Raspberry Pi devices used in our vehicle, which reduces the complexity of controlling the robot. 
 
	•	Servo Motors are also space efficient, which is important for this use case because of the rules around the size and weight limitations of the Future Engineers general rules. 
 
 
In conclusion, for the mobility management and the chassis of the car, we decided to use a 500 RPM DC Motor, a custom 3D Printed chassis, and a MG995 Servo motor, and the most important reason why we decided to use these parts are cost effectiveness and the way in which the work together efficiently to make the vehicle maneuver itself more swiftly around obstacles, and fit into parking spaces, we also used fusion 360 to make the chassis for the car due to its ease of use and availability to students. 
 
Power and Sense Management 
Battery Setup 
For the battery setup we decided to use a 10,000 milliamp-hour battery bank for the Intel RealSense D455 Depth Camera and the Raspberry Pi 5, and a 2200 milliamp-hour Lithium Polymer Battery for the motor and movement of the vehicle, and there are multiple reasons why we decided to go with this battery setup. 
	•	The first one is that the use of a dual battery setup reduces the load on each battery, this is due to the fact that each battery only needs to power a specific set of components of the vehicle instead, meaning that thermals will be more under control and the battery can power the vehicle for longer. 
 
	•	Another important factor is that the sensors and computers require different voltages compared to the motors, due to it being a completely different use case, hence using two separate batteries allows each subsystem of the vehicle. 
 
	•	One more reason that we have chosen this specific dual battery system is that the motor has more fluctuating power needs, which can be provided more consistently by the LiPo battery, whereas something like an Arduino Uno R3, Raspberry Pi 5, or Intel RealSense D455 require more constant, stable power, hence why it makes sense to separate the power supply for these parts. 
	•	However, if you plan on doing this yourself, you can also opt for a higher power rated battery in order for a similar power setup, while saving weight and some complexity, however it may be more expensive and harder to diagnose power issues. 
 


 
 
 
 
 
Sensor Used: 
For this vehicle, we have decided to go with the Intel RealSense D455 as our sensor, which is a depth camera from Intel, that combines a depth sensor, inertial measurement unit (IMU) and simultaneous localization and mapping (SLAM). 
https://www.amazon.in/Intel-RealSense-D455-Webcam-3-1-1280/dp/B08KJCRCGG/ref=sr_1_2?crid=3T81ADRY4AASG&dib=eyJ2IjoiMSJ9.ik7VVLnGPhgp0ogF6KuU3tOKFnEs-x38fWuSIO0l08zqf3xAb6pvXG8yiJEwM3iRR_YM2v2ZpAOCGQGL6JbP6lvsGFv4t5usFCbICh-gCH354O_F2JiPRpwca8f5VErp5AwDHDWJqIiYdLSJg7kzEnWANKeHkr0mO1eIhJ7CllbQLBRjzQ2AqJbIwVLev60GmeCYyl9ZH_2I3ffBDti5c5682PShnqeZrhcrfXR3VRQ.GcxEiNB_ntZOE5NmAonGhIV4ygBY5eojJExRPDDTVUI&dib_tag=se&keywords=intel+realsense+d455&nsdOptOutParam=true&qid=1727993668&sprefix=intel+realsense+d45%2Caps%2C190&sr=8-2 
	•	The Intel RealSense D455 Depth Camera has a 6-meter-long radius for accurate detection of depth, making it so that it has more than enough range to cover the entire Future Engineers obstacle course, and the accuracy of the depth camera allows it to easily and rapidly detect nearby objects and provide feedback to the algorithms running on the Raspberry Pi 5 using TensorFlow. 
 
	•	The RealSense also has a field of view of around 87 degrees which allows for it to have a wider perspective and fewer blind spots, which is useful especially in the use case scenario of something like the parking challenge, where field of view is crucial for making sure that the vehicle has sight of the parking space at all times so that the algorithm can properly guide the car to the parking spot.   
	•	Another reason that the Intel RealSense is a good fit for this vehicle is the fact that the Intel RealSense D455 has an integrated IMU (Inertial Measurement Unit), which is important because it supplements the sensor data with accelerometer and gyroscope data from the Inertial Measurement Unit for more accurate data on the motion of the vehicle. 
 
However, if you are implementing this robot, I would suggest that you also look at the Intel RealSense L515 along with the Intel RealSense D455 that we are using due to its longer range and smaller footprint, however the D455 does have a higher framerate. 
 


 
 
 
The Intel RealSense draws only 1.5-2.5 Watts of power consistency while using both the Depth Sensors and RGB data, which is important to maintain consistently low power usage from the battery to ensure that the Single Board Computer, which in this case is the Raspberry Pi 5, and to ensure that the vehicle has adequate runtime on battery. 
 
(Insert Picture of Wiring Diagram) 
 
In conclusion, for power and sense management of this vehicle, we have decided to use a 10,000 milliamp-hour lithium-ion battery to power the single-board computer and the sensors, and a 2200 milliamp-hour battery to power the motor and microcontroller, due to differences in the nature and applications of these different devices, and the way in which they are utilized, I believe that the dual battery solution is optimal for this application, as it provides the optimal voltage for both the single board computer and sensor, while also providing optimal voltage for the microcontroller through the use of separate batteries. 
For sense, we decided to go with an Intel RealSense D455 Depth Camera for the most optimal sense experience, as the RealSense combines an RGB Camera, a Depth Camera, an Inertial Measurement Unit, and even Simultaneous Localization and Mapping all in one small package that can be easily mounted for such robotics applications. 
Obstacle Management 
How we plan on tackling obstacles with our vehicle 
One of the main categories of the World Robot Olympiad Future Engineers category is the obstacle round, and there are multiple ways to calculate a route in which the vehicle not only avoids the obstacles, but also goes around them in the right direction based on the color of the obstacles. 
We implemented this using multiple different software and hardware solutions, one of which being OpenCV, if you are unfamiliar with OpenCV, it basically provides an array of tools that can be used to process images directly from the RGB camera of the Intel RealSense, using this tool, the robot can easily differentiate different objects in order to maneuver around them for a faster and more efficient lap. 
The vehicle is also designed to use depth information from the Intel RealSense D455 in real time, hence providing the robot the information to accurately predict the distance from the obstacles, allowing for faster and more reliable performance in an obstacle course such as the one in the World Robot Olympiad Future Engineers Category. 
Another piece of software that we are making use of is TensorFlow, which is an application that can be used to run deep learning models on the Raspberry Pi 5, which lets the single board computer classify objects around it, meaning that the Pi can be trained to detect certain objects such as the World robot Olympiad Future Engineers traffic signs. 
With the combination of the data from the Intel RealSense and the algorithms in TensorFlow, the vehicle can differentiate between the different objects and obstacles present in the environment near the vehicle. 
TensorFlow models can also be trained in order to predict the most optimal paths based on inputs given real time by the onboard sensors, which can allow the artificially intelligent vehicle to make more informed decisions about the way in which it operates. 
OpenCV and TensorFlow also have large community support and are very well documented, so that most common issues with any of these platforms used for deep learning can be resolved more simply compared to any other artificial intelligence training platform. 
If you are implementing this code, you can find all the code in the Google Drive or the GitHub repository for DIRT-LABS WRO 2024, both linked below. 
https://drive.google.com/drive/u/2/folders/1wpYpHlhpfxlnaNbKCSh7umogDouVo02Q?dmr=1&ec=wgc-drive-hero-goto&q=sharedwith:public%20parent:1wpYpHlhpfxlnaNbKCSh7umogDouVo02Q 
(Insert GitHub Repo Link) 


 
 
In the above flowchart, you can observe the hierarchy of the instruction set being used for operating the vehicle, in this hierarchy, you can see that the raw data from the Intel RealSense depth camera is being sent to the Raspberry Pi 5 for processing, which is applied to the RealSense SDK and a custom set of algorithms, and then processed by TensorFlow and OpenCV using the method demonstrated in above paragraphs. After which the processed output is sent to the Arduino Uno, and then the Uno relays it to the motors, leading to the car moving in a way that corresponds to the obstacles in its path and environment, and where it needs to go next. 
In conclusion, we have used advanced algorithms and machine learning platforms such as TensorFlow and OpenCV in order to guide the vehicle through the obstacles placed on the World Robot Olympiad Future Engineers map, these programs are powered by the Raspberry Pi 5 and fed by the Intel RealSense D455. 
Pictures – Team and Vehicle 
 


     
