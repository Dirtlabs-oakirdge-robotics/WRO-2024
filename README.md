Mobility Management
Importance of Mobility:
Ensures smooth movement through obstacles and precise parking.
Motor Choice: Johnson 500 RPM DC Geared Motor
Speed & Torque: Balances speed with torque for control and sharp turns.
Compatibility: Works well with common motor drivers, Raspberry Pi 5, and Arduino Uno.
Efficiency: Geared motor simplifies gear ratio calculations, reducing computational load.
Potential Alternative: A BLDC motor could offer better performance but is more complex and costly.
Chassis and Motor Implementation
Custom 3D Printed Chassis:

Rapid Prototyping: Allows fast iteration and design adjustments for WRO Future Engineers.
Part Freedom: No restrictions from pre-built chassis designs, allowing part customization.
Space Efficiency: Optimizes use of space to meet WRO size regulations.
Software Used: Fusion 360 was chosen for its collaborative features, ease of use, and free access for students.
Generative Design: Fusion 360's design tools allow more reliable and efficient iterations.
Printing Setup: Used PLA filament on Bambu Lab P1S and Anycubic Kobra 2 Neo for high print quality.
Integration of Motor and Chassis:

Transmission System: Per-gear ratio of 0.6:1 for smoother power transmission.
Custom Motor Mounts: Printed mounts for the Johnson Motor and Intel RealSense D455 sensor.
Steering of Vehicle
Servo Motor: MG996R
Precise Control: Ideal for fine steering adjustments.
Easy Control: Uses PWM signals, compatible with Raspberry Pi 5 and Arduino Uno.
Space Efficiency: Meets WRO size/weight constraints for Future Engineers category.
Power Efficiency: Handles complex steering maneuvers with minimal power consumption.
Power and Sense Management
Battery Setup:
Dual Battery System:
Power Sources:
10,000 mAh battery for Intel RealSense D455 and Raspberry Pi 5.
2200 mAh LiPo battery for motor and Arduino.
Load Distribution: Each battery powers specific components, enhancing efficiency.
Voltage Needs: Different power needs for motor (fluctuating) and computer/sensors (stable).
Alternative: Higher-rated single battery could simplify the setup but increase cost.
Sensor: Intel RealSense D455
Why D455?
6m Depth Range: Covers entire obstacle course.
87-degree FOV: Wide field of view to minimize blind spots, crucial for parking challenges.
Integrated IMU: Provides accelerometer and gyroscope data for more precise vehicle motion.
Power Efficiency: Consumes only 1.5-2.5 watts while processing depth and RGB data.
Alternative Sensor: Intel RealSense L515 offers longer range but lower frame rate.
Obstacle Management
Handling Obstacles:
Software Used:
OpenCV: Processes images from Intel RealSense D455 to detect and classify obstacles based on color.
TensorFlow: Uses deep learning models on Raspberry Pi 5 to identify and avoid obstacles (e.g., traffic signs).
Community Support: Both platforms have strong documentation and large communities for troubleshooting.
Real-time Feedback: RealSense depth and RGB data provide real-time input to Raspberry Pi algorithms, optimizing decision-making.
Obstacle Course Strategy
Path Planning:
Depth Information: Real-time depth data enables accurate obstacle avoidance.
TensorFlow Training: Models predict optimal paths using sensor inputs, guiding the vehicle efficiently around obstacles.
Algorithm Hierarchy:
Input Flow: Intel RealSense data → Raspberry Pi 5 (via RealSense SDK, TensorFlow, OpenCV) → Arduino Uno → Motors.
Output: Motors adjust vehicle movement based on processed input from sensors and deep learning algorithms.
