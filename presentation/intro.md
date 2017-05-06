---
title: Piece of Pi
---

## Piece of Pi

Python Programming with Raspberry Pi

<img src="images/pi.png" width="20%" />

<div style="font-size:70%;font-style:italic">Aaron Xiang</div>
<div style="font-size:50%;font-style:italic">Computer Science Club</div>
<div style="font-size:50%;font-style:italic">5/6/17</div>

---

### What is Raspberry Pi

* Credit card size computer               <!-- .element: class="fragment" -->
* Linux Operating System                  <!-- .element: class="fragment" -->
* General Purpose Input Output (GPIO)     <!-- .element: class="fragment" -->
* Suited for IoT projects                 <!-- .element: class="fragment" -->

---

### Computer in Palm

<img src="images/pi-in-palm.jpg" width="80%" />

---

### Raspberry Pi Circuit Board Layout

<img src="images/pi3-model-b.png" width="80%" style="background:white" />

---

### Controlling Light-emitting Diode (LED)

<img src="images/led-control-wiring.jpg" width="70%" />

---

### LED Control GPIO Configuration

<img src="images/led-control-pin.png" width="70%" />

---

### LED Control Programming (Python)

```python
import RPi.GPIO as GPIO   ## Import GPIO library
import time               ## Import time library

GPIO.setmode(GPIO.BCM)    ## Use Broadcom pin numbering
GPIO.setup(1, GPIO.OUT)   ## Setup GPIO Pin 1 to OUTPUT mode

## Blink LED 3 times
for i in range(3):
    GPIO.output(1, GPIO.HIGH)   ## Turn on GPIO pin 1
    time.sleep(1000)            ## Wait 1 second
    GPIO.output(1, GPIO.LOW)    ## Turn on GPIO pin 1
    time.sleep(1000)            ## Wait 1 second

GPIO.cleanup()    ## Reset all GPIO pins
```

---

### Ultrasonic Distance Sensor 
#### (HC-SR04)

<img src="images/hc-sr04.png" width="70%" />

---

### How Distance Sensor Works

<img src="images/distance-sensor-mechanism.png" width="80%" />

---

### Distance Calculation

Speed of sound: 343 m/s

<img src="images/hc-sr04-eq1.png" />
<img src="images/hc-sr04-eq2.png" />

---

### HC-SR04 Wiring Diagram

<img src="images/hc-sr04-config.png" width="60%" />

---

### HC-SR04 Timing Diagram

<img src="images/hc-sr04-timing.png" width="70%" />

---

Distance Sensor Python Code

<img src="images/hc-sr04-python.png" width="45%" />

--- 

### The End

---