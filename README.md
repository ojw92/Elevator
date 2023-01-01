# Elevator
elevator project

This project was motivated by my personal unsatisfactory experience with the elevator at my apartment. I will attempt to develop a more efficient algorithm using the parameters that I consider to be essential in optimizing wait time & travel time for the user(s) involved.

Points to consider:
 - time for elevator to stop at a floor, open door & close door
 - time for elevator to move from one floor to the next
 - time from starting floor to next floor as it accelerates & 2nd to last floor to last floor as it deccelerates
 - for simplicity of problem, assume electrical energy spent & durability of equipment are negligible
 - define "window of usage" (WoU or simply window) as the duration between the start of waiting for the elevator (pressing the button at the initial floor) and end of the elevator travel (opening of the elevator door for exit)

Problem statement:
Minimize wait time & travel time for users in the same "window of usage"
 1. what is the maximum difference in floors between 2 ppl for an elevator to choose to pick up the person on the higher floor, then the lower floor, and still be efficient?
 2. (For 2 elevators) What is the minimum difference in floors between 2 ppl for elevator 1 to choose person 1 over person 2 so elevator 2 can stop at person 2?
 3. How can the algorithm be designed to prioritize different goals (time-efficient (person-centric), energy-efficient (machine-centric), philanthropic, etc)?




Currently in progress for ironing out the details of the algorithm. More to come!
