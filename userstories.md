## ★Future Work★ [May 2023]
To keep the integrity of documentation this notice is posted as an overiew of changes made and features not implemented.

* Switch from a local search on MapKit to a custom annotation search. 
    * database for campus buildings' closest parking lots based on permit type
* Map parking lot annotations and reroute polyline to chosen parking lot 
* Update real-time for duration to get from user location to destination 
* Send notifications to user if closer parking is found if desired 

**Arduino, WIFI module, and sensor are not compatible with each other for the goals of this project**
* If troubleshooting works connect Arduino and web server to communicate with app 
* Otherwise research for a more efficient mechanism to detecting open/free parking spots

# User Stories

## Freshman student at NMSU

*As a person that’s totally new to the parking situation at NMSU Campus, I would like to have a dedicated app that will show where I can park based on my permit, open spots, and how to navigate to the spot.*

Elaboration: Users should have the ability to just open the app. Input their status on where they can park; and find where is the closest parking spot based on their desired campus building location.
				
Effort Estimation: ~60-80 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: Perform the task of having the user input. Then 
seamlessly translate to the in-app navigation to the parking spot.
	 
	 	 	
## Senior student at NMSU with some development knowledge
	 	 	   
*As a student that has the NMSU parking map like the back of my hand. I would love a dedicated app that will show the closest parking lot with open spots. Navigation would be nice but not really an importance.*

Elaboration: User should be able to open the app. Input their destination based on campus buildings and be shown parking lots closet.
			
Constraint: Amount of time allotted to development, Knowledge in using sensors, How fast the app will update with new information.
	 
Effort Estimation: ~100-120 person-hours
			
Intergrated Tools: IPhone, some type of mini computer that will take the sensor data, and the use of some local sever to keep all the updated info.
	 	 	
Acceptance Test: Seamless use of the app running and use. It updates at least every time the user requests or automatically.


## Professor at NMSU
	 	 	
*As a faculty member there is a lot of options that are closer to the building I’m teaching in. The use of an official parking app for NMSU would be nice if it had the functionality of telling me the closest parking space that’s open. The spot chosen should have shortest distance to walk to the building I want to go to. Also a nice feature would to have an update if there is any closer spaces open than the original option.*
	 	 	
Elaboration: User will be able to open the app and input the building they need to go to. Based on the desired location the app will show the open parking space closest. The app should send me a notification suggesting to change routes if a better parking spot becomes available.
	 	 	
Constraints: The refresh rate of sending a notification to your phone. The usability of the UI.Lastly, how much cost for said app?
			
Effort Estimation: ~150-200 person-hours
			
Intergrated Tools: The use of a microcontroller sensor combo an iPhone, and also a local server to seamlessly send out notifications.
	 	 	
Acceptance Test: An app that runs flawlessly and is consistent in its operation


## Sophmore purchased a commuter permit

*Due to my classes being further away from free parking I purchased a commuter permit. I would like to have the option to update that I have a permit and have the possible parking shown updated.*

Elaboration: Users should have the ability to change their intial permit type and have the app update and correspond. 
	 	 	
Constraints: None
				
Effort Estimation: ~30-40 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: Perform the task of having the user input. The needed input, and then seamlessly translate to the in-app navigation. 


## Easy accessibility and navigation

*I want an app that is easy to navigate. I don't want anything too overcomplicated and fancy. I want to use this as a tool that is straight to the point.*

Elaboration: Users should be able to use the app easily and find what they need fast. 
	 	 	
Constraints: None
				
Effort Estimation: ~20 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: Find parking and access the map fast

## Route user location to destination 
*Have the ability to route the user's location to the destination* 

Elaboration: When users type in their desired destination a polyline should connect them with the destination.  

Constraints: None
				
Effort Estimation: ~6 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: App updates in realtime giving route on screen

## Search for destination using MapKit
*Be able to search for campus building on search bar and save it as a destination*

Elaboration: When users type in their desired campus building auto-complete should bring up the campus building. 

Constraints: None
				
Effort Estimation: ~4 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: App updates in realtime autocompleting


## Update parking lots with available parking 
*Sort the top 3 parking lots closet to desired campus building based on parking permit, availability, and distance 

Elaboration: The UI should update with the parking lots on screen ordering the best parking lot option the user can choose far left. 

Effort Estimation: ~20 person-hours
			
Intergrated Tools: Your device either iPhone or android
	 	 	
Acceptance Test: App updates in realtime with correct information 








