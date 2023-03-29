# Problem Statement

## Introduction
### 1.1 Purpose of Product
Looking for parking around campus can be a time-consuming task. In 2022 the biggest freshman class since 2009 enrolled at NMSU main campus (2.6 increase). With more students enrolled, the number of available parking spaces has been lessened. There are about 13,500 parking spaces available and 14,268 students enrolled as of 2022. Free lots do offer available parking spots but at the disadvantage of a distance. 

The Possible solution is an application with GPS tracking that will be able to let you know when an open parking space near your preferred location is available. The user would input their preferred location and the system would let the user know the closest available spots. Spot allocation will be on a first come/ first serve basis.

### 1.2 Scope of Product
The overall Scope of this product will be the following: 
* Interactive map that shows users the overall parking map of NMSU and which lots are closest based on a search bar. 
* Create a Database that will have an accurate model of the real-world parking space right next to Science Hall on NMSU Campus.
* Create a working prototype of an Ultrasonic sensor that will keep a running tally; of the number of cars within the parking lot.
* The use of Google Map API to help the user get to said parking lot.
* Simple UI design to create a seamless user experience.

### 1.3 Acronyms, Abbreviations, Definitions
- APIs 
- Database/Web Server
- Arduino 
- - Ultrasonic sensor 
- Swift 

## General Description of Product
### 2.1 Context of Product
This product could branch out to other bigger buildings with large parking spaces.But, for Scuff Development this will mostly be based on the bigger parking lot next to Science Hall on NMSU Campus. The application will be accessed through your phone, we will be developing for IOS users specifically (ie.Swift). 

### 2.2 Domain Model with Description
![Domain Model](/Domain%20Model-User.png)

The domain model is for the user class. The user must select if they are a student or faculty member. If they are a student, they will be asked about their permit. The app then uses the initial user data for the campus map and finding parking functions. In the settings the user can change the initial data submitted. 

### 2.3 Product Functions (general)
With the combined effort of database/web server use, APIs, and Sensors, we would be able to:
* Have a service that will help out students and also faculty on NMSU campus. 
* Reduce the amount of driving around to find an open parking space.
* Produce an interactive map that will be a collection of NMSU parking spaces where users can search for lots closest to their desired building location. 

The pseudo code for the mechanics of the ultrasonic sensor would be as follows:

```
Func checkSpot(Sensor echo (data)) {
  
  // If there is an echo, there is an object in front of sensor
  If (echo)
    Return Taken
  
  // No echo = no object, parking spot is free
  Else
    Return Open
}
```

### 2.4 User Characteristics and Expectations
The expectations we will have for users is the following:
* Moderate knowledge of using the internet/ knowledge over common UI design within using any app on a phone.
* Users will also be mainly college students and also faculty. 

### 2.5 Constraints
Most of the Constraints for this Project will be time management. Since, we can’t possibly launch a full-scale project. We will be testing the main features using simulated data.    

### 2.6 Assumptions and Dependencies
The assumptions we will have for this project will be the following: 
* The use of Simulations
* One working prototype of the sensor
* The use of APIs 
* A cloud system to streamline 
To create the main code to detect and update live the amount of cars within a parking lot.  

## Functional Requirements
Our expectations for functionally at the end of this project will be the following. Seamless/ease of use experiences for the users. Working, databases that will update continuously. 

## System and Non-functional Requirements
### 4.1 External Interface Requirements (User,Hardware,Software,Communications)
The user should have the ability to operate the software on their phone. The interface will have a simple layout with options to look at interactive maps and start routes. 

### 4.2 Performance Requirements
The software will need possibly about up to 150 MB of space to operate. Depending on the progress of the project the number may change. 

### 4.3 Design Constraints
Some of the Design Constraints for us would be deciding on just going with an Arduino Uno board. Instead of going fully into creating a custom board-circuit.Since, we are more focused on the actual programming side, not the physical tech side.

### 4.4 Quality Requirements
The quality expectation for this would be; an usable app

