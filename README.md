# Elevator
elevator project

This project was motivated by my personal unsatisfactory experience with the elevator at my apartment. I will attempt to develop a more efficient algorithm using the parameters that I consider to be essential in optimizing wait time & travel time for the user(s) involved.


Problem Statement:
Minimize wait time & travel time for users in the same "window of usage"
 1. For a single-elevator apartment, what is the maximum difference in floors between 2 ppl for an elevator to choose to pick up the person on the higher floor, then the lower floor, and still be efficient?
 2. For 2 elevators, what is the minimum difference in floors between 2 ppl for elevator 1 to choose person 1 over person 2 so elevator 2 can stop at person 2?
 3. How can the algorithm be designed to prioritize different goals (time-efficient (person-centric), energy-efficient (machine-centric), philanthropic, etc)?


Points to consider:
 - time for elevator to stop at a floor, open door & close door
 - time for elevator to move from one floor to the next
 - time from starting floor to next floor as it accelerates & 2nd to last floor to last floor as it deccelerates
 - for simplicity of problem, assume electrical energy spent & durability of equipment are negligible
 - define "window of usage" (WoU or simply 'window') as the duration between the start of waiting for the elevator (pressing the button at the initial floor) and end of the elevator travel (opening of the elevator door for exit)


Constraints & constants:
Time it takes for a door to accommodate a stop (values as close to measured values as possible)
 - given x_0 as departure point, x_f as destination, and x_(f-k) as every floor in between travel, where k is an integer that is 0 < k < f
 - assume it takes 1.5 seconds to travel in between floors that are not adjacent to x_0 & x_f, i.e. x_(f-k)
 - assume it takes 3 seconds to travel into the destination floor to zero velocity (x_0 -> x_1) and 4.5 seconds to travel out of the departure point from zero velocity to its adjacent floor (x_(f-1) -> x_f)
 - assume it takes the door 4.5 seconds to fully open and 4 seconds to fully close, and that there is a 6.5-second duration in between when the door remains open
 - assume that once a person enters the elevator at the departure point, he/she does not hold the door open, simply presses the button for the destination floor and waits until he/she arrives
 - 


Stages of elevator travel:
1. press the button from starting floor (x_0)
2. wait for the elevator to travel along intermediate floors (x_(f-k))
3. wait for the elevator to travel into starting floor and deccelerate to a full stop 
4. wait for the door to open, enter, press the button to the destination floor, and wait for the door to close automatically (assuming the 'close door' button does not work)
5. wait for the elevator to travel along intermediate floors (x_(f-k))
6. wait for the elevator to travel into destination floor and deccelerate to a full stop
7. wait for the door to open and exit the elevator (x_f)







Currently in progress for ironing out the details of the algorithm. More to come!
