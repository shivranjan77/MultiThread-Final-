# MultiThread-Final-



Write a multithreaded program that calculates various statistical values for a list of numbers.
This program will be passed a series of numbers on the command line and will then create three separate worker threads. 
One thread will determine the average of the numbers, the second will determine the maximum value, and the third will determine the minimum value.
For example, suppose your program is passed the following integers as input (assuming a.out is your program):

a.out 90 81 78 95 79 72 85

The program will report:

The average value is 82
The minimum value is 72
The maximum value is 95

The variables representing the average, minimum, and maximum values will be stored globally. 
The worker threads will set these values, and the parent thread will output the values once the workers have exited.

Program Notes:This works because the parent and child processes have their own copies of the data. 
 The program perfoms fork(), then enters into a if loop and if pid == 1 (if it is busy) then it waits till it equals 0 (not busy).
 When it is 0 then it can perform the calculations. It checks to see if it is even or odd and performs the appropriate equation. 
 This repeats until it reaches one, then it breaks out of the loop.
 To start the program: To Complie write on terminal <gcc multithreads.c -lpthread> without<>  
 To run the assignment go to the terminal and find the directory that contains
 the compiled multithreads file. To run the multithreads program, type <./a.out> <(int) arguments with spaces between them> //without <> //
 The program immediately responds with calculations after it is ran and given its arguments.
    
