# Cliff: Autonomous Quadruped Robot

Cliff is an Arduino-based quadruped robot designed and built in two weeks for a Mechatronics final project. It combines mechanical design, embedded programming, and sensor integration to move independently, avoid obstacles, and respond to a simulated treat.

## Features

- **Quadrupedal locomotion:** Four independently controlled servo motors coordinate the legs to produce forward shuffling motion.
- **Obstacle avoidance:** Two front-mounted infrared sensors detect obstacles and trigger changes in direction.
- **Interactive treat mode:** An ultrasonic sensor detects an object approximately 2 cm away, causing Cliff to stop, wag its tail, and sit for two seconds before resuming movement.
- **Digital collar:** An OLED display shows the robot’s name.

## Hardware

- Component Purpose 
- Arduino - Runs the control program and processes sensor input 
- Four leg servos - Control locomotion and sitting 
- One tail servo - Produces tail-wagging motion 
- Two infrared sensors - Detect obstacles on the front left and right 
- Ultrasonic sensor - Detects nearby objects to activate treat mode 
- OLED display - Displays Cliff’s name 
- Two 6V battery supplies - Provide power 

## How It Works

During normal operation, Cliff coordinates its four leg servos to shuffle forward while monitoring the infrared sensors. When an obstacle is detected, the robot adjusts its direction to avoid a collision.

When an object is placed approximately 2 cm in front of the ultrasonic sensor, Cliff enters treat mode:

1. Stops moving forward.
2. Wags its tail.
3. Sits for two seconds.
4. Returns to normal walking behavior.

Treat recognition is based on distance sensing; Cliff does not visually identify food.

## Design and Development

The project required repeated mechanical adjustments, programming changes, and physical testing.

Because the legs do not have knee joints, developing an effective walking motion was a major challenge. I spent approximately one week experimenting with cardboard foot designs to improve traction and help the robot push itself forward.

An early wiring approach connected two servos to the same control pin, limiting independent leg movement. I revised the wiring to give each servo its own control pin, enabling more flexible movement and coordinated behaviors.

## Challenges and Limitations

- Locomotion relies on shuffling rather than a natural stepping gait.
- Maintaining a straight path remains a challenge.
- Obstacle avoidance uses simple sensor-based reactions.
- Movement depends on foot geometry and contact with the floor.

## Future Improvements

- Improve foot designs for more consistent traction.
- Refine servo timing for smoother movement.
- Improve directional control.
- Explore additional leg joints and more advanced gait patterns.

## Skills Demonstrated

- Arduino programming
- Sensor and actuator integration
- Servo coordination
- Mechanical prototyping
- Electrical troubleshooting
- Iterative testing and debugging

## Author

Ashlynn Flammia
