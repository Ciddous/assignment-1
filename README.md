# Programming Project 1
Colin Jones
CS3113
10/5/2024
# 1. Introduction
In this project we will create 4 processes, what is special about it is each processes will have a shared memory through the local variable "total". After each process is create we will increment value inside of each process by either 100,000, 200,000, 300,000, or 500,000 and then print out its value. Once all the processes have finished the parent of these process will release the shared memory and wait until all the children proceess finished. After the child gets executed it will print out its ID.

# 2. Expected Output
The output of this project is supposed to look like the following format

Sample output
From Process 1: counter = 270547.
From Process 2: counter = 347860.
From Process 3: counter = 400001.
From Process 4: counter = 500000.
Child with ID: 2412 has just exited.
Child with ID: 2411 has just exited.
Child with ID: 2413 has just exited.
Child with ID: 2415 has just exited.
End of Simulation.

# 3. Project Implementation
To implement the project with the following constraints we will need to follow the steps below
1. First we need to define a key for shared memory used SHMKEY
2. Will define a  structure for the shared memory that will hold value "total"
3. Will create 4 seperate functions that each will be used after the processes are created to increment "total"
4. Will create 2 seperate if statements to create the shared memory segement and attach it to the process's address space![assignment1ss1](https://github.com/user-attachments/assets/4121975d-edbe-4537-9fea-9b7ecce59c67)
