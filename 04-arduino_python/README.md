# Python x Arduino on ESP32 Test

### Controlling LED Brightness with PWM
In a loop, it gradually decreases the LED's brightness from 100% down to 0% in steps of 10, with a 0.5-second delay between each change. This effect simulates a dimming of the LED.

The way this works is by using PWM (Pulse Width Modulation) in Arduino. PWM allows controlling the power (in this case, brightness) of an LED by changing the ratio of time at which the LED is switched on and off in a cycle.

Duty Cycle Ratio: PWM works by adjusting the ratio of time between ‘on’ and ‘off’. For example, with a duty cycle of 100%, the LED is always on, and with a duty cycle of 50%, the LED will be on half the time and off half the time. The brightness of the LED will appear lower if the ‘on’ ratio is lower.

### Proving

<img src="https://github.com/gredychristian/Mikrokontroller-A081_22081010195_Gredy-Christian-Hendrawan-Putra/blob/main/04-arduino_python/Python%20on%20ESP32%20Test%20PWM%20Control%20LED%20Power.gif" height="500">
