## Table of contents
* [Author Info](#author-info)
* [Problem Statement](#problem-statement)
* [Technique To Solve Promblem](#technique-to-solve-promblem)
* [Setup](#setup)
* [Known Bugs](#known-bugs)
* [References](#references)
* [Worked With](#worked-with)

## Author Info
Name: Shrey Patel
V#: V00900319
Course: CSC 360
Section: A1
Assignment#: 2
Part#: 3

## Problem Statement
This project solves "The Dining Philosopher Problem", which states that K philosophers seated around a circular table with one chopstick between each pair of philosophers. There is one chopstick between each philosopher. A philosopher may eat if he can pickup the two chopsticks adjacent to him. One chopstick may be picked up by any one of its adjacent followers but not both.
	
## Technique To Solve Promblem
This problem can be solved using "Semaphore". Each philosopher is represented by the following pseudocode:

```
process P[i]
   while true do
      {  THINK;
         PICKUP(CHOPSTICK[i], CHOPSTICK[i+1 mod 5]);
         EAT;
         PUTDOWN(CHOPSTICK[i], CHOPSTICK[i+1 mod 5])
      }
```

There are three states of philosopher : THINKING, HUNGRY and EATING. Here there are two semaphores : Mutex and a semaphore array for the philosophers. Mutex is used such that no two philosophers may access the pickup or putdown at the same time. The array is used to control the behavior of each philosopher. But, semaphores can result in deadlock due to programming errors.

## Setup
To run this project, follow below given steps:

```shell
$ cd ../Project_Directory
$ make
$ make run
$ make clean
$ clear
```

## Known Bugs
N/A

## References
* https://en.wikipedia.org/wiki/Dining_philosophers_problem 
* https://www.geeksforgeeks.org/dining-philosopher-problem-using-semaphores/

## Worked With
* Amee Gorana (V#: V00882943)