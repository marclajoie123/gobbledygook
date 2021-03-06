title: Consolidated Problem Sets 3 and 4, Spring 2020
tags: psets
date: 2020-03-07

This problem set is worth 55% of the grade in this course. It is due on Friday, May 8, at 5pm, via email to Diana Dewalle. 

**How to turn in this problem set**: As before, please turn in all your code, and, if you have any prose to write, your prose (formatted as markdown cells), for all of the problems in a single Jupyter Notebook file, entitled `lastname_ps1.ipynb` (obviously with your last name), which you will turn in to the dropbox on ICON.  **The filename should be the only place with your name in it.** Diana Dewalle will anonymize the files by replacing the name with a number before sending them to me to grade.

For each of the problems, you need not package all of your code in a single function. For example, you may write helper functions, import libraries outside of your function, etc.  However, you must turn in a single Jupyter Notebook file with all the code that makes your functions work as well as the functions themselves.  I expect to be able to run all the cells in the notebook you turn in, and, at the end, have a working function for each problem, so that I can call those functions with appropriate input and get the correct result. In all cases, your functions should return `None` if they receive inappropriate input.

## HONOR CODE

Each student must agree to the following honor code; if you do not agree to this honor code, do not turn in this problem set and drop the course.

*I will not solicit, receive, or provide any unauthorized assistance on this or any problem set in this course. I understand that unauthorized assistance includes seeing the work of any other student, including code, calculations, data analysis, or answers to problems. Students are permitted to discuss their general strategies for solving problems with one another, help one another understand lesson material or documentation for Python libraries, and the like, or other conversation short of sharing actual answers, calculations, data analysis, or code. Students are not permitted to seek or receive assistance or advice whatsoever from any person not enrolled in this course---this prohibition includes asking for help on public online forums such as stackoverflow.com, although students are free to search such websites and learn from preexisting discussions in which they are not participants.*

*If I have any doubt about the permissibility of any kind of assistance, I will seek a ruling from the professor. I will report any violations of this honor code of which I am aware. Violating this honor code is grounds for immediate disenrollment from this course, or other sanctions as provided for by College of Law and University policy on academic dishonesty.*

# Part 1 (Former Problem Set 3)

## Problem 1 (50 points)

In your data folder is a file named "executions.csv."  It is a dataset covering executions in the United States.  There is also a dataset named "StandYourGround.csv" which is a dataset covering cases in which people raised Stand Your Ground law defenses.

### 1.a (10 points)

Read McCleskey v. Kemp, 481 U.S. 297 (1987).  Does the executions.csv dataset you've been provided support or undermine the overall theory of discrimination in that case?  Explain why.

### 1.b. (40 points)

Using regression analysis, defend a conclusion as to whether the Stand Your Ground dataset includes evidence of racial discrimination.  

Note, because you have a binary dependent variable, you will probably want to use logistic regression, a variation on regression analysis that just uses a slightly different equation, but otherwise works the same.  We've mentioned this in class but haven't dug in; for present purposes you can just swap logistic regression code in for linear regression code following [this tutorial online](http://blog.yhat.com/posts/logistic-regression-python-rodeo.html). 

## Problem 2 (50 points) 

Consider the following Mystery Code, which is buggy: 

```python

def mystery_math_01(x, y, z):
    return x * y / z

def mystery_math_02(alpha, bravo, charlie):
    return (alpha * bravo) + (charlie * 1 - bravo)

def mystery_function(kevin, joe, nick):
    lizzo = mystery_math_02(kevin, nick, 1 - joe)
    return mystery_math_01(kevin, nick, lizzo)

```

the names are deliberately nonsensical.

## 2.a. (25 points) 

What is `mystery_function` trying (but currently failing) to do?  Explain. 

## 2.b. (25 points)

Fix the bug in that code!  Then run the code with an example and confirm that it's really doing the thing that you thought it was supposed to be doing in the previous question.  *Hint*: you can check it against an example in a lesson you've already had.

----

# Part 2 (Former Problem Set 4)

The questions in this part are all about Lee Epstein & Andrew Martin, *Does Public Opinion Influence the Supreme Court? Possibly Yes (But We're Not Sure Why)*, 13 U. Pa. J. Const. L. 263 (2010), which you can download from any of the standard legal research databases.  A copy of the dataset they used for this paper is available on our folder as PublicOpinion.csv 

## Question 1 (40 points): 

Describe the methods and results of the Epstein and Martin paper in your own words.  In doing so, be sure to: 

- Explain what statistical techniques they used, and why they make sense for their data;
- Explain how they designed their research, i.e., what the independent and dependent variables are, how the data are structured, etc.; 
- Explain why they thought that their research was an improvement on the prior research in the area; and 
- Explain what they found, and why their results might matter. 

## Question 2: (50 points): 

Replicate their results.  This may require some work with the dataset, and may require making some decisions in the case of ambiguity (for example, they don't supply a codebook, so you'll have to examine the variable names and try to figure out what goes with what).  That's part of the challenge!  You should be able to figure out pretty well what variables they used with a little bit of careful thought and detective work.  It's ok if your numbers don't come out exactly the same as theirs do, but you should get as close as possible. Also, you don't need to replicate their robustness checks. 

## Question 3 (10 points): 

Suggest one way in which this research could be improved.  The more detailed, the better. 