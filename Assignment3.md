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
		
		
 
	
