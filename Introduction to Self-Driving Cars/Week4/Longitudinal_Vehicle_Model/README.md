#### Implement longitudinal vehicle model

- The Step Function Calculate
  1. Engine Torque
  2. Gravitational Force
  3. The load forces consist of aerodynamic drag
  4. Rolling Fraction
  5. Engine Speed 
  6. wheel Slip 
  7. Tire Force 
  Then Update
  8. Distance = old_Distance + Velocity * SampleTime
  9. Velocity = old_Velocity + Acceleration * SampleTime
  10. Acceleration = (Fx - Fload)/m
  11. We = We + We_dot * SampleTime
  12. We_dot = (Te - GR(Reff * Fload))/Je

- Implement Ramp Angle 
  1. Get Alpha

![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week4/Longitudinal_Vehicle_Model/Image/Alpha.PNG?token=AICENQYOFBHLI6S3MEO6LC27CYBUA)

   From the Image Get
   - if x < 60 so Alpha is Constant and Equal (y/x) = arctan(3/60)
   - if x between 60 , 150 Alpha is Constant and Equal (y/x) = arctan(3/60)
   - if x more than 150 Alpha will be zero

2. Get Throttle

![Image](https://raw.githubusercontent.com/Nada8773/Self-Driving-Car/master/Introduction%20to%20Self-Driving%20Cars/Week4/Longitudinal_Vehicle_Model/Image/Throttle.PNG?token=AICENQ67RDM6GDUG3M6AAJK7CYB2O)

   - As t_data.shape[0] equal to 2000
   - So 5s means 500
   - check if x less than 500 the throttle will be (slop * x + b)
   - if x between 500 and 1500 the throttle is const and equal to 0.5
   - if x more than 1500 so throttle will be (slop * x + b) slop is negative

