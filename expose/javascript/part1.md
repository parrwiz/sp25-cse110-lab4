Answer 1: 
1: values added:  20
2: final result:  20
3: You shouldn't use var because it doesn’t limit the variable to just the block where it’s declared. Instead, var makes the variable accessible anywhere in the function, even outside the if or for block where you defined it which can cause bugs.


Answer 2: 
4: values added:  20
5: The error happens because let is block scoped, which means the variable result only exists inside the if (add) block. When you try to access result outside of that block, like in the last console.log, it no longer exists, so JavaScript throws a ReferenceError. To fix this, you’d need to declare result outside the if block so it’s available throughout the whole function.


Answer 3: 

6:  Nothing is printed because the line before it (result = num1 + num2;) causes a TypeError. The variable result was declared using const, which means it can’t be reassigned. Since the code tries to change its value, the program crashes before reaching the console.log.

7:Also nothing, because the function crashes earlier due to the error on line 7. The code never makes it past that point, so line 13 is never executed.