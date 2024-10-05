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
5. Nextly will using the fork method to create each of the 4 processes and then once their made will call each of these functions to increment their "total" value
6. Then will use a for loop to go through each child process to print out their "total and "ID" value while also using the wait function to make sure the parent go's after the children
7. Then will use 2 if statements to detach the shared memory and remove it ![assignment1ss2](https://github.com/user-attachments/assets/a3938c1c-2f42-4dd2-b695-81f320e37d83)

# 4. Testing the Project
To see if the project works within the given constraints will run it multiple times to see if the project is both formatted correctly and runs within the order we want.
![assignment1ss3](https://github.com/user-attachments/assets/35f07eac-8353-4b4b-947d-2bebbb7bd6bd)

For this project we did 4 sample runs, from this we can draw some conclusions on our project. For one the project executes correctly, the counter is updated throughout the project (except for process 1), we see the ID print out, the format is correct, and the parent process is executed last. We also the value of the ID for each process is different which is good, because if it wasn't that means the processes wouldn't be executed. Same thing for the counter if the counter was the same wasn't roughly within the same range that means that the shared memory wouldn't be getting released. So our program is working properly, some things we can note is that the process counter isn't increment for process 1 and that they don't terminate in order. This is due the way that the stall of the processes for the execution is taking place which isn't going to be perfect.

# 5. Conclusion
In conclusion we see the project follow the constraints giving and represent the concept of forking and using shared memory between processes accurately.
