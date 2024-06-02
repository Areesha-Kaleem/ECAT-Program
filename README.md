# ECAT-Program
This Python program administers an ECAT with features for skipping and revisiting questions, calculating results, and determining admission eligibility. It supports Pre-Engineering, Pre-Medical, and ICS tracks, with user authentication and registration.

This code is a Python program designed to conduct an ECAT (Engineering College Admission Test). It has several functionalities that include administering tests for different educational tracks, calculating results, allowing students to skip and later answer questions, and determining admission eligibility. Here’s a breakdown of the main components and how the code works:

Key Features
Multiple Test Types: The code can administer tests for three tracks: Pre-Engineering, Pre-Medical, and ICS (Intermediate in Computer Science).
Structured Questions: Each test consists of 10 questions divided into sections:
English: 1 question
Chemistry/Computer: 3 questions
Physics: 3 questions
Mathematics/Biology: 3 questions
Result Calculation: A function calculates and displays the test results, including marks, percentage, skipped questions, correct answers, wrong answers, and admission eligibility.
Question Sections: The user is informed which section they are currently answering.
Skipping and Revisiting Questions: Users can skip questions and revisit them later using a designated function.
Automatic Submission: The test will automatically submit once all questions are answered or skipped questions are revisited, but the user can also submit at any point.
Main Functions
result_calculator Function:

Takes four parameters: skipped questions, total marks, correct answers, and wrong answers.
Calculates and prints the user's percentage.
Determines if the user is eligible for admission based on their score.
answer_to_skip Function:

Allows users to revisit and answer previously skipped questions.
Recursively calls itself if the user decides to skip questions again.
Calls result_calculator when all questions are answered or when the user decides to submit the test.
ecat Function:

Main function for administering the test.
Sets up the test based on the user's chosen category (Pre-Engineering, ICS, Pre-Medical).
Presents questions to the user and records their answers.
Manages skipped questions and invokes the answer_to_skip function if needed.
Invokes result_calculator when the test is completed.
User Authentication and Registration:

At the start, the user is authenticated by name and roll number.
New users can register by providing their CNIC and name, receiving a chalan number for payment, and getting a new roll number.
Example Flow
The user is prompted to enter their name and roll number for authentication.
After successful login, the user selects the type of test they want to take.
The test begins, presenting one question at a time.
The user answers each question, with the option to skip questions or submit the test at any point.
If questions are skipped, the user can revisit them using the answer_to_skip function.
Once all questions are answered or skipped questions revisited, the test is submitted automatically or manually.
The result_calculator function displays the user's results and eligibility for admission.
Simplified Code Overview
Here’s a simplified overview of the code structure:
import random

def result_calculator(skipped, total_marks, correct_answers, wrong_answers):
    # Display results and calculate eligibility
    ...

def answer_to_skip():
    # Handle skipped questions
    ...

def ecat():
    # Main function to conduct the ECAT test
    ...

# User authentication and registration process
while True:
    # Authenticate or register user
    ...

    if authenticated:
        start = input("Enter START\n")
        if start == "START":
            ecat()
            break
This explanation provides a high-level understanding of how the code works to conduct an ECAT test, manage user interactions, and calculate results.
