# Design Doc
Parking App (IOS Application)
Swift is responsible for the user interface of the app. It provides an intuitive and user-friendly way for users to search for available parking spaces. It will also communicate with the Arduino code and the web server to retrieve and display information about available parking spaces. Within what we labeled parking_app, is the detailed view of the campus map. In Settings, you will in the future, be able to change certain functionalities of the app. 

Ultrasonic Sensor (Arduino)
The Arduino is responsible for collecting and transmitting data from sensors located in the parking spaces. These sensors detect the presence of a vehicle in the parking and it communicates this information to the app. The Arduino code also controls other hardware components, such as gate openers and ticket dispensers, to provide a seamless user experience.

Web Server (Java)
The web server is the backbone of the parking app, by providing a centralized location for storing and accessing information about available parking spaces. The web server communicates with Swift and the Arduino to provide real-time updates on parking availability.
This is the main web server that will get send the info from the Arduino, to then, update the parking app.

#Architecture
![arch2](https://user-images.githubusercontent.com/107898813/233269676-bf9874a0-2c79-4797-af45-d27e5691ba1b.jpg)
