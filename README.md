## we are going to run servo and brushless motors with Arduino using a simple codes, so keep up with me :trollface:



# servo-motor-using-Arduino
We are going to run a servo motor using Arduino

### the connection should be something like this

![servo](https://user-images.githubusercontent.com/107954336/179149776-8fc1d202-0438-4007-aa3a-5e1455229a2e.png)

- the black wire on the ground.
- red wire 5v.
- the third wire you can connect it with any pin, in my example it was pin 11

#### Now let's move to the coding part

to create a servo object to control a servo and variable to store the servo position

```
#include <Servo.h>


Servo myservo;  
int pos = 0;    

```

now attach the servo on pin 11 to the servo object

```

void setup() {

  myservo.attach(11);  

}
```

we are going to use for loop to goes from 0 degrees to 180 degrees, by using "Write" we tell servo to go to position in variable 'pos'.
using "delay" to waits 10ms for the servo to reach the position.

```
void loop() {

  for (pos = 0; pos <= 180; pos += 1) { 

    myservo.write(pos);              
    delay(10);                      
  }
  ```
  
  using for loop to move from 180 degrees to 0 degrees, tell servo to go to position in variable 'pos'.
  waits 10ms for the servo to reach the position
  
  ```
    for (pos = 180; pos >= 0; pos -= 1) { 
    myservo.write(pos);              
    delay(10);                       // waits 15ms for the servo to reach the position

  }

}
 ```
 
 ### the result should be like this.
 
 

https://user-images.githubusercontent.com/107954336/179151868-fa429dd1-becb-4ad5-b6f0-47893838f6a6.mp4



# Brushless-motor-using-Arduino

### the connection should be like this

<img width="592" alt="image" src="https://user-images.githubusercontent.com/107954336/179473373-0af190d1-7b43-48b0-9b7d-7e59b99bdb9f.png">

and the code 

```
void setup()
{
   pinMode(13, OUTPUT);
   pinMode(12, OUTPUT);
  
}
void loop()
{
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
}

```
