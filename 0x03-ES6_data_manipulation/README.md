# ES6 data manipulation

## This is a folder containing answers on the following topic concepts:
- Array
- Typed Array
- Set Data Structure
- Map Data Structure
- WeakMap

## These are the questions.

0. Create a function named __getListStudents__ that returns an array of objects.

Each object should have three attributes: __id__ (Number), __firstName__ (String), and __location__ (String).

The array contains the following students in order:
``` plaintext
	- Guillaume, id: 1, in San Francisco
	- James, id: 2, in Columbia
	- Serena, id: 5, in San Francisco
```
1. Create a function __getListStudentIds__ that returns an array of ids from a list of object.

This function is taking one argument which is an array of objects - and this array is the same format as __getListStudents__ from the previous task.

If the argument is not an array, the function is returning an empty array.

You must use the __map__ function on the array.

2. Create a function __getStudentsByLocation__ that returns an array of objects who are located in a specific city.

It should accept a list of students (from __getListStudents__) and a __city__ (string) as parameters.

You must use the __filter__ function on the array.

3. Create a function __getStudentIdsSum__ that returns the sum of all the student ids.

It should accept a list of students (from __getListStudents__) as a parameter.

You must use the __reduce__ function on the array.

4. Create a function __updateStudentGradeByCity__ that returns an array of students for a specific city with their new grade

It should accept a list of students (__from getListStudents__), a __city__ (String), and __newGrades__ (Array of “grade” objects) as parameters.

__newGrades__ is an array of objects with this format:
``` javascript
  {
    studentId: 31,
    grade: 78,
  }
```
If a student doesn’t have grade in __newGrades__, the final grade should be __N/A__.

You must use __filter__ and __map__ combined.

5. Create a function named __createInt8TypedArray__ that returns a new __ArrayBuffer__ with an __Int8__ value at a specific position.

It should accept three arguments: __length__ (Number), __position__ (Number), and __value__ (Number).

If adding the value is not possible the error __Position outside range__ should be thrown.

6. Create a function named __setFromArray__ that returns a __Set__ from an array.

It accepts an argument (Array, of any kind of element).

7. Create a function named __hasValuesFromArray__ that returns a boolean if all the elements in the array exist within the set.

It accepts two arguments: a __set__ (Set) and an __array__ (Array).

8. Create a function named __cleanSet__ that returns a string of all the set values that start with a specific string (__startString__).

It accepts two arguments: a __set__ (Set) and a __startString__ (String).

When a value starts with startString you only append the rest of the string. The string contains all the values of the set separated by __-__.

9. Create a function named __groceriesList__ that returns a map of groceries with the following items (name, quantity):

``` plaintext
Apples, 10
Tomatoes, 10
Pasta, 1
Rice, 1
Banana, 5
```

Result:

``` plaintext
Map {
  'Apples' => 10,
  'Tomatoes' => 10,
  'Pasta' => 1,
  'Rice' => 1,
  'Banana' => 5
}
```

10. Create a function named __updateUniqueItems__ that returns an updated map for all items with initial quantity at 1.

It should accept a map as an argument. The map it accepts for argument is similar to the map you create in the previous task.

For each entry of the map where the quantity is 1, update the quantity to 100. If updating the quantity is not possible (argument is not a map) the error __Cannot process__ should be thrown.

- * The  code will be tested using jest and the command npm run test.
- * The code will be verified using ESLint.
