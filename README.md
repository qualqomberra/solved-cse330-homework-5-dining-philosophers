Download Link: https://assignmentchef.com/product/solved-cse330-homework-5-dining-philosophers
<br>
<strong>1.Dining Philosophers Problem:</strong>

Using the semaphores you have implemented, detect deadlocks in Dining Philosophers problem.




<strong>2.Test case:</strong>

The first line of the test case contains two numbers

A,B

A is the number of philosophers, and B is the number of entries coming after the first line

The number of chopsticks is the same as number of philosophers

Your program should have an array of semaphores where each semaphore (each element of the array) corresponds to each chopstick.

Each philosopher gets access to “the right” chopstick by doing

P(Sem[(philosopher ID – 1)% (number of Chopsticks)])

Then yields to the next philosopher

When the philosopher comes back the philosopher attempts to access “the left” chopstick by doing

P(Sem[philosopher ID % (number of Chopsticks) ])

Then yields to the next philosopher

When it comes back it prints

Printf(“
 Philosopher %d is eating 
”, philosopher ID);

Then it releases the right chopstick by doing

V(Sem[(philosopher ID – 1)% (number of Chopsticks)])

Then it releases the left chopstick by doing

V(Sem[(philosopher ID)% (number of Chopsticks)])

Then it deletes itself from the readyQ.

Then it yields to the next philosopher







The next B lines has philosopher numbers in order to populate the Ready Queue.

The program starts with the first element of the Ready Queue.




Test case example

4,2

1

3

Output

Philosopher 1 is eating

Philosopher 3 is eating




Test case example 2

4,2

1

2

Output

Philosopher 2 is eating

Philosopher 1 is eating




Your project must consist of 5 files




<ol>

 <li>h (uses ucontext.h)</li>

</ol>




<ol start="2">

 <li>h (includes TCB.h)</li>

</ol>




<ol start="3">

 <li>h (includes q.h)</li>

</ol>




<ol start="4">

 <li>h (includes threads.h) if you have written one.</li>

</ol>




<ol start="5">

 <li>proj-5.c (includes threads.h)</li>

</ol>

(make sure the compile command, “gcc proj-5.c” does the correct compilation).




All 5 files are to be ZIPPED into one zip file and uploaded in Canvas. The name of this file should reflect the name of the student (abbreviated, do not make it too long).




<strong>Note: Grading is on Ubuntu. It is in your interest to make sure the program compiles and runs in the target test platform.</strong>

<strong> </strong>




<strong>Testing your code on grading test cases</strong>

Grading test cases are different from the test cases provided.

To test your code against grading testcases follow these steps:




Put the four files q.h tcb.h threads.h and proj-5.c in one zip file and name the file  YOUR LAST NAMEProject5.zip (no gaps)




Make sure you do not have a folder inside your zip. When we unzip we should only have the files not a folder.




For example BanerjeeProject5.zip


