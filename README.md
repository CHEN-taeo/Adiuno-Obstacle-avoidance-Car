--- 
>To be honest,this car cost much money about three hundred.But it is okay,i have made a full prepare for the cost.So let us have a eye feast.
--- 
## Project Introduction
This is a beginner-level 4-wheel-drive robot car control project based on Arduino.
I completed hardware wiring,pin-by-pin actual measurement,motor direction and stable drive code writing independently.
Solved many common novice bugs: inconsistent motor rotation direction,and the wire fired,wrong board silk-screen pins,single-side wheel failure and so on.


# Objiect list
- Main contronller : Arduino Uno R3
- Drive board: Integrated 4WD motor driver board
- Power supply: Lithium battery power pack
- Car chassis + 4 DC reduction motors
- Total cost: About 300 RMB
## physical Display

![Uploading tb_image_share_1778934633889.png…]()
![Uploading IMG_20260516_170329.jpg…]()


## Actual Measured Pin Definition
**Eliminate false labels on the driver board,all verified by manual testing**

LEFT_FORWARD = 4
LEFT_BACKWARD = 2
RIGHT_FORWARD = 8
RIGHT_BACKWARD= 7
Note: This board has no available ENA/ENB speed control pins, only pure direction control
--- 


## Complete Stable Running Code

```
// FINAL WORKING CODE - NO SPEED PINS NEEDED

# define LEFT_FORWARD 4

# define LEFT_BACKWARD 2

# define RIGHT_FORWARD 8

# define RIGHT_BACKWARD 7

// the pins are texted by me one by one

void setup(){

  // turn on motors

  pinMode(LEFT_FORWARD,OUTPUT);

  pinMode(LEFT_BACKWARD,OUTPUT);

  pinMode(RIGHT_FORWARD,OUTPUT);

  pinMode(RIGHT_BACKWARD,OUTPUT);

  

}

void loop(){

  //start to move

  

  // run forward for 2 second

  digitalWrite(LEFT_FORWARD,HIGH);

  digitalWrite(RIGHT_FORWARD,HIGH);

  digitalWrite(LEFT_BACKWARD,LOW);

  digitalWrite(RIGHT_BACKWARD,LOW);

  delay(2000);

  //run backward for 2 second

  digitalWrite(LEFT_FORWARD,LOW);

  digitalWrite(RIGHT_FORWARD,LOW);

  digitalWrite(LEFT_BACKWARD,HIGH);

  digitalWrite(RIGHT_BACKWARD,HIGH);

  delay(2000);

  // spin for left

  digitalWrite(LEFT_FORWARD,HIGH);

  digitalWrite(RIGHT_FORWARD,LOW);

  digitalWrite(LEFT_BACKWARD,LOW);

  digitalWrite(RIGHT_BACKWARD,HIGH);

  delay(1000);

  // spin for right

  digitalWrite(LEFT_FORWARD,LOW);

  digitalWrite(LEFT_BACKWARD,HIGH);

  digitalWrite(RIGHT_FORWARD,HIGH);

  digitalWrite(RIGHT_BACKWARD,LOW);

  delay(1000);

}
```

## Function Realized
1.Four wheels move forward and backward steadily
2.In-place left rotation & right rotation steering
3.Stable cycle operation,suitable as the basic chassis of obstacle avoidance robot

## Follow-up Upgrade Plan
- Access HC-SR04 ultrasonic sensor to realize automatic abstacle avoidance
- Optimize power supply structure to solve insufficient current problem

## Learning Experiences
As a mechanical engineering student who aims to engage in robot research and entrepreneurship,this chassis practice lets me truly understand the matching logic of hardware and program.
Only through actual measurement and repeated debugging can we master the underlying logic of robot control,rather than mechanically copying codes.
