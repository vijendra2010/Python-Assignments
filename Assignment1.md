**Q1. Why do we call Python as a general purpose and high-level programming language?**

Ans. Python has multiple usecases in different domains say web development, Machine Learning, Artificial Inteligence etc that's why it is called         general purpose language. The reasons behind pythons so divers capabilities is its libraries and utilities and the ease of learning and writing code     in python. Python is an interpreter language which means the python code is executed line by line from top to bottom an as the code written in python     seems like english language sentences and human readable it is high level language. 

**Q2. Why is Python called a dynamically typed language?**

Ans. Because we don't have to specify the variable type while declaring the variables, it dynamically identify the type based on the assigned value.

**Q3. List some pros and cons of Python programming language?**
		
	Pros
	1. Ease to write and learn.
	2. Wide support of libraries and utilities.
	3. Usage in divers IT domains.
	4. Larger community support.
	5. Highly Scalable.

	Cons
	1. Slower then compiled languages.
	2. High memory consumption.
    
**Q4. In what all domains can we use Python?**

Ans. Machine Learning, Deep Learning, Artificial Inteligence, Data Science, Big Data domain, Web Development etc.

**Q5. What are variable and how can we declare them?**

Ans. Variables are the reference names to the memory location that holds the values that are being used in the python program. In python variables case be simply declare as follows.

	name = 'Vijendra'
	age = 25
              
**Q6. How can we take an input from the user in Python?**

Ans. To take input from user/console we use the 'input()' function which is pythons in-built function used to take inputs. The function can have argument       also that can be message to the user.        

**Q7. What is the default datatype of the value that has been taken as an input using input() function?**

Ans. String

**Q8. What is type casting?**

Ans. Converting one type of data to another type.

**Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?**

Ans. Yes, we can take multiple inputs using singe inpur() function.
	
	a, b, c = input().split()
    
**Q10. What are keywords?**

Ans. Keywords are the reserved words that have their meaning in python.

**Q11. Can we use keywords as a variable? Support your answer with reason.**

Ans. No, we can not use keywords as variables it will show SyntaxError.
	
	this = 5

Error: SyntaxError: invalid syntax
    
**Q12. What is indentation? What's the use of indentaion in Python?**

Ans. Indentation is the space from where any statement starts, in python indentations are used to describe the scope of any block of code.

**Q13. How can we throw some output in Python?**

Ans. Using 'print()' function.

**Q14. What are operators in Python?**

Ans. Operators are symbols that are use to perform different operations in pythons between two or more operands, examples are arithmatic operators and bitwise operators.

**Q15. What is difference between / and // operators?**

Ans. Float division: / ==>  5/2 = 2.5 Always returns float value in output.
     Integer division: // ==> 5/2 = 2 Always return the int value in output.
     
**Q16. Write a code that gives following as an output. ( iNeuroniNeuroniNeuroniNeuron )**

	print("iNeuron"*4)

**Q17. Write a code to take a number as an input from the user and check if the number is odd or even.**

	num = int(input('Please enter a number: '))
	if(num%2==0):
	 print('even')
	else:
	 print('odd')
        
**Q18. What are boolean operator?**

Ans. and, or and not are boolean operators in python.
    
**Q19. What will the output of the following?**

Ans. 1 or 0 = 1
     0 and 0 = 0
     True and False and True = False
     1 or 0 or 0 = 1
     
**Q20. What are conditional statements in Python?**

Ans. Equals: a == b.
     Not Equals: a != b.
     Less than: a < b.
     Less than or equal to: a <= b.
     Greater than: a > b.
     Greater than or equal to: a >= b
     
**Q21. What is use of 'if', 'elif' and 'else' keywords?**

Ans. if and elif is use to execute the specific code that only has to be executed when certain condition gets satified.

**Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".**

Ans. users_age = int(input('Please enter your age in years: '))

	if (users_age < 18):
	 print("I can't vote")
	else
	 print("I can vote")
        
**Q23. Write a code that displays the sum of all the even numbers from the given list. ( numbers = [12, 75, 150, 180, 145, 525, 50] )**

	for i in numbers:
	 if (i%2==0):
	 sum += i
	print(sum)
     
**Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.**

	num1, num2, num3 = int(input("Enter 3 different numbers: ").split())
	if (num1 >= num2) and (num1 >= num3):
	 largest = num1
	elif (num2 >= num1) and (num2 >= num3):
	 largest = num2
	else:
	 largest = num3
	print("The largest number is", largest)
     
**Q25. Write a program to display only those numbers from a list that satisfy the following conditions
    - The number must be divisible by five
    - If the number is greater than 150, then skip it and move to the next number
    - If the number is greater than 500, then stop the loop
    numbers = [12, 75, 150, 180, 145, 525, 50]**
		
	for i in numbers:
	 for i in numbers:
	  if (i%5==0):
		 if (i>150):
		  continue
		 if (i>500):
			break
		print(i)


