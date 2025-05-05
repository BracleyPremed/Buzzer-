<h1 align="center"><strong> Buzzer </strong></h1>

<p>This project covers the basics of how to connect a buzzer and use the <code>tone()</code> and <code>noTone()</code> functions with an Arduino board.</p>

![Final Project](https://github.com/BracleyPremed/Buzzer-/blob/main/BZ.png?raw=true)
---

## Buzzer Component Basics

- **Long leg**: Positive (Anode) — connect to a **digital pin** on the Arduino  
- **Short leg**: Negative (Cathode) — connect to **GND (ground)**

> Just like an LED, polarity matters with buzzers. Always double-check the legs.

---

## Setting Up a Buzzer in Arduino

1. Choose a pin to control your buzzer.
2. Define the buzzer pin using a **constant integer**:

   
   ```cpp
   const int buzzer = 2;

    ```
Place the declaration outside of setup() and loop() so it's available globally.


 ```cpp
void setup() {
  pinMode(TonePin, OUTPUT);
}

void loop() {
  tone(TonePin, 1000, 2000); // Plays 1000Hz tone for 2 seconds
  delay(400);                // Wait for 400 milliseconds
}

 ```
Key Points About the Code

 ```cpp
pinMode(pin, OUTPUT); // Initializes the buzzer pin as an output.
 ```

 ```cpp
tone(pin, frequency, duration);// Generates a square wave of the given frequency (Hz) on the pin for the specified duration (ms).
 ```

 ```cpp
noTone(pin);: Stops the sound on that pin.
 ```

 ```cpp
delay(milliseconds);: Pauses the code; useful for timing between tones.
 ```


<strong> Note</strong>
Do not connect buzzers directly to power without a current-limiting resistor if you're unsure about their specs.

<strong> <i> Quick Reference:</i></strong> tone() 

<strong> Parameter	Description </strong> 
<p> <strong> pin </strong>	Digital pin connected to the buzzer <p>
<p> <strong> frequency</strong> Pitch in Hz (e.g., 1000 = 1kHz) <p>
<p> <strong> duration </strong> 	Time in ms the tone will play <p> </br>



<strong>  Sam Cherilus <strong> 
