 
<h1>🚗🔧🏭👷Track-Based Robot for Tool Retrieval and Return in Industrial Workspaces</h1>

<h2>Description</h2>
This project introduces an intelligent, app-controlled robot designed to streamline tool handling in industrial environments. The system combines autonomous navigation, IoT control, and smart mechanical interaction to reduce operator movement and improve workflow efficiency.

The robot follows a predefined track and is remotely activated via a mobile application. Upon receiving the command, it navigates to the tools table, where a smart robotic arm (mounted at the tool station) detects the robot's arrival. The arm selects and places the required tool onto the robot. Once the tool is secured, the robot automatically returns to the operator, delivering the tool safely and precisely.

Key Features:

🤖 Line-following autonomous robot

📲 Remote activation via mobile app

🖐️ Smart robotic arm for tool pickup

🧠 IoT-enabled coordination between devices

🔁 Bidirectional transport: operator ↔ tool station

⚙️ Ideal for workshop and factory environments

This project enhances efficiency, reduces downtime, and introduces smart automation into traditional manual workflows — a practical step toward Industry 4.0.
<br />


<h2>Components and Tools Used</h2>


<h3>Hardware Components:</h3>

<h4> - Microcontroller:</h4> Arduino Nano & ESP32

<h4> - Line Following Sensors:</h4> TCRT5000 (IR) sensors for track detection

<h4> - Motors:</h4> DC motors with motor driver module , L298N for robot movement

<h4> - Servo Motors SG-90 :</h4> To operate the smart robotic arm for tool pickup

<h4> - Smart Robotic Arm :</h4> 

<p align="center">
<br/>
<img src="https://www.gie.com.my/UploadFiles/robotics/kits/arcylic_robot_arm_1_large.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h4> - Wireless Module:</h4> Built-in Wi-Fi  on ESP32

<h4> - Power Supply:</h4> 11.1V, 3000mAh (Robot) / 7.4V, 3000mAh & Step-Down Module 5V (Arm)

<h4> - Chassis:</h4> Robot base frame with wheels

<h4> - Track:</h4> Predefined physical line 

<h4> - Sensors for Tool Detection & Robot Detection:</h4> FC-51 IR Sensor

<h4> - Software and Utilities:</h4>

<h5> - Arduino IDE:</h5> For programming the microcontroller firmware

<h5> - RemoteXY:</h5> For creating the mobile app interface and managing wireless communication

<h5> - Libraries:</h5>

Servo motor control libraries ( Servo.h)

Enables Wi-Fi connectivity for the ESP32 (WiFi.h)

RemoteXY library for UI communication(RemoteXY.h)

Mobile App Platform: Android/iOS via RemoteXY app

<h2>Robot-Program walk-through:</h2>

<p align="center">
Libraries Declaration <br/>
<img src="https://i.imgur.com/dEFCtqG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
RemoteXY settings  <br/>
<img src="https://i.imgur.com/YeBJQEL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Pins & Variables Declaration : <br/>
<img src="https://i.imgur.com/PZIu9xg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
void setup()  <br/>
<img src="https://i.imgur.com/LpcGoYk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Robot Movement Algorithms with Obstacle Avoidance:  <br/>
<img src="https://i.imgur.com/vO9yD9V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br/>
<img src="https://i.imgur.com/N8Fb9LO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Handles incoming UI commands from the RemoteXY app interface & Start Command Trigger from App &  Reset Button State  <br/>
  <br/>
<img src="https://i.imgur.com/Di0R06x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Line Following and Obstacle Detection  <br/>
<img src="https://i.imgur.com/xt4UNQb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Line Following and Obstacle Detection  <br/>
<img src="https://i.imgur.com/C5lKYmj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Stop Robot if Not Running  <br/>
<img src="https://i.imgur.com/FcOUGwc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  

<h2>Arm-Program walk-through:</h2>
<p align="center">
🔧 Servo and Sensor Setup <br/>
<img src="https://i.imgur.com/OKzV7YU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
🚀 Initialization <br/>
<img src="https://i.imgur.com/e1oaDBs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
🔁 Main Loop - Object Detection and Response <br/>
<img src="https://i.imgur.com/ENcLSZO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Arm-Wiring-Diagram:</h2>
<p align="center">
 <br/>
<img src="https://i.imgur.com/zVgTVbZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h2>Robot-Wiring-Diagram:</h2>
<p align="center">
 <br/>
<img src="https://i.imgur.com/FDXksz2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
