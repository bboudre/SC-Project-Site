# Design Document

## Architecture Model
![arch2](https://user-images.githubusercontent.com/107898813/233269676-bf9874a0-2c79-4797-af45-d27e5691ba1b.jpg)

The chosen architecture for the application "Aggie Park" is client server model with 3 major programs driving the architecture. The ultrasonic sensor detects a specific distance when a car passes it and in turn sends it to the web server to translate it to the database to keep track of the number of cars going in and out of the parking lot. In the app the user is able to request navigation to their desired destination and get info on the number of parking spots available from the web server. Notifications are sent when a closer parking space is found as well. 

### Parking App (IOS Application)
Swift is responsible for the user interface of the app. It provides an intuitive and user-friendly way for users to search for available parking spaces. It will also communicate with the Arduino code and the web server to retrieve and display information about available parking spaces. Functions of the app include navigation, interactive map of NMSU, and settings to change certain functionalities of the app. 

### Ultrasonic Sensor (Arduino)
The Arduino is responsible for collecting and transmitting data from sensors located in the parking spaces. These sensors detect the presence of a vehicle in the parking and it communicates this information to the web server and then to the app.

(For the scope of the current project)
2 sensors will be placed in the entrance and exit to keep track of the number of cars, rather than having a sensor in each parking space. 

### Web Server (Java)
The web server is the backbone of the parking app, by providing a centralized location for storing and accessing information about available parking spaces. The web server communicates with Swift and the Arduino to provide real-time updates on parking availability.
This is the main web server that will get send the info from the Arduino, to then, update the parking app.

## Major Classes / Components

### FindParking(User,Destination)
This is class is used when the user requests navigation to their desired destination based on campus buildings. Parking lots shown will be first filtered through the user info. The user info is based on 2 options of being a student (corresponding to permit type) and faculty/staff.

### AvailableParking()
After the request is made the web server will send back information for the available parking spots open its corresponding lot. The navigation will update the destination as the parking lot. 

### distance 
The value interpreted by the web server of the number of cars going in and out of the parking lot. 

### numCars
It what the web server sends to the database to keep track of the number of cars in the parking lot. 

## Control Issues
Functionality of the app design depends on the WIFI connection, and users may find it difficult to use the app if traffic is high. The data stream may also be delayed if traffic is high at a given time. 

Reliance on good internet has been one of our biggest constraints, and it also affects the total user experience. If one of the components of our system is down, the whole system is down.




