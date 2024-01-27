COMP1811 CW1 Python Project due 22/01/2024

Authors: Aleksandar Bozov(Partner A/Responsible for F1), Peter Yovchev(Partner B/Responsible for F2)

Description: This is our submission for COMP1811 CW1 for Python assigned to us. It is a real time simulation of an supermarket lane checkout system
with its own integrated GUI. We believe it meets all the features requested in the specification, as well as in terms of quality standards

THIS PROJECT ALSO INCLUDES OUR SUBMISSION FOR LOGBOOK TASK 1. PETER YOVCHEV DID SUBFEATURE V DISPLAY CUSTOMER BASKET CONTENT,
AND ALEKSANDAR BOZOV DID LANE DISPLAY. BUTTONS ARE IN THE GUI CLASS, AND WHOEVER DID WHAT WAS INCLUDED IN THE COMMENTS

SINCE WE ALREADY ADDED A GUI FOR THE SIMULATION BEFORE THE LOGBOOK TASKS WERE GIVEN, WE DECIDED TO PUT BOTH FEATURES IN THE 
SAME WINDOW INSTEAD OF SEPARATE ONES

The simulation is ran from GUI.py

Files:

README.txt <------
CustomerClass.py = contains AbstractCustomer and CustomerClass
LanesClass.py = contains Lane, RegularLane and SelfCheckout classes respectively
AllLanes.py = contains code for AllLanes class 
AllCustomer.py = contains code for AllCustomer class 
Events.py = contains code for the Events class
SimulationClass.py = contains code for the Simulation class
GUI.py = contains code for the GUI class, and the simulation is ran from there


Classes in the simulation:
AbstractCustomer = an abstract class from which you can derive a base from which you can build customer classes from
Customer = A customer class which is designed to represent the average customer in the simulation
AllCustomer = a class which allows a centralised control of Customer class instances
Lane = A abstract base lane class from which you can build different lane classes
RegularLane = designeed to represent a regular traditional lane in a supermarket
SelfCheckout = a class designed to represent a self checkout section in a supermarket
AllLanes = a class designed to bundle SelfCheckout and RegularLane instances, and allow for a more centralised control of lane instances
Events = A class designed to bundle AllCustomer and AllLanes classes and allow for the creation of methods which will act as events in the simulation.
Simulation = where the simulation is triggered
GUI = GUI class integrates the simulation with a tkinter window, allowing for more user interactivity

Basic Code Logic:

-Customer Class instances are meant to represent the average customer in the simulation
-Lane Classes, both SelfChekcout and RegularLane, are meant to represent lanes in a supermarket, where customer can go and check out
-AllLanes and AllCustomer classes's use is to provide a more centralise way to control lane and customer instances, significantly simplifying code
-Events Class bundles AllCustomer and AllLanes classess, and allows for more centralised control and behaviors to be placed upon them, as well as easier time implementing interaction between customer and lanes
-From the simulation class, the simulation is ran with the use of a while loop continually iterating events (methods from the Events class) until the loop is broken. The for loop gives
an illusion of 
-And from the GUI class, the simuatlion is integrated with a GUI, which allows for better user experience and interactivity
