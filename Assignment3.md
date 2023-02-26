**Q1. What is the purpose of Python's OOP?**

Ans: Aim is to implement the real-world entities programatically, ex: inheritance, polymorphism and encapsulation. The main aim of OOPs is to bind the data and the functions that work on these data in a single unit/block of code such that no other part of code can access the data directly.

**Q2. Where does an inheritance search look for an attribute?**

Ans: The inheritance search looks for an attribute starting from the nearest scope which is instance object, then the class from which the object is created, then in the superclasses.

**Q3. How do you distinguish between a class object and an instance object?**

Ans: Object is a actual thing that is store physically in the memory and instance is a virtual copy of the object.

**Q4. What makes the first argument in a class’s method function special?**

Ans: In OOPs whenever we define a method in a class we use **'self'** as the first argument. There can be multiple object of any class, and the **'self'** keyword is used to show the instance of the given class.
  
	class Point(object):
		def __init__(self,x = 0,y = 0):
			self.x = x
			self.y = y

		def distance(self):
			return (self.x**2 + self.y**2) ** 0.5

Let us now instantiate this class and find the distance.

	>>> p1 = Point(6,8)
	>>> p1.distance()
	10.0

In the above example, __init__() defines three parameters but we just passed two (6 and 8). Similarly distance() requires one but zero arguments were passed. 

	>>> type(Point.distance)
	<class 'function'>
	>>> type(p1.distance)
	<class 'method'>
	
We can see that the first one is a function and the second one is a method. A peculiar thing about methods (in Python) is that the object itself is passed as the first argument to the corresponding function.

In the case of the above example, the method call p1.distance() is actually equivalent to Point.distance(p1)

**Q5. What is the purpose of the init method?**

Ans: The __init__ method is similar to the constructor in other languages, it is called each time whenever a new object is created of any class. It is also use to initialise the Object's attributes.

**Q6. What is the process for creating a class instance?**

Ans: To create a instance of a class call the class using class name and pass the arguments its __init__ method accepts.

	class Employee:
		def emp_details():
			print("Emp details")
			
	emp = Employee()
	emp.emp_details()
	
**Q8. How would you define the superclasses of a class?**

Ans: The class from which the other class gets inherite is called superclass.

**Q9. What is the relationship between classes and modules?**

Ans: Module is just a collection of classes or functions, and to use these classes/function we have to import the module in our program. All the related classes/functions are kept in a single module. Example: Math

**Q10. How do you make instances and classes?**

Ans: To make an instance of the class you need to call the class and pass the arguments accepted by the class.

**Q11. Where and how should be class attributes created?**

Ans: Class attributes should be declared inside the class but out side the function, in this way the attributes are accesible throughout the class.

	class Employee:
		company_name = 'TCS'	#Attribute 1
		
		def display():
			print(self.company_name)
			
**Q12. Where and how are instance attributes created?**		

Ans: Instance attributes are not shared by objects, each object has its own copy of instance attributes. To display all the instance attributes of an object we have 2 functions

	1. var() - This displays all the instance attributes in the from of dictionary.
	2. dir() - This function displays more attributes then the var(), it also displays class attributes and it also displays attributes of the ancester classes.
	
	class emp:
		def __init__(self):
			self.name = 'xyz'
			self.salary = 4000

		def show(self):
			print(self.name)
			print(self.salary)

	e1 = emp()
	print(vars(e1))
	print(dir(e1))

Output

	Dictionary form :{'salary': 4000, 'name': 'xyz'}
	['__doc__', '__init__', '__module__', 'name', 'salary', 'show']
	
**Q13. What does the term "self" in a Python class mean?**

Ans: The keyword **'self'** in python refers to the current instance of the class and is used to access the variable of the class.

**Q14. How does a Python class handle operator overloading?**

Ans: Operator overloading means to extend the meaning beyond the operational meaning of the given operator, such as the '+' operator is used to add two integers, to concate two strings and also to merge two lists, this is being done as the class 'int' and class 'str' have overloaded the operator '+'.

If we try to add two objects of any type then the compiler will show us error as the compiler don't know how to add the given objects, but if we define a function for the operator that know how to add those objects then there will be no error, this process is call operator overloading. To perform operator overloading, Python provides some special function or magic function that is automatically invoked when it is associated with that particular operator. For example, when we use + operator, the magic method __add__ is automatically invoked in which the operation for + operator is defined.

**Q15. When do you consider allowing operator overloading of your classes?**

Ans: When ever we try to perform some sort of operations with the operators which are not their default operation and when we provide the function that can be invoked to perform that operation then we can say we are allowing the operator overloading to our class.

**Q16. What is the most popular form of operator overloading?**

Ans: Most populer operator overloading is for addition(+) which is use for performing addition on numbers and is used to concate string values.

**Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?**

Ans: Inheritance and polymorphism are fundamental concepts of object oriented programming. These concepts help us to create code that can be extended and easily maintainable.Inheritance is a great way to eliminate unnecessary repetitive code. A child class can inherit from the parent class partially or entirely. Python is quite flexible with regards to inheritance. We can add new attributes and methods as well as modify the existing ones. Polymorphism contributes to Python’s flexibility as well. An object with a particular type can be used as if it belonged to a different type.

**Q18. Describe three applications for exception processing.**

Ans: Exception handling is the process of responding to unwanted or unexpected events when a computer program runs. Exception handling deals with these events to avoid the program or system crashing, and without this process, exceptions would disrupt the normal operation of a program.

**Q19. What happens if you don't do something extra to treat an exception?**

Ans: If we don't handle the ecveptions then the program or system gets crashed in case of any exception occurance.

**Q20. What are your options for recovering from an exception in your script?**

Ans: If there is any suspicious code in the script that may cause any exception then we put that code inside try-except block or we can also use the variants of try-except like try-except-else or try-finally.

**Q21. Describe two methods for triggering exceptions in your script.**

Ans: To handle exception in python we have two methods.
**1. Try** - This method catches exceptions raised by the program.
**2. Raise** - Triggers the exceptions manually using custom exceptions.

The **Try** method is use with except or with except else. The code that are likely to have exception during run time are placed inside the try block and the logic that has to be executed on any exception occurance are kept under except block.

	import sys
	
	l = ['a', 1e-15, null]
	
	for i int l:
		try:
			print(i)
			res = 1/int(i)
			break
		 except:
      print(“Whew!”, sys.exc_info()[0], “occurred.”)
      print(“Next input please.”)
      print()
	print(“The answer of”, result, “is”, y)		

The **Raise** is another way to that we can use when any exception occure at run time to clearify why the exception has occured.

	try:
		x = int(input(“Enter a positive integer: “))
    if x <= 0:
			raise ValueError(“It is not a positive number!”)
	except ValueError as val_e:
		print(val_e)
		
**Q22. Identify two methods for specifying actions to be executed at termination time, regardless of whether or not an exception exists.**

Ans: There are two methods else and finally that are used, they both have there own usage. 

The else is used to execute the code that is must be executed when the try block don't raise any exception. The use of the else clause is better than adding additional code to the try clause because it avoids accidentally catching an exception that wasn’t raised by the code being protected by the try

	for arg in sys.argv[1:]:
		try:
    	f = open(arg, 'r')
    except OSError:
    	print('cannot open', arg)
    else:
    	print(arg, 'has', len(f.readlines()), 'lines')
    	f.close()

The try statement has another optional clause finally which is intended to define clean-up actions that must be executed under all circumstances. The finally clause will execute as the last task before the try statement completes. The finally clause runs whether or not the try statement produces an exception. 
				
	def divide(x, y):
    try:
			result = x / y
    except ZeroDivisionError:
    	print("division by zero!")
    else:
    	print("result is", result)
    finally:
    	print("executing finally clause")			
			
**Q23. What is the purpose of the try statement?**

Ans: The puspose of try block is to hold the code that is likely to have the chances to have exceptions, and to throw the exception to the catch block to get it handled there.

**Q24. What are the two most popular try statement variations?**

Ans: The try is used with except and sometimes with multiple excepts, apart from this there is a optional methods else and finally that can also be used with the try block.

**Q25. What is the purpose of the raise statement?**

Ans: The raise keyword is used to raise an exception. You can define what kind of error to raise, and the text to print to the user.
	
	x = "hello"
	if not type(x) is int:
  	raise TypeError("Only integers are allowed")
		
**Q26. What does the assert statement do, and what other statement is it like?**

Ans: The assert keyword is used when debugging code. The assert keyword lets you test if a condition in your code returns True, if not, the program will raise an AssertionError.

	x = "hello"
	#if condition returns False, AssertionError is raised:
	assert x == "goodbye", "x should be 'hello'"
	
**Q27. What is the purpose of the with/as argument, and what other statement is it like?**

Ans: **with** statement is used in exception handling to make the code cleaner and much more readable. It simplifies the management of common resources like file streams. Example of file handling 

	# Without using with statement and without try-catch
	file = open('file_path', 'w')
	file.write('hello world !')
	file.close()
		
The above code is not able to handle any exception and the code is also not much readable and compact. An exception during the file.write() call in the above code can prevent the file from closing properly which may introduce several bugs in the code.

	# Without using with statement with try catch
	file = open('file_path', 'w')
	try:
  	file.write('hello world')
	finally:
  	file.close()
		
The above code can handle the exception but it is not that compact

	# using with statement
	with open('file_path', 'w') as file:
  	file.write('hello world !')
		
The above code is more compact and redable and also there is no need of the file.close() here as the with itself ensures proper acquisition and release of resources.		

**Q28. What are *args, **kwargs?**

Ans: Python has *args, which allows us to pass a variable number of non-keyword arguments to a function. Non-keyword here means that the arguments should not be a dictionary (key-value pair), and they can be numbers or strings.

When an asterisk(*) is passed before the variable name in a Python function, then Python understands that here the number of arguments is not fixed. Python makes a tuple of these arguments with the name we use after the asterisk(*) and makes this variable available to us inside the function. This asterisk(*) is called an “unpacking operator”. 

	def multiplyNumbers(*numbers):
    product=1
    for n in numbers:
        product*=n
    return product
	print("product:",multiplyNumbers(4,4,4,4,4,4)) 

*args enable us to pass the variable number of non-keyword arguments to functions, but we cannot use this to pass keyword arguments. Keyword arguments mean that they contain a key-value pair, like a Python dictionary. **kwargs allows us to pass any number of keyword arguments. Python will consider any variable name with two asterisks(**) before it as a keyword argument.

	def makeSentence(**words):
    sentence=''
    for word in words.values():
        sentence+=word
    return sentence
 	print('Sentence:', makeSentence(a='Kwargs ',b='are ', c='awesome!'))
	
Using Both *args and *kwargs in a Python Function. While doing this, the order of the arguments matter, *args has to come before *kwargs. So if you are using standard arguments along with *args and **kwargs, then you have to follow this order- Standard Arguments, *args, **kwargs.

	def printingData(codeName, *args, **kwargs):
    print("I am ", codeName)
    for arg in args:
        print("I am arg: ", arg)
    for keyWord in kwargs.items():
        print("I am kwarg: ", keyWord) 
	printingData('007', 'agent', firstName='James', lastName='Bond') 

The single and double asterisks that we use are called unpacking operators. Unpacking operators are used to unpack the variables from iterable data types like lists, tuples, and dictionaries. A single asterisk(*) is used on any iterable given by Python. The double asterisk(**) is used to iterate over dictionaries.
	
		
		
		
 
	
