# Design Architecture: NMSU Parking App
Scuff Development
Bianka Boudreaux, Patrick Jojola, Rey Aguirre

# Project Overview
An application with GPS tracking that would be able to let users know when an open parking space, near your preferred location, is available.

Additional features/goals include, but not limited to, the following:
  - Interactive map that shows users the overall parking map of NMSU and which lots are closest based on a search bar. 
  - Database that will have an accurate model of the real-world parking space right next to Science Hall on NMSU Campus.
  - Create a working prototype of an Ultrasonic sensor that will keep a running tally; of the number of cars within the parking lot.

# Key Architectural Drivers
Essential System Requirements:
1. Ultrasonic Sensor/Arduino
  - Arduino collects data of count of cars in a given parking lot, with a live sensor. WIFI module for Arduino will send data to web server.

2. Web Server/Database
  - Java web server will collect data from Arduino, which will then be sent to Swift IOS app for further data manipulation.
   
3. Swift IOS Parking App
  - Finally, the app will display available parking spots for a given lot based on the running count collected from the Arduino.

# Architectural Style Choices
Pipes-and-Filter
- Parallel processing
- Flexible and Ease of editing
- Re-usability
- Filter most of the “Junk” data that the users don’t need to see.

Client-Server
- Server offers services
     - Stores important data
- Clients access services w/ request/reply protocol
- Client may send the server an executable callback
     - Client will request information on specific lots.

# Client Server
![Architecture Design (1)](https://user-images.githubusercontent.com/107898813/231241042-559f6ce4-fe35-4d17-9b33-a5d4508bf7ad.jpg)

# Conclusion
Architectural Driver:
Client-Server

Issues:
- Could arise an overload of the server if redundancy is not built to handle all the data being sent in.
- Bugs could be unforgiving
    - If one aspect of the system fails, the whole system fails

Risks:
- Addition of large numbers of independent filters could reduce performance. 
- Ultrasonic sensor could produce incorrect data on lots.

Client Implications:
- Fully depends on the current load the wifi network has currently
