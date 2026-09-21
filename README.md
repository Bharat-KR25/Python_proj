# Python_proj
Python Assignment 1 - Data Structures - Strings & Tuples

Assignment Task Overview
Problem Statement:
This assignment focuses on understanding Python string operations and tuple manipulation,
including concatenation, slicing, built-in methods, and tuple operations.
Tasks:
Strings (Concatenation, Slicing, and Other Methods) :
1. String Concatenation:

Write a Python program that takes two strings, i.e., string 1 "Hello" and string 2 “get
name” as input from the user, and concatenates them together. Display the
concatenated string as the output.
Sample Output:
Enter your Name: Zara
Hello Zara

Now, concatenate string 3, "Welcome to Python programming,” to the existing string
and display the output string.
Sample Output:
Hello Zara, welcome to Python programming

2. String Slicing and Indexing:

Write a Python program using the above concatenated string as input and perform
the following tasks:
a. Print the first character of the string.
b. Print the last character of the string.
c. Print the first 5 characters of the string.
d. Print the last 11 characters of the string.
e. Print the string in reverse.
f. Use slicing and print the word “Python” from the existing string.

3. String Methods:

Write a Python program that takes a string, strM = “Python beginner tutorial," and
performs the following tasks:
a. Convert the sentence to uppercase.
b. Convert the sentence to lowercase.
c. Use Capitalize and return the sentence to the original input form.
d. Count the total number of occurrences of character ‘t’ in the string.
e. Replace all occurrences of “Python” with “Data Analytics” in the input string
strM = “Python beginner tutorial.”

Tuples (Creation, Modification and Access) :
Create the 1st tuple with values -> (10, 20, 30) and the 2nd tuple with values -> (40, 50, 60):

a. Concatenate the two tuples and store it in “t_combine”
b. Repeat the elements of “t_combine” 3 times
c. Access the 3rd element from “t_combine”
d. Access the first three elements from “t_combine”
e. Access the last three elements from “t_combine”


  
  
# Python Assignment 2- Data Structures - List, Dictionary, Set & Conditional

Statements

Assignment Task Overview
Problem Statement:
As a Python learner, this assignment focuses on working with core data structures such as lists,
dictionaries, and sets, along with implementing conditional statements.
The objective is to develop a strong understanding of:
● List creation, modification, and access operations
● Dictionary creation and manipulation using key-value pairs
● Set properties and operations like uniqueness, union, and intersection
● Decision-making using conditional statements (if, elif, else)
You are required to write Python programs that demonstrate these concepts and display outputs as
per the given tasks.
Tasks:
List (Creation, Modification, and Access):
1. List Creation:
a. Create a list named age_list with five integer elements. For eg., [24, 25, 27, 28 ,29]
b. Create a list named name_list with five string elements.

2. List Operations / Modifications:
a. Append the string "Yazhini" to name_list.
b. Insert the element 26 at index 2 in age_list.
c. Remove the string "Yazhini" from name_list.
d. Pop the last element from age_list.
e. Extend the age_list with additional ages [31,30,32].
f. Sort age_list in descending order.
g. Find the max age, min age, and sum of all ages from age_list.

3. Accessing List Elements:
a. Print the first element of name_list.
b. Print the last element of name_list.
c. Print the elements from index 2 to index 4 in name_list.
d. Print the elements of name_list in reverse order.

Dictionary (Creation, Modification and Access):

a. Create a dictionary named student_marks that maps the names of five students to
their marks (use a scale of 0 to 100).
b. Access and print the mark of a specific student of your choice.
c. Add a new student, "Janani," with a mark of 80 to the student_marks dictionary.
d. Update the mark of any one older student to 82.
e. Use the keys(), values(), and items() methods to print all keys, values, and key-value
pairs in the student_marks dictionary.

Sets (Operations):

a. Create a set called my_set with the following values: ['a','e','i','o','u','a','a','i']
Analyze the output and explain the same.
b. Attempt to access my_set[4]. If the code throws an error, provide an explanation.
c. Create two sets:

set1 with values: {1, 3, 5, 7, 9}
set2 with values: {2, 3, 5, 8, 10}

d. Compute and print the union and intersection of set1 and set2.

Operators & Conditional Statements : (IF, ELIF, ELSE)
Performance Category Program:
1. Prompt the user for input. Score range should be from 0 to 10 (both inclusive).
2. Find the performance category based on the input score using the following criteria:
a. Above Average: Score greater than 7
b. Average: Score between 4 and 7 (both inclusive)
c. Below Average: Score less than 4
3. Output: Print the Performance category
5. Additional Step: You can give a prompt of your choice to each category. For example, if
the score is below average, “Need to improve your performance; consistent practice
will lead to better results”.

Sample Output:
Enter your score (0 to 10): 7

# Python Assignment 3–While Loop, For Loop, and Function
    
Assignment Task Overview

This assignment focuses on implementing loops, control statements, and functions in Python.
The objective is to develop an understanding of:
● Iteration using a while loop and a for loop
● Control statements such as break, continue, pass, and else
● Function creation and usage
● Logical problem-solving using real-world examples
You will build programs, including a number guessing game, a multiplication table generator, and a
BMI calculator.
Tasks:
Task 1: While Loop & Control Statements -Number Guessing Game
Problem Statement: Create a Python program that implements a simple number guessing
game using a while loop. The program should make use of control statements such as else,
break, and continue.
Instructions:
1. Set Up the Game:
★ Generate a random number between 1 and 10 that the user has to guess.
Import random and use randint function.
2. Prompt the User:
★ Ask the user to guess the number.
★ Set a variable attempts to 3, which represents the maximum number of
guesses allowed.

3. Implement the Guessing Logic:
★ Use a while loop to allow the user to keep guessing until they get the correct
number or run out of attempts.
★ Provide feedback to the user for each guess:

➢ If the guess is out of the valid range (1 to 10), inform the user.
➢ If the guess is greater than the secret number.
➢ If the guess is lower than the secret number.
➢ If the guess is correct, congratulate the user and end the game.

4. Control Statements:
★ Use continue to skip the rest of the loop after informing the user if the guess is
out of range.
★ Use break to exit the loop when the guess is correct.
★ Use else with the while loop to provide a message like "Better luck next time!"
if the user runs out of attempts without guessing the correct number.

Task 2:- For Loop - Multiplication Table Generator

Problem Statement: Create a Python program that generates and prints a multiplication
table (from 1 to 10) for a given number using a for loop and the range function.
Step-wise Instructions:
1. Prompt user for input. Ask the user to enter a number for which they want to generate
a multiplication table.
2. Generate the Multiplication Table: Use a for loop to iterate through the numbers 1 to
10. In each iteration, calculate the product of the user's number and the current
number from the loop.
3. Display the Multiplication Table:
Print each line of the multiplication table in the format "number x i = result."

Assignment Task Overview
Project Title: Customer Support Ticket Analyser
Problem Statement
Customer support teams handle numerous service tickets daily. Analysing support tickets helps
identify common issues, customer sentiment, support quality, and areas for improvement.
In this project, you will build a Python-based Ticket Analysis System that stores, cleans, analyses,
and extracts insights from customer support tickets.

Step 1: Preloaded Tickets

Begin your program with the following dictionary of lists containing 10 customer tickets:
ticket_data = { 'Ticket_No': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
'Customer_Name': [ 'Ravi', 'Meera', 'Sam', 'Anu', 'Rakesh', 'Divya', 'Arjun', 'Kiran', 'Leela', 'Nisha'
],
'Issue_Description': [
' Internet not working!!! ', 'slow response, very poor service ',
'GREAT support! issue resolved.',' okay... need help ', 'not BAD but slow', 'Excellent guidance, Very Helpful!',
'good support and good behaviour!', 'Poor handling of technical issue', 'Satisfied. Could be better.', 'Good service...
quick response.'
],
'Priority': ['High', 'Low', 'High', 'Medium', 'Low', 'High', 'Medium', 'High', 'Low', 'Medium']}
print(ticket_data)

● Task: Print the initial ticket data in a readable format.

Step 2: Add More Tickets
❖ Ask the user: How many new tickets do you want to add?
❖ For each new ticket, collect:
➢ Customer Name
➢ Issue Description
➢ Priority (High / Medium / Low)
Requirements:
● Ticket numbers must auto-increment starting from 11.
● Validate priority (accept only High, Medium, Low).
● Append new data to ticket_data.

Step 3: Text Cleaning for Issue Descriptions
❖ Clean all issue descriptions by applying:
➢ Remove punctuation (.,!?-)
➢ Convert multiple spaces → single space
➢ Remove leading/trailing spaces
➢ Convert text to lowercase
➢ Replace slang/shorthand (example: "ok" → "okay")
❖ Hints:
Use .replace(), .split(), ' '.join(), .strip(), .lower().
Step 4: Keyword-Based Issue Insights
Create a function:
def count_tickets_with_word(word):
Function Requirements:
● Case-insensitive search
● Returns how many ticket descriptions contain the given word

Use this function to print:
● Number of tickets containing "poor"
● Number of tickets containing "good"
● Number of tickets containing "slow"
● Number of tickets containing "excellent"

Step 5: Final Summary & Insights
Produce detailed analytics:
1. Display Final Cleaned ticket_data
Nicely formatted dictionary-of-lists output.
2. Priority Analysis
Compute:
● Number of High-priority tickets
● Number of Medium priority tickets
● Number of Low-Priority tickets
3. Find the Ticket With the Longest Issue Description
Based on word count, print:
● Ticket number
● Customer name
● Cleaned issue text
● Word count
4. Extract Unique Words Used
Generate a set of all unique words across all issue descriptions.
Show:
● Count of unique words
● The word list (sorted)
