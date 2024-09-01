代做、讲解请联系微信：liklikQAQ

# COMP201
COMP201 task 
Task1
1.General Operation

ID	uc1a
Actor	User
Name	Access System Use Case
Description	The “Access System” use case involves the User interacting with the system to gain access using a swipe card and an access code. The user must have a valid swipe card and enter the correct access code to successfully access the system.
Pre-conditions	•The user has a valid swipe card.
•The user is aware of the correct access code associated with the swipe card.
Event Flow	1.User swipes their card.
2.User enters the access code.
3.System verifies the card and access code.
4.If the verification is successful, the user gains access to the system.
Post-conditions	•If the verification is successful, the user is granted access to the system.
• If the verification fails, the user is denied access.
Includes	None
Extensions	•If the user enters an incorrect access code three times, the system triggers the “Lock User Out and Sound Tamper Alarm” use case.
Triggers	Card reader，Password Input Terminal

ID	uc1b
Actor	User (Staff)
Name	Configure Burglar Alarm
Description	The“Configure Burglar Alarm”use case involves the User configuring the burglar alarm system after successfully accessing the system. The user must enter the specific access code associated with the burglar alarm to configure its settings.
Pre-conditions	•The user has successfully accessed the system.
•The user knows the specific access code for configuring the burglar alarm.
Event Flow	1.User selects the“Configure Burglar Alarm”option.
2.User enters the burglar alarm configuration code.
3.System validates the code.
4.If the code is valid, the user can configure the burglar alarm settings.
Post-conditions	If the code is valid, the user can configure the burglar alarm settings.
• If the code is invalid, the user is notified and unable to configure the burglar alarm.
Includes	None
Extensions	None
Triggers	Password Input Terminal


ID	uc1c
Actor	User (Staff)
Name	Configure Fire Alarm
Description	The “Configure Fire Alarm” use case involves the User configuring the fire alarm system after successfully accessing the system. The user must enter the specific access code associated with the fire alarm to configure its settings.
Pre-conditions	•	The user has successfully accessed the system.
•	The user knows the specific access code for configuring the fire alarm.
Event Flow	1.User selects the “Configure Fire Alarm” option.
2.	User enters the fire alarm configuration code.
3.	System validates the code.
4.	If the code is valid, the user can configure the fire alarm settings.
Post-conditions	•	If the code is valid, the user can configure the fire alarm settings.
•	If the code is invalid, the user is notified and unable to configure the fire alarm.
Includes	None
Extensions	None
Triggers	None


ID	uc1d
Actor	User ( Staff, criminal offender)
Name	Lock User Out and Sound Tamper Alarm
Description	The “Lock User Out and Sound Tamper Alarm” use case involves the system locking the User out of the system and triggering a tamper alarm sound if the user enters an incorrect access code three times consecutively.
Pre-conditions		The user has attempted to access the system with an incorrect access code three times consecutively.
Event Flow	1.	System detects the third consecutive incorrect access code attempt.
2.	System locks the user out of the system.
3.	System triggers a tamper alarm sound from the console speaker.
4.	User’s swipe card is disabled.
Post-conditions	The user is locked out of the system.
•	A tamper alarm sound is triggered.
•	User’s swipe card is disabled.

Includes	None
Extensions	None
Triggers	Password Input Terminal

2.Fire Alarm Operation

ID	uc2a
Actor	Fire Alarm System
•	Heat Sensors
•	Smoke Detectors
•	User (if pressing the fire alarm button)
Name	Trigger Fire Alarm
Description	The “Trigger Fire Alarm” use case involves the Fire Alarm System reacting to specific conditions that indicate a potential fire. The system can be triggered if any of the heat sensors detect a temperature greater than TC, if any smoke detectors detect smoke for a time greater than ‘Time Critical’, or if the fire alarm button is pressed.
Pre-conditions	•	The fire alarm system is active and operational.
•	Heat sensors and smoke detectors are functional and properly calibrated.
•	The fire alarm button is in working condition.
Event Flow	1.	Heat sensors detect a temperature greater than TC OR smoke detectors detect smoke for a time greater than ‘Time Critical’ OR a fire alarm button is pressed.
2.	The fire alarm system verifies the triggering condition.
3.	If the condition is met, the fire alarm is activated.
Post-conditions		The fire alarm is triggered, indicating a potential fire situatio
Includes		Automatic Summoning of Fire Brigade
	•	Activation of Fire Alarm Bells and Flashing Lights
Extensions		If the triggering condition is not met, the use case ends without activating the fire alarm.
Triggers	Heat sensors, Somke sensors, Fire alarm button


ID	uc2b
Actor	Fire Alarm System
•	Fire Brigade
Name	Automatic Summoning of Fire Brigade 
Description	The “Automatic Summoning of Fire Brigade” use case involves the Fire Alarm System automatically notifying the fire brigade when a fire is detected.
Pre-conditions	The fire alarm has been triggered due to detected fire conditions.
Event Flow	1.	The fire alarm system detects a fire based on the triggering conditions.
2.	The system activates the automatic calling system.
3.	The fire brigade receives the automatic notification.
Post-conditions	•	The fire brigade is informed and dispatched to the location of the fire.
Includes	None
Extensions	None
Triggers	None 


ID	uc2c
Actor	Fire Alarm System
Name	Activation of Fire Alarm Bells and Flashing Lights
Description	The “Activation of Fire Alarm Bells and Flashing Lights” use case involves the Fire Alarm System activating audible and visual signals throughout the building to alert occupants about the detected fire.
Pre-conditions	The fire alarm has been triggered due to detected fire conditions.
Event Flow	1.	The fire alarm system detects a fire based on the triggering conditions.
2.	The system activates fire alarm bells and flashing lights throughout the building.
Post-conditions	Audible alarm bells and visual flashing lights are active throughout the building, alerting occupants about the fire.
Includes	None
Extensions	None
Triggers	Fire alarm bell, Flashing lights, Fire door release solenoids

3.Resetting Fire Alarm

ID	uc3a
Actor	Authorized Personnel
Name	Stop Fire Alarm
Description	The “Stop Fire Alarm” use case involves Authorized Personnel interacting with the system to stop the fire alarm. To do so, the authorized personnel must input a fire disable code on the system console and swipe a valid card.
Pre-conditions	The fire alarm is currently active and sounding.
•	Authorized Personnel have access to the system console.
•	Authorized Personnel have a valid swipe card
Event Flow	1.	Authorized Personnel accesses the system console.
2.	Authorized Personnel enters the fire disable code.
3.	Authorized Personnel swipes a valid card on the console.
4.	System verifies the entered code and card.
5.	If the code and card are valid, the fire alarm is stopped, and the alarm sound ceases.

Post-conditions	The fire alarm is stopped and no longer sounding.
Includes	None
Extensions	If the entered code or card is invalid, the system does not stop the fire alarm, and an error message is displayed. The use case returns to the initial state, and the alarm continues to sound.
Triggers	Card reader，Password Input Terminal


4.Burglar Alarm Operation

ID	uc4a
Actor	Authorized Staff
Name	Set Activation Schedule
Description	The “Set Activation Schedule” use case involves the Authorized Staff interacting with the system to define specific activation times for the burglar alarm. Authorized Staff can set different activation and deactivation times for each day of the week or activate the system for a fixed number of days for continuous 24/7 protection during holidays.
Pre-conditions	Authorized Staff has access to the system.
•	The system is in a configuration mode.
Event Flow	1.	Authorized Staff selects the “Set Activation Schedule” option.
2.	Authorized Staff specifies activation and deactivation times for each day of the week or selects a fixed number of days for continuous activation.
3.	The system records the specified schedule.
Post-conditions	The burglar alarm system is configured with the specified activation schedule.
Includes	None
Extensions	None
Triggers	None


ID	uc4b
Actor	Door Sensor
•	Window Sensor
•	Floor Sensor
•	Panic Alarm Button
•	Burglar Alarm System
Name	Trigger Burglar Alarm
Description	The “Trigger Burglar Alarm” use case involves the Door Sensor, Window Sensor, Floor Sensor, and Panic Button triggering the burglar alarm under specific circumstances when the system is active. If a door is opened, a window is opened, floor sensor is triggered, or panic button is pressed while the system is active, the burglar alarm is activated.
Pre-conditions	•	The system is in an active state.
•	Sensors are functional and properly connected to the system.
Event Flow	1.Door Sensor detects an opened door OR Window Sensor detects an opened window OR Floor Sensor is triggered OR Panic Button is pressed.
2.System checks if it’s in an active state.
3.	If the system is active and any of the above events occur, the burglar alarm is triggered.
Post-conditions	The burglar alarm is triggered.
•	Warning sound and flashing lights are activated.
•	Message is sent to the police.
Includes	None
Extensions	None
Triggers	Door Sensor,Window Sensor, Floor Sensor, Panic alarm Button


ID	uc4c
Actor	Authorized Staff
•	Burglar Alarm System
Name	Configure Entry Points
Description	The “Configure Entry Points” use case allows Authorized Staff to designate specific doors as entry points. When these doors are opened while the system is active, an audio warning is issued, and a countdown begins. If the system is not deactivated before the countdown reaches zero, the burglar alarm will be triggered.

Pre-conditions	Authorized Staff has access to the system.
•	The system is in a configuration mode.
Event Flow	1.	Authorized Staff selects the “Configure Entry Points” option.
2.	Authorized Staff designates specific doors as entry points.
3.	An authorized user opens a designated door.
4.	System issues an audio warning and starts a countdown.
5.	If the system is not deactivated before the countdown ends, the burglar alarm is triggered.
Post-conditions	If deactivated before countdown ends, the system remains in an active state.
•	If not deactivated, the burglar alarm is triggered.
Includes	None
Extensions	None
Triggers	Door sensors

ID	uc4d
Actor	Authorized Staff
•	Burglar Alarm System
Name	Deactivate/Disable Alarm
Description	The “Deactivate/Disable Alarm” use case allows Authorized Staff to deactivate or disable the burglar alarm system. To do so, an authorized user must enter a code into the alarm console and present a valid swipe card.
Pre-conditions	•	Authorized Staff has access to the system.
•	The system is in an active state.
Event Flow	1.	Authorized Staff enters a deactivation/disabling code into the alarm console.
2.	Authorized Staff presents a valid swipe card.
3.	The system verifies the code and card.
4.	If the verification is successful, the burglar alarm system is deactivated/disabled.
Post-conditions	The burglar alarm system is deactivated/disabled.
Includes	None
Extensions	None
Triggers	Card reader, Password input terminal

ID	uc4e
Actor	Authorized Staff
•	Burglar Alarm System
Name	Configure Burglar Alarm
Description	The “Configure Burglar Alarm” use case allows Authorized Staff to configure various aspects of the burglar alarm system. Authorized Staff can use an alarm code to access the configuration settings.
Pre-conditions	Authorized Staff has access to the system.
•	The system is in a configuration mode.
Event Flow	1.	Authorized Staff selects the“Configure Burglar Alarm”option.
2.	Authorized Staff enters the alarm code.
3.	The system validates the alarm code.
4.	If the code is valid, Authorized Staff can configure burglar alarm settings.
Post-conditions	The burglar alarm system is configured according to the specified settings.
Includes	None
Extensions	None
Triggers	Password input terminal
5.Card readers

ID	uc5a
Actor	Users
Name	Authenticate for Configuration
Description	The “Authenticate for Configuration” use case involves Users interacting with the security system panel to authenticate themselves for system configuration purposes. Users must provide valid credentials to gain access to configuration settings.
Pre-conditions	•	Users intend to configure the security system.
•	Security System Panel is accessible.
Event Flow	1.	Users approach the Security System Panel.
2.	Users provide their authentication credentials (e.g., swipe card, enter access code).
3.	The Security System Panel verifies the credentials.
4.	If the credentials are valid, Users gain access to configuration options.
Post-conditions	•	If the credentials are valid, Users can configure the security system settings.
Includes	None
Extensions	If the provided credentials are invalid, Users are denied access to configuration options.
Triggers	Security System Panel

ID	uc5b
Actor	Users
Name	Access High Security Areas
Description	The “Access High Security Areas” use case involves Users using card readers on doors to verify their identity and gain access to high-security areas. Users must present a valid card to access these areas.
Pre-conditions	•	Users need access to high-security areas.
•	Doors with card readers are installed and operational.
Event Flow	1.	Users approach a door with a card reader.
2.	Users present their access card to the card reader.
3.	The card reader verifies the card’s authenticity.
4.	If the card is valid, the door is unlocked, and Users can enter the high-security area.
Post-conditions	If the card is valid, Users gain access to the high-security area.
Includes	None
Extensions	If the card is invalid or tampered with, the door remains locked, and Users are denied access to the high-secu
Triggers	Card reader

Task2
1. Compliance with Security Regulations (Regulatory Requirement):
   - Necessity: Adherence to applicable security regulations and standards is imperative.
   - Assessment: External security audits will assess conformity to these regulations and standards.

2. System Uptime (Reliability Requirement):
   - Necessity: The system must maintain operational status 99.9% of the time, not accounting for planned maintenance.
   - Assessment: Monitoring of system downtime and computation of uptime will serve as proof of reliability.

3. Access Request Response Efficiency (Performance Requirement):
   - Necessity: The system is required to process access requests in under two seconds for card readers and five seconds for alarm activations.
   - Assessment: Performance evaluations will be conducted to measure the response times to access requests.

4. Secure Data Transmission (Security Requirement):
   - Necessity: It is essential that data exchanges between system components utilize industry-recognized encryption methods.
   - Assessment: The employed encryption protocols will undergo testing and verification against standard benchmarks.

5. Card Reader Durability (Reliability Requirement):
   - Necessity: Card readers should demonstrate a minimum mean time between failures (MTBF) of 100,000 hours.
   - Assessment: Collection and analysis of MTBF data will determine adherence to this requirement.

6. System Compatibility (Compatibility Requirement):
   - Necessity: The system must exhibit compatibility with pre-existing security hardware and protocols.
   - Assessment: Compatibility trials will be executed to ensure integration with existing security infrastructure.

7. Hardware Integrity (Physical Requirement):
   - Necessity: The physical components of the system, such as card readers, must be resistant to tampering.
   - Assessment: Physical examinations and the presence of tamper-evident features will validate this resistance.

8. Mobile Application Efficiency (Usability Requirement):
   - Necessity: The mobile application used for managing the security system must display high responsiveness, loading within three seconds on both Android and iOS platforms.
   - Assessment: Performance tests on various mobile devices will confirm the application's efficiency.

9. Operational Resilience under Environmental Variations (Environmental Requirement):
   - Necessity: System components, including card readers and sensors, must function effectively within predetermined temperature and humidity ranges.
   - Assessment: Environmental tests will be employed to ensure component functionality under varied conditions.

10. Prompt Emergency Reaction (Safety Requirement):
    - Necessity: The system is required to initiate emergency protocols, such as alarms and notifications to authorities, within ten seconds following the detection of a critical security breach.
    - Assessment: The timeliness of emergency responses will be evaluated during simulated critical security incidents.
