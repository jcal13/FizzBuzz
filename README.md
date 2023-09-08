# CSC207 Course Notes - Fizz Buzz

Let's start off our exploration of Java with a classic programming challenge, Fizz Buzz!

## Fizz Buzz

Fizz Buzz is a game where people sit in a circle. Counting from 1 and going around the circle, people say one of four things for a number `i`:


we must create different outputs based on a number we continually increment. It is a classic technical interview question.
Print
Let `i` be a number; output the following:

* If `i` is divisible by 3, print 'Fizz'
* If `i` is divisible by 5, print 'Buzz'
* If `i` is divisible by 3 and 5, print 'Fizz Buzz'
* Otherwise, print the value of `i`

So, starting with `i = 1` and counting until `i = 6` we would get:

```
1
2
Fizz
4
Buzz
Fizz
```

## A Java version

```java
/**
 * Solve the FizzBuzz challenge.
 */
class FizzBuzz {

    public static void main(String[] args) {

        for (int i = 1; i < 100; i++) {

            // Find out which numbers divide i.
            boolean divisibleBy3 = i % 3 == 0;
            boolean divisibleBy5 = i % 5 == 0;

            // Print our appropriate result.
            if (divisibleBy3 && divisibleBy5) {

                System.out.println("Fizz Buzz");

            } else if (divisibleBy3) {

                System.out.println("Fizz");

            } else if (divisibleBy5) {

                System.out.println("Buzz");

            } else {

                System.out.println(i);

            }
        }
    }
}
```

This program (which you should run for yourself right now; open Lab1/src/FizzBuzz
in the top left of this
window and click the Run button) prints out the first 100 numbers of Fizz Buzz.
You may never have seen Java before, but we bet you can puzzle out how it works.
Take a minute and read this through and take guesses at what different pieces of
the code do. For example, what's the Java version of Python's `and`? What's going
on with that weird `for` loop?

## The Main Function

In Python, any code that you write in a file will get run when you execute the file.
This is not the case in Java. You must define a method called `main` in a class
and tell Java ot run the file containing that class.

```java
public static void main(String[] args)
```

This is the main method, the entry point of your program. You have installed Java,
and it is a program that knows how to compile and run your program — it calls
method `main` in the file you choose to run.

Later in this course, you'll learn what all that mess means.

## Rewrite this using `while`

You've puzzled through how Java `for` and `if` statements work. Rewrite this
to use a `while` loop instead of a `for` loop.

## How to test it

How do you know that it's correct? Part of the problem here is that we can't
easily test this program. The iteration and the calculation are tightly coupled.
If we refactored this by extracting the body of the loop into a method, we could
test the calculation for several interesting numbers.

## How to refactor it

Select all the lines inside the body of the loop. Don't include the for/while
line or the closing brace `}` of the loop.

Now select menu item

    Refactor —> Extract/Introduce —> Method…

Immediately, type the method name you want, maybe something like `doFizzBuzz`.  Rerun the program to verify.

That's your first big IntelliJ trick! There are lots more.

# Technical interviews  (and Java practice)

Technical interviews for developer internships often have you write
some code. It usually uses first- and second-year material, and many students
practice these kinds of problems regularly over the academic year.

For this week's homework, you'll solve two of them.

## Multiples of 3 and 5

Right-click on `src` and select `New —> Java Class`. Name it `Multiples`.

We're looking for non-negative multiples of 3 or 5. The first four are 3, 5, 6, and 9, so there are
four below 10. How many are below 1000?

In `Multiples.java`, write a main program that prints how many multiples of 3 or 5 there are below 1000.
Add this file to your project, commit, and push. If you don't get the right answer, that's okay!
This is to get you to practice.


## Multiples of 3 and 5

Right-click on `src` and select `New —> Java Class`. Name it `Multiples`.

We're looking for non-negative multiples of 3 or 5. The first four are 3, 5, 6, and 9, so there are
four below 10. How many are below 1000?

In `Multiples.java`, write a main program that prints how many multiples of 3 or 5 there are below 1000.
Add this file to your project, commit, and push. If you don't get the right answer, that's okay!
This is to get you to practice.

## Reduce a number to 0

Right-click on `src` and select `New —> Java Class`. Name it `Reduce`.

Starting with a number n, if n is even divide it by 2. If n is odd, subtract 1. Repeat.

if you start with n = 2, the answer is 2:

```
2 (even, divide by 2)
1 (odd, subtract 1)
0
```

In `Reduce.java`, write a main program that prints how many steps it takes to reach 0 if you start at 100.
Add this file to your project, commit, and push. Again, if you don't get the right answer, that's okay!

## Further practice

[LeetCode](https://leetcode.com) is a very popular source of practice problems.
[CoderByte](https://www.coderbyte.com/) is another. 
If you want an internship, we recommend that you register and practice these problems over the year.