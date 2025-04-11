## Design and Implementation of Arduino Based Air
## Quality Meter Using Blynk
# Abigail Frimpong
## Queen Mary University
Corresponding email: a.frimpong@se24.qmul.ac.uk
## Abstract 
Air pollution is the contamination of the atmosphere, primarily due to human
activities. Due to the lack of awareness, the air is being polluted by various sources; in recent
years, it has become a major concern, largely driven by the growing number of factories,
vehicles and mills. These sources have contributed significantly to air pollution by releasing
smoke and toxic gases like Nitrogen dioxide (NO₂) and Particulate Matter (PM2.5 & PM10).
This project presents an Internet of Things (IoT) – -based pollution monitoring system to
measure hazardous gas levels in the air.
The data collected by the system can be viewed through a smartphone application; in this
project we used Blynk.
Keywords: Internet of Things (IoT), Humidity sensor, Gas Sensor, Air Quality, Arduino Uno,
Blynk Software.


## Hardware Connections Design
### 1. Sensing - DHT11 Temperature/

Humidity:

o VCC: 5V (Arduino)

o GND: GND (Arduino)

o Data Pin: Any digital pin (e.g.,
D2)
### 2. Sensing - MQ-2 Gas Sensor:

o VCC: 5V (Arduino)

o GND: GND (Arduino)

o A0 (Analog Pin): Analog input
pin on Arduino (e.g., A0)
### 3. Display- I2C LCD 2004:

o VCC: 5V (Arduino)

o GND: GND (Arduino)

o SDA: SDA pin (on Arduino
UNO: A4)

o SCL: SCL pin (on Arduino
UNO: A5)
### 4. Controller & Communication -
Arduino UNO R4 WiFi:
 No specific connection to power
or GND, just connect the
required sensors and the LCD to
the board pins as mentioned.

## Software Development
The air quality monitoring system consists
of the peripheral devices with software.
The monitoring system includes several
sensors, like the Gas and temperature
sensors, MCUs and connections for
communication that can be programmed by
the Arduino UNO R4 WiFi.

After that, all virtual and hardware
connections will be implemented and
synchronized with the Blynk application;
the latter controls the Arduino
microcontroller on the internet.

We will use Arduino Uno IDE application
to edit the developed code to allow
functionality upon detection of an air
quality condition. The Arduino Uno Ide
will check if the code is compiling
successfully and is verifying. Upon
success, the code will be uploaded on the
Arduino Uno via its serial peripheral
interface (SPI) bus.

Arduino Uno R4 Wi-fi will collect all the
data from the sensors, process it, and
upload it to the Blynk app over its
integrated ESP32-S3 module which allows
users to connect to Wi-Fi networks and
perform network operations.
Then the data is sent to the I2C LCD 2004
module and Blynk applications.
The received data will be analysed and
utilised on data visualisation for the end-
user to receive the air quality updates and
notifications based on the notification alerts
(functions presents with the Blynk app on a
smartphone).

 ### Software Libraries
It is required to download some software
libraries to connect both the hardware
devices and to link Arduino to Blynk
interface.

To connect the hardware devices to the
Arduino UNO R4 Wifi, download the
following libraries to Arduino IDE:

• 𝐿𝑖𝑞𝑢𝑖𝑑𝐶𝑟𝑦𝑠𝑡𝑎𝑙 − 𝐼2𝐶 [8] available
on Github. This provides the
interface to connect the Arduino
UNO to the LCD.

• 𝐷𝐻𝑇11 [9] also available to
download on Github and on the
Arduino IDE Library Manager [10].

• 𝐴𝑛𝑎𝑙𝑜𝑔𝑅𝑇𝐶𝐿𝑖𝑏 by Analog devices
[10]. This library helps as an
interface for Analog devices (like
the MQ-2 Gas Sensor) Real time
clocks.

To implement and link the sensors' output to
Blynk downloaded the following libraries to
Arduino IDE:

• 𝐵𝑙𝑦𝑛𝑘 by Volodymyr Shymanskyy,
downloadable from GitHub [11].
This allows the connectivity of the
Arduino UNO R4 Wi-fi board with
Ethernet, Wi-Fi, Cellular. This is
necessary to connect the
Arduino’s IP address to the Wi-fi in
use. The Arduino’s IP address can
be obtained by searching through
the connected devices on the Hub
The manager of the Wi-Fi router is
used.

### Conclusion
Air quality in this day and age is of notable
consideration due to the rate of air pollution
and the environmental and health
implications caused by this.
Air quality monitoring helps improve the
quality of air by eliminating the observed
causes of changes in the air quality.
Air quality monitoring can be expensive but
with this IoT implementation system, it is
offered an accessible, cost effective and
efficient way of keeping track of air
pollution and environmental changes.
With the use of Blynk’s dashboards on the
smartphone, users experience a system that
allow air quality monitoring in a target area,
thus taking any actions or precautions to
keep the air quality under control or to
avoid the area entirely if unsafe to visit.
This is a highly user-friendly, economical
and with urgent necessity application.
#define BLYNK_PRINT Serial
