(“var” variable is either entire function scoped or global scoped regardless of block scope)
1.i is a “var” variable and is inside the function so it is a function scoped variable. Therefore, it prints the value of i for last iteration.

2.discountedPrice is a “var” variable and is inside the function so it is a function scoped variable. For each iteration of the loop, discountedPrice is redeclared, so it prints for the last iteration.

3.finalPrice is a “var” variable and is inside the function so it is a function scoped variable. For each iteration of the loop, finalPrice is redeclared, so it prints for the last iteration.

4.It returns [ 50, 100, 150 ]. The function returns discounted which is a “var” variable and is declared in the function, so it is a function scoped variable. For every iteration of loop, it pushes the finalPrice for corresponding prices[i]. As a result, 0.5 discount gives the price 50, 100, 150 in order.

(“let” variable is limited to the scope of a block statement)
5.i is a “let” variable and is declared inside the loop statement so it is not defined after the loop. It will not print anything and report an error.

6.discountedPrice is a “let” variable and is declared inside the loop statement so it is not defined after the loop. It will not print anything and report an error.

7. finalPrice is a “let” variable and is defined in function block so it is a function scoped variable. For each iteration of the loop, finalPrice is redeclared, so it prints for the last iteration.

8.It returns [ 50, 100, 150 ]. The function returns discounted which is a “let” variable and is declared in the function scope, so it is a function scoped variable. For every iteration of loop, it pushes the finalPrice for corresponding prices[i]. As a result, 0.5 discount gives the price 50, 100, 150 in order.

(“const” variable is similar to “let” variable that it comes to block scope. “const” variable cannot be reassigned.)
9.i is a “let” variable and is declared inside the loop statement so it is not defined after the loop. It will not print anything and report an error.

10.discountedPrice is a “const” variable and is declared inside the loop statement so it is not defined after the loop. It will not print anything and report an error.

11. finalPrice is a “const” variable and is defined in function block so it is a function scoped variable. Since, “const” variable cannot be reassigned, but we assume the assignment is successful. For each iteration of the loop, finalPrice is redeclared, so it prints for the last iteration. 

12.There is an error since line 7 that “const” variable cannot be reassigned. If we assume that the assignment is successful, it will return [ 50, 100, 150 ]. If we assume that the assignment fails, it will return [ 0, 0 ,0 ] since “const” finalPrice which is 0 is added to discounted.

13(a) student.name
  (b) student[“Grad Year”]
  (c) student.greeting()
  (d) student[“Favorite Teacher”].name
  (e) student.courseLoad[0]

14(a) 32  The addition operator concatenates string 3 and number 2 which is converted to a string.
(b) 1  The subtraction operator subtracts string 3 which is converted to number 3 with number 2.
(c) 3  The addition operator adds number 3 and null which is converted to 0.
(d) 3null  The addition operator concatenates string 3 and null which is converted to a string “null”.
(e) 4  The addition operator adds true which is converted to 1 and number 3.
(f) 0  The addition operator adds false which is converted to 0 and null which is also converted to 0.
(g) 3undefined  The addition operator concatenates string 3 and undefined which is converted to a string “undefined”.
(h) NaN   The subtraction operator subtracts string 3 which is converted to number 3 with undefined which is converted NaN. And 3+NaN is still NaN.

15(a) true  String 2 becomes number 2 and 2 > 1.
(b) false  First compare the first character of both strings, ‘2’ > ‘1’ so return false.
(c) true  Convert both to values and 2 == 2 so return true.
(d) false  === checks the equality without type conversion and, since a number is not a string, return false.
(e) false  true is converted to number 1 and 1 != 2.
(f) true  Boolean(2) is true, and true is definitely equal to true.

16.For non-strict equality check, use == which converts both sides to numbers. For strict equality check, use === which checks equality without type conversion that different types will return false.

17.It prints ‘How are you?’. For the first if statement (2 == true), == converts both sides to numbers that is to check 1 == 2 which returns false. Enter the else if statement, check if 2 is true that 2 > 0 so enter the else if statement and print ‘How are you?’. 

18.See code here or part1-question18.js.

19.It returns [6,8,10]. The input array is [1,2,3] of length 3 and the function doSomething. For each iteration, newArr pushes doSomething(the ith element in array, function 2*x). For the first element 1, first do 1+2 = 3 as input parameter for callback in doSomething, then call the function 3*2 = 6. Finally, newArr pushes 6. Similarly, push (2+2)*2=8, and (3+2)*2=10 into newArr. Return newArr which is [6,8,10].

20.
let d = new Date();
let time = d.toLocaleTimeString();
setInterval(function(){console.log(time)},1000)

21. Print as following:
1
4
3
2
