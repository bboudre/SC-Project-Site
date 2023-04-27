# Test Report

## Component Testing
### Arduino/Ultrasonic Sensor w/ ESP 8266 ESP-01 WIFI Module
The Arduino can be a powerful tool, but configuration and adjustments to the environment can take some time; but are necessary in order for desired code to be run on the Arduino IDE. For testing in the project, specific code files and wire configurations to the breadboard were saved to ensure correct functionality between the Arduino and the computer. Within these code files, there is the ultrasonic sensor test code, to test for correct output and functionality from the sensor, and the ESP 8266 ESP-01 WIFI module test code, to test for successful connectivity to the internet. Finally, the last test code file is a combination of all the components, to test that they can work and coincide with one another. The test code mainly consists of small, generic Arduino classes, but they ensure that these independent pieces, like the sensor, work correctly.
Performing these small configurations and testing at the start saves time from debugging later. 

The component testing consists of:
* Arduino Test Code
    * Ultrasonic Sensor
    * ESP 8266 ESP-01 WIFI Module
    * Whole System 
* Breadboard configurations (Wiring)

## System Testing
### Web Server
Testing the web server has a couple of different parts. The first one is making sure the web server, generated from Java code, is compiled and can be viewed with the correct HTTP response. This shows that our server can be manipulated and communicated with. Making sure that the web server works is vital because it acts as the storage bin to the data we are transporting. Next, we have to make sure the web server can receive and display test data. Test data, in terms of our project, can be total count on a parking lot like 1, 2, 3, etc. , or just the current time. Correct output on the web server allows for real-time data to be sent in and dealt with accordingly. 
The web server is the middle man, so testing for proper functionality unites our system together. 

### Swift IOS Application (Aggie Park)
Finally, testing for the Aggie Park app mostly consists of the user interface and collecting data to display to users. With the UI, making sure app pages and functionality, such as buttons and search bars, all work creates a better user-experience. Using XCode app preview, checking for bugs is extremely easy. The preview builds your app to allow you to see what it would look like on an IPhone. This makes design and overall look changes easy as well. Next, testing that the backend of Aggie Park can read and display test data from the web server on the app is another important piece. Test data, in terms of our project, can be total count on a parking lot like 1, 2, 3, etc. , or just the current time. Once this testing has passed, we can connect all the components for completion of the project. 

## Acceptance Testing
We validated the features based on User Acceptance Testing (UAT). Each separate component was tested frequently with progress. The user stories made prior were crucial in developing the features for the application. The acceptance criteria then determined if we needed to change the directions or debug for implementing the features. Below is the status of the user stories and acceptance test. The basics of UI and Design have been fully implemented as towards the “Senior student with development knowledge” wants. But we still need to add in the navigation API. Also, we have the choice of Faculty and Student towards both needs for “Freshman and Professor”. Lastly, we need to integrate more working parts for the sensor to send the data to the server then update the app. It currently does sense movement. For the most part it's on-par for the finishing on time for the schedule. That we Scuff Development Inc have set.  


### User Stories
    Freshman student at NMSU
Acceptance Test: Perform the task of having the user input. Then seamlessly translate to the in-app navigation to the parking spot.

    Senior student at NMSU with some development knowledge
Acceptance Test: Seamless use of the app running and use. It updates at least every time the user requests or automatically.

    Professor at NMSU
Acceptance Test: An app that runs flawlessly and is consistent in its operation

    Sophomore purchased a commuter permit
Acceptance Test: Perform the task of having the user input. The needed input, and then seamlessly translate to the in-app navigation.

    Easy accessibility and navigation
Acceptance Test: Find parking and access the map fast

