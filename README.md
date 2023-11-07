# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:
Initiate the MobileRobot.

Step2:
Connect your PC with the MobileRobot.

Step3:
Program the movements of the robot using python code

Step4:
Execute the python program.

## Program
python
```
from robomaster import robot
import time
from robomaster import camera

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x=0.8,y=0,z=62,xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=225,b=0,effect="on")

    ep_chassis.move(x=0.9,y=0,z=0,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=225,effect="on")

    ep_chassis.move(x=0,y=-0.8,z=65,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0,y=0,z=223,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=102,b=153,effect="on")

    ep_chassis.move(x=-1,y=0,z=0,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=-1,y=-0.9,z=0,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=157,g=114,b=176,effect="on")
   
    ep_chassis.move(x=0,y=0,z=107,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=0,y=-1.5,z=0,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")

    ep_chassis.move(x=-2.1,y=0,z=261,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=204,b=0,effect="on")

    ep_chassis.move(x=0.4,y=0,z=0,xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=120,effect="on")

    
    time.sleep(4)




    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![WhatsApp Image 2023-11-07 at 08 30 13_1d76fa26](https://github.com/Sudharsanram/mobilerobot-openloopcontrol/assets/119393980/165a4b56-43b7-419b-a26f-a0a593f97c7b)

## MobileRobot Movement Video:

https://youtu.be/wR3m9QyEGT8?si=X_rOKWj3jncRso1_

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
