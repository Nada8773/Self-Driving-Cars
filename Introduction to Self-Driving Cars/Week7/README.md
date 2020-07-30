## Implementation

In this project, implement a controller for the CARLA simulator.
will control the vehicle to follow a race track by navigating through preset waypoints. 
The vehicle needs to reach these waypoints at certain desired speeds, so both longitudinal and lateral control will be used.

![Image](https://github.com/Nada8773/Self-Driving-Car/blob/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/vehicle%20track3.PNG)
![Image](https://github.com/Nada8773/Self-Driving-Car/blob/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/vehicle%20track2.PNG)


#### 1. longitudinal vehicle Modle
- will use the equation in the image to get acceleration
  and in this assigment will assume that acceleration equal to throttle
  
![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/Longitudinal1.PNG?token=AICENQZQZ4IKTZR3NMV62FC7ELS2K)

#### 2. Lateral Vehicle Modle

- For this project i used  Pure pursuit is the geometric path tracking controller.
  A geometric path tracking controller is any controller that tracks a reference path using only 
  the geometry of the vehicle kinematics and the reference path

![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/lateral3.PNG?token=AICENQZLZQY25LTJRKOCPCC7ELSQO)
![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/1.PNG?token=AICENQ5H2GPLHQT6GYPRBYS7ELSIC)

###### Lateral Formaluation
![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/lateral1.PNG?token=AICENQ62SVXU2JS3WXK3RHK7ELSXO)

![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/lateral2.PNG?token=AICENQYKFTNSMOBFHT62BU27ELSUQ)

#### Solution Figures
![Image](https://github.com/Nada8773/Self-Driving-Car/blob/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/out1.PNG)

#### Grade
![Image](https://github.com/Nada8773/Self-Driving-Car/blob/master/Introduction%20to%20Self-Driving%20Cars/Week7/Image/out.PNG)


## How to use
- Windows 10 
1. Run the carla simulator
  - Use that command
   - CarlaUE4.exe /Game/Maps/RaceTrack -windowed -carla-server -benchmark -fps=30
2. Run Your Python Script 
   - python module_7.py

## Reference 

- Empirical PID gain tuning (Kevin Lynch)
https://www.youtube.com/watch?v=uXnDwojRb1g

- PID 
https://nicisdigital.wordpress.com/2011/06/27/proportional-integral-derivative-pid-controller/

- Three Methods of Vehicle Lateral Control: Pure Pursuit, Stanley and MPC
https://medium.com/@dingyan7361/three-methods-of-vehicle-lateral-control-pure-pursuit-stanley-and-mpc-db8cc1d32081
