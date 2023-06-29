# ES6 CLASSES

## This folder contains tasks covering the following topics:
- Defining Class
- Adding methods to a Class
- Adding static methods to a class
- Extending a class from another
- Metaprogramming and symbols

## Here are the questions.

0. Implement a class named __ClassRoom__:

	- Prototype: <span style="background-color: gray">export default class __ClassRoom__</span>
	- It should accept one attribute named <span style="background-color: gray">maxStudentsSize</span> (Number) and assigned to <span style="background-color: gray">\_maxStudentsSize</span>

1. Import the __ClassRoom__ class from __0-classroom.js__.

	- Implement a function named <span style="background-color: gray">initializeRooms</span>. It should return an array of 3 <span style="background-color: gray">ClassRoom</span> objects with the sizes 19, 20, and 34 (in this order).

2. Implement a class named __HolbertonCourse__:

	- Constructor attributes:
		* name (String)
		* length (Number)
		* students (array of Strings)
	- Make sure to verify the type of attributes during object creation
	- Each attribute must be stored in an “underscore” attribute version (ex: <span style="background-color: gray">name</span> is stored in <span style="background-color: gray">\_name</span>)
	- Implement a getter and setter for each attribute.

3. Implement a class named __Currency__:

	- Constructor attributes:
		* code (String)
		* name (String)
	- Each attribute must be stored in an “underscore” attribute version (ex: <span style="background-color: gray">name</span> is stored in <span style="background-color: gray">\_name</span>)
	- Implement a getter and setter for each attribute.
	- Implement a method named <span style="background-color: gray">displayFullCurrency</span> that will return the attributes in the following format <span style="background-color: gray">name (code)</span>.

4. Import the class __Currency__ from __3-currency.js__

Implement a class named __Pricing__:

	- Constructor attributes:
		* amount (Number)
		* currency (Currency)
	- Each attribute must be stored in an “underscore” attribute version (ex: <span style="background-color: gray">name</span> is stored in <span style="background-color: gray">\_name</span>)
	- Implement a getter and setter for each attribute.
	- Implement a method named <span style="background-color: gray">displayFullPrice</span> that returns the attributes in the following format <span style="background-color: gray">amount currency_name (currency_code)</span>.
	- Implement a static method named <span style="background-color: gray">convertPrice</span>. It should accept two arguments: <span style="background-color: gray">amount</span> (Number), <span style="background-color: gray">conversionRate</span> (Number). The function should return the amount multiplied by the conversion rate.

5. 

6. 

7. 

8. 

9. 

10.
