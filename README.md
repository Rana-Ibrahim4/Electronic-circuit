# Electronic-circuit
## Write an algorithm running servo-type motors to from a robot walking movement 



* Determine the number of servo motors required to achieve the desired walking motion. Typically, six servo motors are used - two for the hips, two for the knees, and two for the ankles.

* Connect the servo motors to the robot's control board. This may require using a communication protocol such as I2C or PWM to send control signals to the servo motors.

* Program the walking motion control logic. This involves simulating human walking by defining the appropriate joint angles for each servo motor at each step.

* Tune the motion parameters such as frequency, speed, and direction to achieve a natural and smooth gait.

* Test the motion and make necessary adjustments to the programming and physical connections.

* Integrate the walking motion with other robot functions such as balance and navigation.

ex Git : 

```
1. Define variables to store the position of each servo motor in the robot:

   - hip_angle: the angle of the hip motor
   - knee_angle: the angle of the knee motor
   - ankle_angle: the angle of the ankle motor

   These variables will be used to store the current angle values for each servo motor in the robot. These variables will be updated during the execution of the algorithm.

2. Calculate the required angles for each servo motor to achieve the desired limb position:
   - Use geometric relationships to calculate the required angles, such as:
     - Calculating the hip angle from the position of the pelvis and thigh
     - Calculating the knee angle from the position of the thigh and leg
     - Calculating the ankle angle from the position of the foot and leg

   In this step, geometric relationships will be used to calculate the required angles for each servo motor based on the current limb positions. These calculations may involve using trigonometry and mathematical equations to find the appropriate angles.

3. Move each servo motor to the calculated angle from the previous step using feedback control to ensure the required angle is reached.
   In this step, commands will be issued to move each servo motor to the angle calculated in the previous step.

4. Wait a short time period to stabilize the limbs in the new positions.
   After moving the motors to the new positions, a short time period will be waited to allow the limbs to stabilize in these new positions before proceeding to the next step.

5. Repeat steps 2 through 4 to obtain a repeating walking pattern.
   To obtain a repeating walking pattern, steps 2 through 4 will be repeatedly executed. This will result in the limbs being moved in a specific sequence to achieve the desired walking motion.
```
## Connecting and programming an electronic circuit containing 6 servo motors using a simulation program

### The key aspects of this task are :

* Connecting the 6 servo motors: The circuit needs to be designed to properly connect and control the 6 servo motors. This likely involves using a microcontroller or servo driver board to provide the necessary control signals and power to the servo motors.

* Servo motor control: The program needs to be able to control the position of each of the 6 servo motors independently. This involves sending the appropriate control signals to each servo motor to move it to the desired angular position.

* Simulation environment: The circuit and servo motor control logic needs to be implemented in a simulation program or software. This allows testing and verifying the behavior of the system without having the physical hardware.


  #### Some common simulation tools that could be used for this task include:

 * Arduino simulation software (e.g. Tinkercad, Fritzing)
* Robot simulation environments (e.g. Gazebo, V-REP, Webots)
* General electronics simulation tools (e.g. Multisim, Proteus)

  #### In simulation,the key steps would be :
1. Modeling the 6 servo motors and their connections to the microcontroller or driver board.
2. Implementing the control logic to send the appropriate signals to each servo motor to achieve the desired positions.
3. Visualizing the movement of the servo motors and the overall system behavior in the simulation environment.

The goal is to create a virtual prototype of the electronic circuit and servo motor control system, allowing you to test and refine the design before implementing the physical hardware. The simulation should demonstrate the functionality and movement of the 6 servo motors based on the control algorithms developed.

#### IMG of the electronic circuit

![Powerful Blorr-Snaget (1)](https://github.com/Rana-Ibrahim4/Electronic-circuit/assets/173770938/6ef54ac6-621a-4ec3-b9c8-0024c135c1fe)



![b1b1eba3-6555-41e6-a943-31a1123f520c](https://github.com/Rana-Ibrahim4/Electronic-circuit/assets/173770938/5c0ac1a3-1138-4ee1-9611-8500465190b9)


![941b0737-85c2-4f1a-94e8-ff044d4e7a9b](https://github.com/Rana-Ibrahim4/Electronic-circuit/assets/173770938/c25c9980-dd5e-44a4-b52d-0f10a5a659b2)

#### Code of Ardiuno IDE

ex git :

```

// C++ code
//
#include <Servo.h>

Servo servo_13;

Servo servo_12;

Servo servo_11;

Servo servo_10;

Servo servo_8;

Servo servo_7;

void setup()
{
  servo_13.attach(13, 500, 2500);
  servo_12.attach(12, 500, 2500);
  servo_11.attach(11, 500, 2500);
  servo_10.attach(10, 500, 2500);
  servo_8.attach(8, 500, 2500);
  servo_7.attach(7, 500, 2500);
}

void loop()
{
  servo_13.write(90);
  servo_12.write(90);
  servo_11.write(90);
  servo_10.write(90);
  servo_8.write(90);
  servo_7.write(90);
  delay(10); // Delay a little bit to improve simulation performance
}

```


