Download Link: https://assignmentchef.com/product/solved-comp301-project-2
<br>
<span class="kksr-muted">Rate this product</span>

In this project, you will work in groups of two or three. To create your group, use the Google Sheet file in the following link:.

This project contains a bonus component specified at the end and there are two code boilerplates provided to you: use Project2MYLET for the project and Project2BONUS for the bonus. Submit a report containing your answers to the written questions in PDF format and Racket files for the coding questions to Blackboard as a zip. Include a brief explanation of your team’s workload breakdown in the pdf file. If you attempt to solve the bonus question, make sure that your zip includes both Project2MYLET and Project2BONUS folders separately. Name your submission files as p2_member1IDno_member1username_member2IDno_member2username.zip

Example: p2_0011221_galtintas17_0011222_mkarakas16.zip.Please use Project 2 Discussion Forum on Blackboard for all your questions.

The deadline for this project is Nov 15, 2020 – 23:59 (GMT+3 : Istanbul Time). Read your task requirements carefully. Good luck!

Table 1. Grade Breakdown for Project 2

Problem Definition: To evaluate the programs, you need to understand the expressions of the language. It is the same for computers; therefore, you saw in the lecture how you can invent a language and define it for the computer to understand and evaluate.

In this project, you will define a language named MYLET that is similar to the simple LET language covered in the class. The syntax for the MYLET language is given below.

Program ::= Expression

Expression ::= Number

Expression ::= String

Expression ::= op(Expression, Expression, Number)

Expression ::= zero? (Expression)

Expression ::= if Expression then Expression{elif Expression then Expression}*

else Expression

Expression ::= Indetifier

Expression ::= let Indetifier = Expression in Expression

a-program (exp1)

const-exp (num)

str-exp (str)

op-exp (exp1, exp2, num)

zero?-exp (exp1)

if-exp (exp1 exp2 conds exps exp3)

var-exp (var)

let-exp (var exp1 body)

Figure 1. Syntax for the MYLET languagePart A. This part will prepare you for the following parts of the project. (15 pts)

(1) Write the 5 components of the language1:(2) For each component, specify where or which racket file (if it applies) we define and

handle them.Part B. In this part, you will create an initial environment for programs to run. (10 pts)

(1) Create an initial environment that contains 3 different variables (x, y, and z).(2) Using the environment abbreviation shown in the lectures, write how environment

changes at each variable addition.Part C. Specify expressed and denoted values for MYLET language. (5 pts)

1Hint: review Lecture 10 slides

2

Part D. This is the main part of the project where you implement the MYLET language given in the Figure 1 by adding the missing expressions.

<ol>

 <li>(1)  Add str-exp to the language. Strings are defined as any text starting and ending with ‘, e.g. ‘comp301’, ‘program’; strings are stored with ‘ symbols. (15 pts)Hint: String is an expression that is similar to Number, understanding the addition and implementation of Number may be helpful to complete this step.</li>

 <li>(2)  Add op-exp to the language. (15 pts) op-exp is similar to the diff-exp of the LET lan- guage; however, in LET language, the only possible operation was subtraction. op-exp enables you to do 4 arithmetic operations via its third input (Number), when third input is:• 1: perform addition (exp1 + exp2)• 2: perform multiplication (exp1 * exp2)• 3: perform division (exp1 / exp2)• any other number: perform subtraction (exp1 – exp2)</li>

 <li>(3)  Add if-exp to the language. Unlike if-exp of the LET language, you can add multiple conditions to be checked through elif-then extension. Starting from the condition of if, conditions will be checked until a true condition is found, and expression corresponding to the true condition will be evaluated as a result. If none of the if/elif conditions are correct, the expression in the else statement will be evaluated. (15 pts)</li>

 <li>(4)  Add a custom expression to the language. The expression can be simple, but you need to clearly explain what it does and how it works. You also need to provide the syntax of the expression. (15 pts)</li>

</ol>

Note that the implementation of the other expressions, that are same with the LET language, are already given in the .rkt file provided. We deleted the former implementations of if and diff-exp.

Part E. Create the following test cases. (10 pts)

(1) custom expression: Write test cases that controls if the expression works according to your explanation of the expression.Note: We provided several test cases for you to try your implementation. Uncomment corresponding test cases and run tests.rkt to test your implementation.

Bonus. Here is an alternative datatype ropes that allows manipulation of sequence of charac- ters instead of the most commonly used strings. You can try to implement ropes instead of strings as a bonus challenge.Note: The bonus question is worth 2 points in your overall final grade and no partial cred- its will be awarded. To get full credit, please implement this problem using the second code boilerplate (Project2BONUS) provided and write at least 6 test cases (two for each: fetch ith character, concatenate, substring) in a clear way to your tests.rkt for us to run. Please make sure that your test cases are clear and tests.rkt doesn’t give any errors, otherwise you won’t be able to receive any credits for this question. Add your code for the bonus problem to your submission as specified in the instructions.

Hint: Define your rope datatype similar to the way you did in the project, clearly define your grammar and feel free to use any helper procedures.