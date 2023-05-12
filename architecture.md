## ★Future Work★ [May 2023]
To keep the integrity of documentation this notice is posted as an overiew of features not implemented.

* Switch from a local search on MapKit to a custom annotation search. 
    * database for campus buildings' closest parking lots based on permit type
* Map parking lot annotations and reroute polyline to chosen parking lot 
* Update real-time for duration to get from user location to destination 
* Send notifications to user if closer parking is found if desired 

**Arduino, WIFI module, and sensor are not compatible with each other for the goals of this project**
* If troubleshooting works connect Arduino and web server to communicate with app 
* Otherwise research for a more efficient mechanism to detecting open/free parking spots
* If we had the capital, we could have researched into making our own microcontroller design / or also go the route of Raspberry pi

# Design Architecture
## Project Overview
An application with GPS tracking that would be able to let users know when an open parking space, near your preferred location, is available.

Additional features/goals include, but not limited to, the following:
  - Interactive map that shows users the overall parking map of NMSU and nearby parking lots based on desired building destination. 
  - Database that will have an accurate model of the real-world parking space right next to Science Hall on NMSU Campus.
  - Create a working prototype of an Ultrasonic sensor that will keep a running tally; of the number of cars within the parking lot.

## Key Architectural Drivers
Essential System Requirements:
1. Ultrasonic Sensor/Arduino
  - Arduino collects data of count of cars in a given parking lot, with a live sensor. WIFI module for Arduino will send data to web server.

2. Web Server/Database
  - Java web server will collect data from Arduino, which will then be sent to Swift IOS app for further data manipulation.
   
3. Swift IOS Parking App
  - Finally, the app will display available parking spots for a given lot based on the running count collected from the Arduino.

## Architectural Style Choices
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

## Architecture Model - Client Server 
- Updated model
![arch2](https://user-images.githubusercontent.com/107898813/233269676-bf9874a0-2c79-4797-af45-d27e5691ba1b.jpg)

## Conclusion
Architectural Driver: Client-Server

Issues:
- Could arise an overload of the server if redundancy is not built to handle all the data being sent in.
- Bugs could be unforgiving
    - If one aspect of the system fails, the whole system fails

Risks:
- Addition of large numbers of independent filters could reduce performance. 
- Ultrasonic sensor could produce incorrect data on lots.

Client Implications:
- Fully depends on the current load the wifi network has currently
