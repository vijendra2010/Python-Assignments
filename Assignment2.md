**Q26. What is a string? How can we declare string in Python?**

Ans: String is a sequence of characters. In Python the string can be declare in the following ways.
  
	single_quote_str = ' This declaration is used when the string itself contains "" '
	double_quote_str = " This declaration is used when the string itself contains '' "
	triple_quote_str = ''' Multi line text '''
	
**Q27. How can we access the string using its index?**

Ans: We can iterate over the string in a similar manner we iterate the arrays using index.

**Q28. Write a code to get the desired output of the following.**
**string = "Big Data iNeuron"
desired_output = "iNeuron"**

	print(string.split(' ')[2])
	
**Q29. Write a code to get the desired output of the following**
**string = "Big Data iNeuron"
desired_output = "norueNi"**

	print(string[::-1].split(' ')[0])
	
**Q30. Resverse the string given in the above question.**

	print(string[::-1])
	
**Q31. How can you delete entire string at once?**

	del string
	
**Q32. What is escape sequence?**

Ans: An escape sequence is a sequence of characters that, when used inside a character or string, does not represent itself but is converted into another character or series of characters that may be difficult or impossible to express directly, like newline (\n), tab (\t), and so on.
	
**Q33. How can you print the below string?**
**'iNeuron's Big Data Course'**

	print("'iNeuron's Big Data Course'")

**Q34. What is a list in Python?**

Ans: List are the use to store multiple values in single variable, the elements in a list can be homogenous or hetrogenous, list are dynamic and the elements can be added and can be deleted at any point in the program. List can also contains duplicate elements.

	profile_details = ['Vijendra', 24, { 'city': 'Ajmer', 'state': 'Rajasthan' }, {'status': True }]
	
**Q35. How can you create a list in Python?**	

Ans: List are represented by [] in python and all the values are comma separated within the square bracket.

	list_example = [ 1, 3, 4, 5, 6 ]
	
**Q36. How can we access the elements in a list?**

Ans: We can access list elements by index that starts with 0 and ends at length-1.

	list_access = [ 1, 3, 4, 5 ]
	print(list_access[2])
	
**Q37. Write a code to access the word "iNeuron" from the given list.**
**lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]**

	lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
	print(lst[4][2])
	
**Q38. Take a list as an input from the user and find the length of the list.**

	nums = []
	n = input('Enter the number of elements: ')
	for i in range(0, n):
	 num = int(input())
	 nums.append(num)
	print(nums)	
	
**Q39. Add the word "Big" in the 3rd index of the given list.**
	
	lst = ["Welcome", "to", "Data", "course"]
	lst.insert(2, "Big")
	print(lst)

**Q40. What is a tuple? How is it different from list?**

Ans: Lists are mutable its values can be change whereas the tuples are immutable and the values can't be change once assigned.

**Q41. How can you create a tuple in Python?**

Ans: We can create a tuple by assigning multiple value within () and assigned it to some variable.

	tuple_ex = ( 1, 2, 3, 3 )
	
**Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.**

	tuple_ex = (1,2,3)
	tuple_ex[0]="Vijendra"
	
	Errormsg:
	TypeError: 'tuple' object does not support item assignment
	
The assignment is not allowed in tuple once it is declared as the tuples are immutable.

**Q43. Can two tuple be appended. If yes, write a code for it. If not, why?**

Ans: Yes, two tuples can be appended.

	a = (1,2,3)
	b = (3,4,5)
	c = a + b
	print(c)
	
**Q44. Take a tuple as an input and print the count of elements in it.**	

	tup = tuple(input().strip().split())
	print(len(tup))
	
**Q45. What are sets in Python?**

Ans: Sets are built-in data structures that can hold collection of data, sets only holds unique values and can't be indexed and changed.

	set_demo = {1, 3, 4, 5}
	print(set_demo)
	
**Q46. How can you create a set?**

Ans: We can declare a set with {} and put multiple values within the {}.

**Q47. Create a set and add "iNeuron" in your set.**

	st = {1, 2, 3}
	st.add(4)
	print(st)
	
**Q48. Try to add multiple values using add() function.**

	st = {1, 2, 3}
	st.add(4)
	st.add(5)
	print(st)
	
**Q49. How is update() different from add()?**	

Ans: The add() method is used to add a single element to the set, whereas the update() mehtod is used to add sequence of elements or any other iterable to the existing set.
	
	#Add ex
	st = {1, 3, 4}
	st.add(5)
	print(st)
	
	#Update ex
	st = {1, 3, 4}
	temp = [2, 5]
	st.update(temp)
	
**Q50. What is clear() in sets?**	

Ans: clear() method is used to remove all the elements from the set.
	
**Q51. What is frozen set?**	

Ans: frozenset() method creates a immutable set of any iterable, it is a built-in method in python and as it is a set it only contains unique elements.

	#On tuples
	tuple_ex = (1, 3)
	frozen_tuple_set = frozenset(tuple_ex)
	
	#On List
	list_ex = [1, 3, 4]
	frozen_list_set = frozenset(list_ex)
	
	#On Dictionary(keys will be part of the resultant set)
	dict_ex = { "name":"Vijendra", "age": 24 }
	frozen_dict_set = frozenset(dict_ex)
	
**Q52. How is frozen set different from set?**	

Ans: Frozen sets are immutable and can't be modified, whereas the normal sets are mutable they can be modified at any point of time.

**Q53. What is union() in sets? Explain via code.**
  
Ans: Union() are used to make a single set from two different sets that contains all the elements of both the sets.

	a = {1,2}
	b = {2,3}
	c = a.union(b)
	
	#There can be multiple sets in the union method new_set = original_set.union( set1, set2, ... )
	
**Q54. What is intersection() in sets? Explain via code.**

Ans: The intersection() method gives the common elements which are present in all the specified sets.

	a = {1, 2, 3}
	b = {2, 4, 5, 7}
	c = {1, 2}
	d = a.intersection(b, c)
	
	#There can be multiple sets in the intersection method new_set = original_set.intersection( set1, set2, ... )
	
**Q55. What is dictionary ibn Python?**

Ans: Dictionary is a collection of key value pair, the dictionary contains the key:value separated by comma. The keys in the dictionary are immutable and can't be repeated whereas the values can be repeated.

	dict = { "name":"Vijendra", "age": 24 }
	
Dictionary can also be created by using the built-in dict() method.

	using_dict = dict({ "name":"Vijendra", "age": 24 })
	
Creating dictionary with each item as a pair.
	
	pair_dict = ([(1, "str1"), (2, "str2")])
	
**Q56. How is dictionary different from all other data structures.**

Ans: In dictionary the data gets stored in key:value pair whereas in the other data types there is not concept of keys. To access the element in dictionary keys are used, whereas other data types use indexing.

**Q57. How can we delare a dictionary in Python?**

Ans: These are the following way to declare the dictionary in python.
	
	#Empty dictionary
	dict1 = {}
	dict2 = dict()
	
	#Dictionary with key:value pair
	dict1 = { key:value }
	dict2 = dict({ key: value })
	
	#Using the fromkeys() method
	dict_name = dict.fromkeys(sequence, value)

**Q58. What will the output of the following?**
**var = {}**
**print(type(var))**

	#Output
	<class 'dict'>
	
**Q59. How can we add an element in a dictionary?**

	dict_ex = { "name": "Vijendra", "age": 24 }
	dict_ex.update({"mobile": "7777777777"})
	print(dict_ex)
	
**Q60. Create a dictionary and access all the values in that dictionary.**

	dict_ex = { "name": "Vijendra", "age": 24 }
	dict_ex.update({"mobile": "7777777777"})

	for key, value in dict_ex.items():
  	print(key,":",value)
    
**Q61. Create a nested dictionary and access all the element in the inner dictionary.**

	data = {
    'emp1': {'Name': 'Bobby', 'Id': 1, "Age": 20},
    'emp2': {'Name': 'ojaswi', 'Id': 2, "Age": 22},
    'emp3': {'Name': 'rohith', 'Id': 3, "Age": 20},
	}
 
	for key_out, value_out in data.items():
		for key_in, value_in in value_out.items(): 
			print(key_in,":", value_in)
			
**Q62. What is the use of get() function?**

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Ajmer"
	}

get(keyname, value)	keyname is required, value is optional if there is no key exist as keyname then value will be return as default.

	print(data.get("name"))
	
**Q63. What is the use of items() function?**

Ans: The items() function is used to return the key:value pair of the dictionary
	
	dict = { "name": "Vijendra", "age": 24 }
	
	for key, value in dict.items():
		print(key, ":", value)
	
**Q64. What is the use of pop() function?**

Ans: The pop() function is the built-in function in python, it is used to remove the element at the specified index. If the index is not specified then the last element will be removed.

**Q65. What is the use of popitems() function?**

Ans: The popitem() function removes the item that was last inserted in the dictionary.The return value of the function is the item that has been removed.

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	
	result = data.popitem()
	#Output ("city": "Jaipur")
	
**Q66. What is the use of keys() function?**

Ans: The keys() function returns a view object, the view object contains the keys of the dictionary in list.
	
	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	
	listed_keys = data.keys()
	print(listed_keys)
	
**Q67. What is the use of values() function?**

Ans: The values() function returns a view object, the view object contains the values of the dictionary in list.

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	
	listed_values = data.values()
	print(listed_values)	
	
**Q68. What are loops in Python?**	

Ans: Loops are the way we can iterate over the iterables in python.

**Q69. How many type of loop are there in Python?**

Ans: There are two types of loops while loop and for loop.

**Q70. What is the difference between for and while loops?**

Ans: for loops are used when the number of iterations are fixed, whereas the while loop is used when the number of iterations are not fixed and the loop continue to execute untill the specified condition is met.

**Q71. What is the use of continue statement?**

Ans: The continue keyword is used to end the current iteration in a for loop (or a while loop), and continues to the next iteration.

**Q72. What is the use of break statement?**

Ans: It is used to terminate the loop when some condition is met.

**Q73. What is the use of pass statement?**

Ans: The pass statement is null statement but it is different from comments. The pass can be place where the user is not sure what code is to be placed, the pass is placed where the empty code is not allowed.

**Q74. What is the use of range() function?**

Ans: The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number.

**Q75. How can you loop over a dictionary?**

Ans: There are multiple ways to iterate over the dictionary.

Using keys()
	
	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	data_keys = data.keys()
	
Using values()

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	data_keys = data.values()
	
Iterate over the all keys and value.

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	for key, value in data.items():
		print(key, ":", value)
		
Get key and value without using items()

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	for item in data:
		print(item, ":", data[item])
		
Access items in key:value pair

	data = {
		"name": "Vijendra",
		"age": 24,
		"city": "Jaipur"
	}
	data_keys = data.items()
	
## Coding Problems

**Q76. Write a Python program to find the factorial of a given number.**

	def fact(n):
		if ( n == 0 | n == 1):
			return 1
		else:
			return n * fact(n-1)

	result = fact(5)
	print(result)
	
**Q77. Write a Python program to calculate the simple interest. Formula to calculate simple interest is SI = (PRT)/100**

	def s_interest(p, r, t):
		si = (p*r*t)/100
		return si

	result = s_interest(100, 5, 2)
	print(result)
	
**Q78. Write a Python program to calculate the compound interest. Formula of compound interest is A = P(1+ R/100)^t.**

	def c_interest(p, r, t):
		ci = p*(1 + r/100)**t
		return ci
		
	result = c_interest(100, 5, 2)
	print(result)

**Q79. Write a Python program to check if a number is prime or not.**

	def is_prime(n):
		if n>1:
			for i in range(2, n):
				if (n%i==0):
					return False
			else:
				return True
		else:
			return False

	result = is_prime(8)
	print(result)	
	
**Q80. Write a Python program to check Armstrong Number.**

	def cube(n):
		return n**3

	def amstrong(n):
		sum = 0
		temp = n
		while(temp>0):
			rem = temp%10
			sum = sum + cube(rem)
			temp = temp//10

		if sum == n:
			return True	
		else:
	  	return False
			
  print(amstrong(371))

**Q81. Write a Python program to find the n-th Fibonacci Number.**

	def fibo(n):
		if n==0:
			return 0
		elif n==1 or n==2:
			return 1
		else:
			return fibo(n-1) + fibo(n-2)

	print(fibo(9))
	
	
