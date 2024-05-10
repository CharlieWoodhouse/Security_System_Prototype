# Security_System_Prototype
The system will use ultrasonic  sensors and motorised mechanics to detect and track potential intrusions within the designated area. Upon  detection of suspicious activity, the system will lock onto the intruding object and provide real-time distance data.
![image](https://github.com/CharlieWoodhouse/Security_System_Prototype1/assets/147112008/c23199e3-2cb9-4a29-aeea-a3bdab3615dc)
## Object Detection + Locking
When scanning the environment, the ultrasonic sensor will identify if an object is in the specified range 
based on the distance measurements. This is done by sending out a brief pulse through the trigPin to 
trigger the ultrasonic sensor and measuring the time it takes for the pulse to bounce back to the echoPin.
The system evaluates the calculated distance against the predefined maximum distance threshold to 
determine if the object is within range, if the distance is less than or equal to the maximum threshold, the 
system will consider an object detected and proceed to halt the servo motor. This will allow the system to 
be locked onto the object allowing for further analysis to capture if the object is moving into the sensor by 
determining the distance from the sensor and the detected object. However, once the object is moved out 
of the detection range the motor will continue to overview the surrounding environment. This ensures that 
the system maintains focus on the potential intrusion and does not allow them to avoid the sensor when at 
the other end of the rotation.

## Distance calculation
The distance calculation will be done using the measured echo time duration, the system calculates the 
distance to detect the object based on the speed of sound (0.034) in the air and the time it took for the 
ultrasonic pulse to return after bouncing off the nearby object. The calculated distance is then used to 
determine the object's proximity to the sensor.

## Scanning
The motor has a sweeping motion pattern, allowing for a 0° to 180° rotation for the ultrasonic sensor to 
scan the area, measuring the distance within the detection range. When the motor rotates in the 180-
degree arc, the sensor will detect if an object is in the detection range in an overview of the surrounding 
environment from the ongoing surveillance and monitoring, allowing for the system to respond promptly to 
changes in detected object's positions
