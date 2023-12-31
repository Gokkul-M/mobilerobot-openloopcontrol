# MobileRobot-Openloopcontrol
## Aim:
To develop a python control code to move the mobilerobot along the predefined path.
## Equipments Required:
1. RoboMaster EP core
2. Python 3.7
## Procedure

### Step1:
Imports Modules for controlling the RoboMaster robot,time-related functions,camera operations.
### Step2:
Move the entire code block under if _name_ == '_main_': to the right by one level of indentation. This creates a function-like structure.
### Step3:
Add def procedure_name(): before the indented code, replacing procedure_name with a descriptive name (e.g., perform_robot_actions).
### Step4:
Outside the if _name_ == '_main_': block, add procedure_name() to execute the procedure.
### Step5:
End the program.
## Program
```
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

    ep_chassis.move(x=2.55, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=225,effect="on")

    ep_chassis.move(x=0, y=-1.4, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=225,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=225,b=0,effect="on")

    ep_chassis.move(x=1.45, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=3, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=225,effect="on")

    ep_chassis.move(x=0, y=-2.1, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=170, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
![WhatsApp Image 2023-12-28 at 15 58 41_957b9482](https://github.com/Gokkul-M/mobilerobot-openloopcontrol/assets/144870543/6a4825b8-88e4-426f-8eca-9d9358e6e656)
![WhatsApp Image 2023-12-28 at 15 58 41_75a7e30d](https://github.com/Gokkul-M/mobilerobot-openloopcontrol/assets/144870543/6cf8526f-4c76-4025-a7f6-166a8bb4a81a)
![WhatsApp Image 2023-12-28 at 15 58 41_b0205d53](https://github.com/Gokkul-M/mobilerobot-openloopcontrol/assets/144870543/b922ae43-356f-4c9b-9ef2-e845634d2d87)
![WhatsApp Image 2023-12-28 at 15 58 41_b0358849](https://github.com/Gokkul-M/mobilerobot-openloopcontrol/assets/144870543/0a3c38e0-58e7-4c2a-a95c-5cc14665911e)
## MobileRobot Movement Video:
https://youtu.be/adctuwXHJtA
## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
