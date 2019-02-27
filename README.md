# VectorRouting
  - Name: Adam Hudson
  - Class: CSE 4344 Computer Networks
  - Assignment: Lab 2 Distance vector routing programming assignment
  
## Instructions on how to run code:
I developed my code on linux with Oracle Java(TM) SE Runtime Environment (build 1.8.0_144-b01). I have included input.txt to test the code with. The code will work with any file you give it as long as the file follows the same format as the one described in the lab description.

## The way my code is run is like so:
```
$ javac vector/routing/*.java 
$ java vector.routing.VectorRouting input.txt
```
- The code can run with any filename you give it. It does not have to be "input.txt". After the code is running, simply follow the command line interface to use the program

## Assumptions made:
I assumed that there would a max input file length of 24 as there would only be a max of 6 routers with 4 connections each. The program will not accept a file that is longer.  I also assumed that the file would follow only one format of the three columns by space delamination.

## Observations:
According to my program and how it performs the distance vector routing, the algorithm runs 3 times and takes about 1 millisecond to complete and reach a stable state on the input file provided in the lab description. Stable state means that the other routers do not need to update their tables based on their current links to each other. My program will detect the first time no tables have been updated and call the system stable. It is interesting to see how fast the process is. It would seem that the routers can reach a stable state so quickly due to the fact that they are all sharing information to each other. By doing this, the router information spreads easily to every router. The reason I think the program only too one millisecond to complete is due to the speed of modern processors. I do not think there was very much data to compute and therefore finished very quickly. The program also is able to overcome broken links as long as there is another way for that router to connect through another router. It make take longer than it would have, but it is very interesting too see how the algorithm tackles that issue.
