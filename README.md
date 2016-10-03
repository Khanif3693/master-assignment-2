# Assignment #2
**Due at 4:59pm on Monday, 10/10/2016**

The goal of this assignment is to have you start working with the dynamic array data structure.  There are two parts to the assignment, outlined below.  Follow the instructions listed in each part, filling in and augmenting the appropriate places in the provided code, as requested.

## Part I

You are given a dynamic array implementation in `dynamicArray.c`. Currently, the array will grow to double the size when we add an item and it reaches capacity.  However, the array will never shrink.

Your task is to modify the given functions (do not modify the prototypes or create new functions) to shrink the array when a remove causes the size to be 1/3rd of the capacity.

Answer the following questions and place your answer in a new file `P1.txt` that you add, commit, and push to your GitHub repo.

1. Does `_dynArrSetCapacity`, as given, allow us to shrink the array? That is, can we call `_dynArrSetCapacity` with a capacity that is lower than the current capacity? If not, describe how the function fails when we attempt to resize to a smaller capacity.

2. What functions in the dynamic array need to be modified to allow the it to be resized to a smaller capacity on remove?

3. The code also has an stack interface that uses a dynamic array. While `topDynArr` and `pushDynArray` call existing dynamic array functions to achieve their goals, `pushDynArray` directly modifies the struct itself.  This is known as breaking encapsulation - what is the disadvantage of doing this? (Hint: See question 2)

Now, modify `dynamicArray.c` so that it correctly resizes the array as described above. When you make a change to a function please put a comment like so

`// PART I: <description of change>`

There is an additional file called `testDynArray.c` you may use to test your solution, it is highly recommended that you do additional testing!

## Part II

Complete the functions in `stack_exercise.c`.  The comments contain further details about how to implement each.  You may test your code in `testExercise.c` file.

## Grading criteria

Your assignment will be graded by compiling it on `flip.engr.oregonstate.edu` using the provided `Makefile`, so make sure you have tested your work under those conditions.

The assignment is worth 100 points total.

* Part I: 50 points
  * 10 points each: questions 1, 2, and 3 in `P1.txt`
  * 20 points: correctly implements array shrinking as described above
* Part II: 50 points
  * 25 points: correctly implements `in_stack()`
  * 25 points: correctly implements `valid_bracket()`

## Submission

We'll be using GitHub Classroom for this assignment. You will submit your assignment via GitHub. Just make sure your completed files are committed and pushed by the assignment's deadline to the `master` branch of the GitHub repo that was created for you by GitHub Classroom.
