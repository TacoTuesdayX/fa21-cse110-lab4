# Answers to Questions in Part 1:
1. Since i is declared as var, it will be in scope at line 12. Therefore, 
i will be logged to console, which is 3 at this point, the number of discounted 
prices. 
2. Since discountedPrice is declared as var, it will be in scope at line 13.
Therefore, discountedPrice will be logged to console, which is 150 at line 13.
3. finalPrice and the console.log are in the same block, therefore 150 will
be printed.
4. The function will return the list [50, 100, 150] to the caller, which isn't
handled and thus the value is destroyed.
5. ReferenceError: i is not defined. This happens since i only has scope in the
 for loop, and not line 12.
6. ReferenceError: discountedPrice is not defined. This happens since 
discountedPrice only has scope in the for loop, and not line 13
7. 150 will be printed. This happens for finalPrice since it was declared
in the same block as line 14.
8. The function will return the list [50, 100, 150] since discounted has
scope at line 14 as it's defined in the same block.
9. The program will terminate with the error ReferenceError: i is not defined.
This occurs because i was defined with let, which only has scope in the loop.
10. The program will log 3 at line 12 since length was defined in the function
block, which is the same as line 12.
11. The function will return the list [50, 100, 150] to the caller, which isn't
handled and thus the value is destroyed.

```js
let student = {
    name: 'Sarah',
    major: 'Computer Science',
    'Grad Year': '2022',
    greeting: function() { console.log('Hello!'); },
    'Favorite Teacher': {
        name: 'Thomas Powell',
        course: 'CSE 110'
    },
    courseLoad: ['CSE 110', 'CSE 134', 'VIS 41']
};
```
- a) student.name;
- b) student['Grad Year'];
- c) student.greeting();
- d) student['Favorite Teacher'].name;
- e) student.courseLoad[0];

# Arithmetic Questions

- a) '32' - this is because 2 was converted to '2' and concatenated.
- b) 1 - this is because '3' was converted to 3 and subtracted by 2.
- c) 3 - this is because null converted to 0, and 3 - 0 = 3
- d) '3null' - this is because null converted to 'null' and concatenated.
- e) 4 - this is because true converts to 1, and is added to 3.
- f) 0 - this is because both null and false conver to 0 in integer addition,
and 0+0=0
- g) '3undefined' - this is because undefined converts to 'undefined' and is
concatenated with '3'.
- h) NaN - this occured because neither '3' or undefined are numbers, so
taking their difference will result in NaN.

# Comparison

- a) true - '2' becomes a number 2, since we're comparing diff types, and 2 > 1
- b) false - '2' and '12' are both strings, thus '2' is not lexigraphically less
than '12'.
- c) true - since we're comparing different types, 's' becomes a 
number 2 and 2 == 2.
- d) false - since '2' and 2 are of different types, they are not strictly equal.
are type string and integer respectively, and thus this is false.
- e) false - since we're comparing different types, true becomes the value 1, and 
1 == 2 is false.
- f) true - since 'true' Boolean(2) are both type boolean, and both are true
they are strictly equal. 

# Difference between == and ===

- The equality opperator '==' is used to check for equality between two values,
if the values are of different type it will attempt to convert then compare.
- The Strictly Equal operator '===' will only consider two values equal iff they
are both of the same type and equal value.

# Functions

- The result should be the modified list [2,4,6]. Essentially what happens
here is we're calling this modifyArray function with the list [1,2,3] and
the callback function doSomething(). In the modifyarray function we construct
a new list by traversing the old list and calling the callback function on
each of it's element. The call back function will multiply each element by 2,
and once returned that new value is pushed to the new list. Then the new array
is returned as well. 

## Question 19

- The values were printed in this order: 1, 4, 3, 2.

- the console.log(1) logs first synchronously, then the console.log(2) logs 2
after the duration of 1000 is comlpete, then the console.log(3) get's delayed
which executes after the synchronous console.log(4) and before 2 get's logged.