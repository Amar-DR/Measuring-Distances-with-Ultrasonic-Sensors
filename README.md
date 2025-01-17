Materials Needed:
-HC-SR04 Ultrasonic Sensor
-LED (Light Emitting Diode)
-Resistor (220Ω)
-Arduino Board (e.g., Arduino Uno, Mega)
-Jumper Wires
-Breadboard (optional)


Explanation:
#define echoPin 7 and #define trigPin 8 → These define the pins used for the ultrasonic sensor. The echoPin receives the reflected sound wave, and the trigPin sends the pulse.
long duration; → This variable stores the time taken for the sound wave to travel to the object and back.
int distance; → This variable stores the calculated distance from the sensor to the object.
pinMode() functions → These are used to configure the pins as OUTPUT for the trigger and LED, and INPUT for the echo.
pulseIn(echoPin, HIGH) → This reads the time taken for the pulse to travel back to the echoPin.
distance = duration * 0.0344 / 2; → This formula calculates the distance in centimeters. The constant 0.0344 represents the speed of sound in cm per microsecond.
Serial.print() → Prints the measured distance to the Serial Monitor.
LED Control → If the measured distance is less than 10 cm, the LED is turned on, otherwise it is turned off.
delay(500); → Pauses for 500 milliseconds before making the next measurement.


