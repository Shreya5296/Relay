# Relay

We need to use one end devices, that can be anything for example: A bulb with a holder and plug, a table lamp or mosquito repellent machine.

“A relay is an electromagnetic switch operated by a relatively small electric current that can turn on or off a much larger electric current.”
The heart of a relay is an electromagnet which is a coil of wire that becomes a temporary magnet when electricity flows through it.

Purpose of Relay:
To convert small electric current into high electric current, like DC (Direct Current) into AC (Alternating Current)

Step -1: Gather the material from the IoT kit:
● 1 x ESP32
● 1 x USB Cable
● 1 x Breadboard
● 3 x Jumper wires
● 1 x Relay
● 1 x Bulb, Lamp, Mosquito Repellent Machine

Step -2: Let’s do connections:
Relay Pins Wiring Connections
VCC(Red) Connect with 3V3 PIN of the ESP32
GND(Black) Connect with GND of the ESP32
INPUT(Yellow) Connect with GPIO PIN 23

The first and foremost step is to create an account on the Arduino IoT Cloud.
1. Go to - https://cloud.arduino.cc/
2. Go to the top right hand side of your screen and click on the square with dots option.Then, click on IoT Cloud.
3. First we need to create a “thing” for our internet of things. So, click on the “CREATE THING” button.
4. Now, you will add a name to this project.
5. After that we need to add a variable named led. This variable will hold the status of our switch.
6. Change the name of the variable to led. Select variable type as “Light”.
7. As we want to switch it on and off in the program, we will assign Read & Write permissions to this variable.
   Also, we would want to update this variable with a switch. Hence, the Variable Update Policy will be set to On Change.
8. Now, we will set up the Associated Device.
   a. Click on the Select Device button.
   b. Click on Set Up a 3rd Party device.
   c. Select the device type as ESP32 and set the module as ESP32 Wrover Module.
   d. Click CONTINUE and add a Device Name.
   e. Now, it will show the Device ID and Secret Key. Copy the Device ID and Secret Key. Make sure you store it somewhere before proceeding with the next steps.
   f. Click on CONTINUE
9. Once the Associated Device is set, go to the Network section and click on the configure button.
    a. Add Wi-Fi Name and Password. Also, add the Secret Key generated while adding Associated Device.
10. Let’s write the program now
    a. Click on the Sketch tab where the predefined code will automatically be added.
    b. Let’s observe the code. We will understand the code and add new functionalities to this project. Initially, thingProperties.h header file is included.
    c. After that setup() method is defined. Here, we will define the pinMode() for pin number 23.
    d. Now, find the onLedChange() method at the bottom. Write the code to set the pin 23 to HIGH and LOW depending on the led variable.
11. Add the switch to control the led variable:
    a. Go to the Dashboards tab and click on the BUILD DASHBOARD button.
    b. Add a name and add a switch to the dashboard.
    c. After that, let’s link the led variable to the switch. Click on the Link Variable button and click on DONE.
    d. Select the led variable and click on LINK VARIABLE

After you create this dashboard, you can also download the Arduino Iot Cloud Remote app on your phone from the playstore.
Once you have downloaded the app, login with the same credentials. You should be able to control the device from your phone now

12.Go back to things again, open your project and go to Sketch. Upload the sketch to your ESP32 board by clicking on right arrow button .
13.Once it is uploaded, go to the Dashboard and control the light with the switch.
