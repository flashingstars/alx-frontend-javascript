# ES6 CLASSES

## This folder contains tasks covering the following topics:
- Defining Class
- Adding methods to a Class
- Adding static methods to a class
- Extending a class from another
- Metaprogramming and symbols

## Here are the questions.

0. Implement a class named __ClassRoom__:

	- Prototype: export default class __ClassRoom__
	- It should accept one attribute named maxStudentsSize (Number) and assigned to \_maxStudentsSize

1. Import the __ClassRoom__ class from __0-classroom.js__.

	- Implement a function named initializeRooms. It should return an array of 3 ClassRoom objects with the sizes 19, 20, and 34 (in this order).

2. Implement a class named __HolbertonCourse__:

	- Constructor attributes:
		* name (String)
		* length (Number)
		* students (array of Strings)
	- Make sure to verify the type of attributes during object creation
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Implement a getter and setter for each attribute.

3. Implement a class named __Currency__:

	- Constructor attributes:
		* code (String)
		* name (String)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Implement a getter and setter for each attribute.
	- Implement a method named displayFullCurrency that will return the attributes in the following format name (code).

4. Import the class __Currency__ from __3-currency.js__

	* Implement a class named __Pricing__:

	- Constructor attributes:
		* amount (Number)
		* currency (Currency)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Implement a getter and setter for each attribute.
	- Implement a method named displayFullPrice that returns the attributes in the following format amount currency\_name (currency\_code).
	- Implement a static method named convertPrice. It should accept two arguments: amount (Number), conversionRate (Number). The function should return the amount multiplied by the conversion rate.

5. Implement a class __named Building__:

	- Constructor attributes:
		* sqft (Number)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Implement a getter for each attribute.
	- Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named evacuationWarningMessage.
		* If a class that extends from it does not have a evacuationWarningMessage method, throw an error with the message Class extending Building must override evacuationWarningMessage

6. Import __Building__ from __5-building.js__.

	* Implement a class named __SkyHighBuilding__ that extends from __Building__:

	- Constructor attributes:
		* sqft (Number) (must be assigned to the parent class Building)
		* floors (Number)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Implement a getter for each attribute.
	- Override the method named evacuationWarningMessage and return the following string Evacuate slowly the NUMBER\_OF\_FLOORS floors.

7. Implement a class named __Airport__:

	- Constructor attributes:
		* name (String)
		* code (String)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- The default string description of the class should return the airport code.

8. Implement a class named __HolbertonClass__:

	- Constructor attributes:
		* size (Number)
		* location (String)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- When the class is cast into a Number, it should return the size.
	- When the class is cast into a String, it should return the location.

9. Fix this code and make it work.

```javascript
const class2019 = new HolbertonClass(2019, 'San Francisco');
const class2020 = new HolbertonClass(2020, 'San Francisco');

export class HolbertonClass {
  constructor(year, location) {
    this._year = year;
    this._location = location;
  }

  get year() {
    return this._year;
  }

  get location() {
    return this._location;
  }
}

const student1 = new StudentHolberton('Guillaume', 'Salva', class2020);
const student2 = new StudentHolberton('John', 'Doe', class2020);
const student3 = new StudentHolberton('Albert', 'Clinton', class2019);
const student4 = new StudentHolberton('Donald', 'Bush', class2019);
const student5 = new StudentHolberton('Jason', 'Sandler', class2019);

export class StudentHolberton {
  constructor(firstName, lastName) {
    this._firstName = firstName;
    this._lastName = lastName;
    this._holbertonClass = holbertonClass;
  }

  get fullName() {
    return `${this._firstName} ${this._lastName}`;
  }

  get holbertonClass() {
    return this.holbertonClass;
  }

  get fullStudentDescription() {
    return `${self._firstName} ${self._lastName} - ${self._holbertonClass.year} - ${self._holbertonClass.location}`;
  }
}


export const listOfStudents = [student1, student2, student3, student4, student5];
```

Result:
```plaintext
bob@dylan:~$ cat 9-main.js
import listOfStudents from "./9-hoisting.js";

console.log(listOfStudents);

const listPrinted = listOfStudents.map(
    student => student.fullStudentDescription
);

console.log(listPrinted)

bob@dylan:~$ 
bob@dylan:~$ npm run dev 9-main.js
[
  StudentHolberton {
    _firstName: 'Guillaume',
    _lastName: 'Salva',
    _holbertonClass: HolbertonClass { _year: 2020, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'John',
    _lastName: 'Doe',
    _holbertonClass: HolbertonClass { _year: 2020, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Albert',
    _lastName: 'Clinton',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Donald',
    _lastName: 'Bush',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Jason',
    _lastName: 'Sandler',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  }
]
[
  'Guillaume Salva - 2020 - San Francisco',
  'John Doe - 2020 - San Francisco',
  'Albert Clinton - 2019 - San Francisco',
  'Donald Bush - 2019 - San Francisco',
  'Jason Sandler - 2019 - San Francisco'
]
```
10. Implement a class named __Car__:

	- Constructor attributes:
		* brand (String)
		* motor (String)
		* color (String)
	- Each attribute must be stored in an “underscore” attribute version (ex: name is stored in \_name)
	- Add a method named cloneCar. This method should return a new object of the class.

__Hint__: Symbols in ES6


The code will be tested using _Jest_ and verified using ESLint.
