# Week 4 Lab Report: Debugging
## By Jerry Gong

## **Code Change #1**
Show a screenshot of the code change diff from Github:

![image](2pic1.png)
Link to the test file for a failure-inducing input that prompted you to make that change:

[test2.md](https://github.com/JGong7/markdown-parse/edit/main/test2.md)

Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)

![image](2pic2.png)

Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.
In the failure-inducing input, there is a link and an image. With our initial purpose, we wanted to only print the link. The symptom in this failed case is that the command-line output included the image name, which was not wanted. The bug was that the code does not check if there exists an exclamation mark before the open bracket in order to distinguish between image and link formats. 
## **Code Change #2**
Show a screenshot of the code change diff from Github (a page like this)
Link to the test file for a failure-inducing input that prompted you to make that change
Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.
## **Code Change #3**
Show a screenshot of the code change diff from Github (a page like this)
Link to the test file for a failure-inducing input that prompted you to make that change
Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.
