# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
 Initiate the MobileRobot
Step2:

Connect your PC with the MobileRobot through Wi-Fi. 

Step3:

 Open batter_level.py file and check the battery.

Step4:

 Open the other Python files and Program the movements of the robot using python. 

Step5:

Execute the python program and record the movements.

## Program
```
#Editing mobilerobot-openloopcontrol
#Developed by : Allen Joveth P
#Regisiter number : 23009582

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0.3, y=0, z=80, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=1.02, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=-1.45, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-118, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_chassis.move(x=-1.55, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-48, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=1.4, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=85, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here

![mobile_robotics](https://github.com/allenjoveth/mobilerobot-openloopcontrol/assets/139422287/4d0e6807-0067-4b65-b3cb-4eb05c18eb75)

![mobile_rob](https://github.com/allenjoveth/mobilerobot-openloopcontrol/assets/139422287/e3c2aa74-3e4a-4779-b5b9-d95d3a7b7ca2)

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://youtube.com/shorts/oav2pgUNh0c?si=W-7EuS9_aH3OUtFs

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
