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
	
	
	

  
