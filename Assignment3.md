**Q1. What is the purpose of Python's OOP?**

Ans: Aim is to implement the real-world entities programatically, ex: inheritance, polymorphism and encapsulation. The main aim of OOPs is to bind the data and the functions that work on these data in a single unit/block of code such that no other part of code can access the data directly.

**Q2. Where does an inheritance search look for an attribute?**

Ans: The inheritance search looks for an attribute starting from the nearest scope which is instance object, then the class from which the object is created, then in the superclasses.

**Q3. How do you distinguish between a class object and an instance object?**

Ans: Object is a actual thing that is store physically in the memory and instance is a virtual copy of the object.

**Q4. What makes the first argument in a class’s method function special?**

Ans: In OOPs whenever we define a method ina class we use **self** as the first argument. There can be multiple object of any class, and the **self** keyword is used to show the instance of the given class.
  
	class Point(object):
		def __init__(self,x = 0,y = 0):
			self.x = x
			self.y = y

		def distance(self):
      return (self.x**2 + self.y**2) ** 0.5
