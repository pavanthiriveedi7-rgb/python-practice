 Tasks-Conditional statements
Task 1: Number Checker
Write a program that asks the user for a number and tells them if it's:
Positive
Negative
Zero

Example Output:
Enter a number: 5
The number is negative


code:

def number_checker(number):
    if number == 0:
        return 'Zero'
    elif number > 0:
        return 'Positive'
    else:
        return 'Negative'
number = int(input("Enter a number: "))
print("The number is:",number_checker(number))


Task 2: Movie Ticket Price
Calculate movie ticket price based on age:
Children (under 12--> $5
Adults 12-64-->$10
Seniors <65--> $7
Ask user for their age and display the ticket price.


Example Output:
Enter your age: 8
Your ticket costs: $5

code:

def ticket_price(age):
    if age == 0:
        return 'Invalid age'
    elif age <= 12:
        return '$5'
    elif age <= 64:
        return '$10'
    else:
        return '$7'
age = int(input("Enter your age:"))
print("Your ticket cost : ",ticket_price(age))




Task 3: Simple Calculator
Ask user for two numbers and an operation (+, -, *, /)
Perform the calculation and show the result.


Example Output:
Enter first number: 10
Enter second number: 5
Enter operation (+, -, *, /): *
Result: 10 * 5 = 50


code:

def calculation(operation):
    if operation == "+":
        return i+j
    elif operation == "-":
        return i-j
    elif operation == "*":
        return i*j
    elif operation == "/":
        if j==0:
            return 'invalid'
        else:
            return i/j
    else:
        return 'Invalid'
i = int(input("enter a first number:"))
j = int(input("enter a second number:"))
operation = input("Enter operation(+,-,*,/) :")
print("result :",calculation(operation))




Task 4: Password Validator
Check if a password is strong:
1
Tasks-Conditional statements
At least 8 characters long
Contains at least one number
Tell the user if their password is "Strong" or "Weak"


Example Output:
Enter password: hello
Weak password! Must be 8 characters and contain a number



code:


password = input("Enter your password: ")


if len(password) >= 8 and any(char.isdigit() for char in password):
    print("Strong")
else:
    print("Weak")




Task 5: Grade Letter Converter
Convert numerical score to letter grade:
90-100--> A
80-89--> B
70-79--> C
60-69--> D
Below 60--> F



Example Output:
Enter your score: 85
Your grade is: B



code:

def grade_converter(marks):
    if marks ==0:
        return 'Invalid'
    elif marks>=90:
        return 'A'
    elif marks>=80:
        return 'B'
    elif marks>=70:
        return 'C'
    elif marks>=60:
        return 'D'
    else:
        return 'F'
marks = int(input("Enter your score:"))
print("Your grade is:",grade_converter(marks))
