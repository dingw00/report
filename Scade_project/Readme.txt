Longitudinal Flight System

Group Members: 

Wendi Ding
Maanasa Sachidanand

The report involves the design of the longitudinal flight system that allows the pilot to direct the aircraft according to the altitude and helps in landing and take-off. 

SystemPA is the longitudinal flight system and it constitutes four subsystems:

1.	Calculs

This sub system involves the calculation of the flight parameters such as altitude of flight, speed of aircraft, vertical speed, density of air and slope of flight in degree.

2.	Alarms

This sub system involves design of three alarms namely stall, crash and descent. The stall alarm is triggered when incidence value is greater than the 12 degrees. The crash alarm is triggered when the landing gear is extended when altitude is less than 300 m. The descent alarm is triggered when the vertical speed is greater than 100 m/s. The alarms are activated only after confirmation time of 0.1 sec.

3.	Controls

The flight controller subsystem involves controlling the position of elevator within -0.4 m and 0.4 m and linearly varying the elevators according to the stick position. The stick positions are limited to values between -15 and 15 degrees.

4.	AutoPilot

This subsystem involves the design of state machine with IDLE state being the initial state which is activated when the pilot does not switch ON the autopilot button. The CTRL state is active when the autopilot button is switched ON and it transitions to other states namely ClimbMode state, DescentMode state and CruiseMode state depending on the altitude of flight.

Two scenario files are included:
TestScenario1: This scenario triggers stall, crash and descent alarms respectively. It performs an flight envelope of take off and landing at low altitudes (h < 8000 m).
TestScenario2: This scenario simulates the ascending process of the aircraft at high altitudes (h > 8000 m) in order to cover all the autopilot state machine conditions and the air density calculator conditions.

The Model Test Coverage achieved 100% test results.

There were three properties that were evaluated for formal proof validation.
Property 1: The stall alarm cannot be triggered if incidence is less than or equal to 12 degrees.
Property 2: The crash alarm cannot be triggered if altitude is greater than or equal to 300 m or landing gear is extended.
Property 3: The descent alarm cannot be triggered if vertical speed is less than or equal to 100 m/s.

All the above-mentioned properties are verified.























































