# OLED-Weather-Display
Displays weather details of your city on an OLED display. (in collaboration with @suvam14das)

## Parts Required:
1. ESP8266 Module (Any one, I used NodeMCU)
2. 0.96" OLED (I2C Based)
3. Jumper Wires
4. Bread Board
5. USB Cable to attach ESP8266 to the computer

## Creating an account on openweathermap.org is straight forward.
Create an account by clicking on signup.
Login and go to the API Tab. Note your API Key.

## On NodeMCU the connections are as follows.
NodeMCU_____________OLED
3V  ---------------> Vcc <br />
GND ---------------> GND <br />
D1  ---------------> SCL <br />
D2  ---------------> SDA <br />

## Open the Program in Arduino IDE.
Select the ESP8266 Module that you are using from the Boards menu and Upload the code to the module.
The code updates the weather information every 10 minutes.
All the weather Icons are placed in the icon.h file.
Icon code is returned from the the call that we make to openweathermap.org
I have used a very crude parsing logic to extract the weather information from the json that is received.
You can used the json library for Arduino if you wish to.
