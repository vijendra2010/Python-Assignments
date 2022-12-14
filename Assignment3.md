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





	
