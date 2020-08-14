# ALGORITHM
An algorithm is a set of well-defined instructions in sequence to solve a problem.

## Qualities of a Good Algorithm

    1. Input and output should be defined precisely.
    2. Each step in the algorithm should be clear and unambiguous.
    3. Algorithms should be most effective among many different ways to solve a problem.
    4. An algorithm shouldn't include computer code. Instead, the algorithm should be written in such a way that it can be used in different programming languages.

## Examples Of Algorithms In Programming
**WRITE AN ALGORITHM TO ADD TWO NUMBERS ENTERED BY THE USER.**

    Step 1: Start.
    Step 2: Declare variables num1, num2 and sum.
    Step 3: Read values num1 and num2. 
    Step 4: 
            Add num1 and num2 and assign the result to sum.
            sum←num1+num2
    Step 5: Display sum
    Step 6: Stop


**WRITE AN ALGORITHM TO FIND THE LARGEST AMONG THREE DIFFERENT NUMBERS ENTERED BY THE USER.**

    Step 1: Start
    Step 2: Declare variables a,b and c.
    Step 3: Read variables a,b and c.
    Step 4: 
        If a > b
           If a > c
              Display a is the largest number.
           Else
              Display c is the largest number.
        Else
           If b > c
              Display b is the largest number.
           Else
              Display c is the greatest number.  
    Step 5: Stop

**WRITE AN ALGORITHM TO FIND THE FACTORIAL OF A NUMBER ENTERED BY THE USER.**

    Step 1: Start
    Step 2: Declare variables n, factorial and i.
    Step 3: 
          Initialize variables
          factorial ← 1
          i ← 1
    Step 4: Read value of n
    Step 5: 
           Repeat the steps until i = n
           5.1: factorial ← factorial*i
           5.2: i ← i+1
    Step 6: Display factorial
    Step 7: Stop

**WRITE AN ALGORITHM TO CHECK WHETHER A NUMBER ENTERED BY THE USER IS PRIME OR NOT.**

    Step 1: Start
    Step 2: Declare variables n, i, flag.
    Step 3: 
           Initialize variables
           flag ← 1
           i ← 2  
    Step 4: Read n from the user.
    Step 5: 
           Repeat the steps until i=(n/2)
           5.1 If remainder of n÷i equals 0
                flag ← 0
                Go to step 6
           5.2 i ← i+1
    Step 6: 
           If flag = 0
              Display n is not prime
           else
              Display n is prime
    Step 7: Stop

**WRITE AN ALGORITHM TO FIND THE FIBONACCI SERIES TILL TERM≤1000.**

    Step 1: Start 
    Step 2: Declare variables first_term,second_term and temp. 
    Step 3: Initialize variables first_term ← 0 second_term ← 1 
    Step 4: Display first_term and second_term 
    Step 5: 
           Repeat the steps until second_term ≤ 1000 
           5.1: temp ← second_term 
           5.2: second_term ← second_term + first_term 
           5.3: first_term ← temp 
           5.4: Display second_term 
    Step 6: Stop
    
## What are Algorithms?

Informally, an algorithm is nothing but a mention of steps to solve a problem. They are essentially a solution.

For example, an algorithm to solve the problem of factorials might look something like this:

**Problem: Find the factorial of "n"**

    Initialize fact = 1
    For every value v in range 1 to n:
         Multiply the fact by v
    fact contains the factorial of n
    
Here, the algorithm is written in English. If it was written in a programming language, we would call it to code instead. Here is a code for finding the factorial of a number in C.

    int factorial(int n) 
    {
        int fact = 1;
        for (int v = 1; v <= n; v++) 
        {
            fact = fact * v;
        }
        return fact;
    }
    
Programming is all about data structures and algorithms. Data structures are used to hold data while algorithms are used to solve the problem using that data.

Data structures and algorithms (DSA) goes through solutions to standard problems in detail and gives you an insight into how efficient it is to use each one of them. It also teaches you the science of evaluating the efficiency of an algorithm. This enables you to choose the best of various choices.

## Examples of an Algorithm's Efficiency

Here are some examples of what learning algorithms and data structures enable you to do:

**Example 1: Age Group Problem**

Problems like finding the people of a certain age group can easily be solved with a little modified version of the binary search algorithm (assuming that the data is sorted).

The naive algorithm which goes through all the persons one by one, and checks if it falls in the given age group is linearly scalable. Whereas, binary search claims itself to be a logarithmically scalable algorithm. This means that if the size of the problem is squared, the time taken to solve it is only doubled.

Suppose, it takes 1 second to find all the people at a certain age for a group of 1000. Then for a group of 1 million people,

- the binary search algorithm will take only 2 seconds to solve the problem
- the naive algorithm might take 1 million seconds, which is around 12 days

The same binary search algorithm is used to find the square root of a number.

**Example 2: Rubik's Cube Problem**

Imagine you are writing a program to find the solution of a Rubik's cube.

This cute looking puzzle has annoyingly 43,252,003,274,489,856,000 positions, and these are just positions! Imagine the number of paths one can take to reach the wrong positions.

Fortunately, the way to solve this problem can be represented by the graph data structure. There is a graph algorithm known as Dijkstra's algorithm which allows you to solve this problem in linear time. Yes, you heard it right. It means that it allows you to reach the solved position in a minimum number of states.

**Example 3: DNA Problem**

DNA is a molecule that carries genetic information. They are made up of smaller units which are represented by Roman characters A, C, T, and G.

Imagine yourself working in the field of bioinformatics. You are assigned the work of finding out the occurrence of a particular pattern in a DNA strand.

It is a famous problem in computer science academia. And, the simplest algorithm takes the time proportional to

    (number of character in DNA strand) * (number of characters in pattern)

A typical DNA strand has millions of such units. Eh! worry not. KMP algorithm can get this done in time which is proportional to

    (number of character in DNA strand) + (number of characters in pattern)

The  *  operator replaced by  +  makes a lot of change.

Considering that the pattern was of 100 characters, your algorithm is now 100 times faster. If your pattern was of 1000 characters, the KMP algorithm would be almost 1000 times faster. That is, if you were able to find the occurrence of pattern in 1 second, it will now take you just 1 ms. We can also put this in another way. Instead of matching 1 strand, you can match 1000 strands of similar length at the same time.
