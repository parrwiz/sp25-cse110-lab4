Answer 1: 3
On line 12, console.log(i) runs after the for loop ends. Since i is declared using var, which is function scoped (not block scoped), it still exists outside the loop. The loop ends when i becomes 3 (because prices.length is 3), so: console.log(i); // prints: 3

Answer2: 150
The discountedPrice will be printed: which is 150. Line 13 prints 150 because discountedPrice is declared with var, which is function scoped. That means the variable still exists even after the for loop finishes. Inside the loop, the last time discountedPrice is updated is when the price is 300, and applying the 50% discount gives 150. So when console.log(discountedPrice) runs, it prints that final value. There’s no error, and the program works as expected.

Answer3: 150
Even though finalPrice is calculated inside the loop, it's declared with var, which is function scoped. That means it’s still accessible after the loop finishes. Since the last value it was set to was Math.round(300 * 0.5 * 100) / 100, which simplifies to 150, that’s what gets printed. No errors happen, and the code runs fine.

Answer4: Nothing is printed because the call at the bottom isn't wrapped in a console.log(), so the return value isn't displayed. However, the function will return [50, 100, 150], which are the final discounted prices. Each original price is multiplied by (1 - 0.5), giving you half of each: 100 → 50, 200 → 100, 300 → 150. These values are rounded and pushed into the discounted array. So while the function works perfectly and returns the correct result, it silently finishes without showing any output. 

Answer 5: 
Nothing is printed because the function is never called. Even though there’s a console.log(i) inside the function, JavaScript won’t run it unless the function is explicitly executed. Since the function is only defined and not invoked, the code runs silently without any output or errors.also there is a let so if the function would have been called, a ReferenceError would have occured.

Answer 6: 
Line 13 causes a ReferenceError because discountedPrice is declared using let inside the for loop, making it block scoped. This means the variable only exists during each loop iteration and is not accessible outside of that block. When console.log(discountedPrice) tries to access it after the loop ends, JavaScript throws an error because the variable no longer exists.

Answer 7: 150
Line 14 prints 150 because finalPrice is declared using let outside of the for loop, so it remains accessible after the loop finishes. Each loop iteration updates finalPrice, and on the last one, it gets the value 150 from the discounted price of 300. Since the variable is still in scope, console.log(finalPrice) runs successfully and prints the last assigned value.

Answer 8: 
The function returns [50, 100, 150]. It loops through the input array, applies a 50% discount to each price, rounds the result, and stores each in the discounted array. All variables are declared with let and used in the correct scope, so no errors occur. However, nothing is printed because the return value isn’t wrapped in a console.log() the function runs and returns the correct result, but it finishes silently without showing anything in the terminal.

Answer 9:
Line 11 causes a ReferenceError because the variable i is declared using let inside the for loop, which makes it block scoped. That means i only exists during the loop and is not accessible afterward. When the code tries to log i after the loop ends, JavaScript throws an error since i no longer exists in that scope.

Answer 10:
Line 12 prints 3 because length is declared using const and assigned the value prices.length, which is 3 in this case. Since length is accessible throughout the function scope and nothing overrides it, console.log(length) runs successfully without any errors. The function logic might be flawed elsewhere, but this specific line works correctly and prints the expected output.

Answer11:
The function returns an array containing three references to the function discountPrices itself. This happens because instead of pushing the calculated discounted price, the code mistakenly pushes the function name. JavaScript allows functions to be treated like values, so no error occurs. However, since the return value isn’t wrapped in a console.log(), nothing is printed to the screen even though the function returns a valid array.


Answer12:
A: student.name
B: student['Grad Year']
C: student.greeting()
D: student['Favorite Teacher'].name
E: student.courseLoad[0]


Answer13:
A: '3' + 2 = 32
B: '3' - 2 = 1
C: 3 + null = 3
D: '3' + null = 3null
E: true + 3 = 4
F: false + null = 0
G: '3' + undefined = 3undefined
H: '3' - undefined = NaN

Answer14:
A: '2' > 1 = true
B: '2' < '12' = false
C: 2 == '2' = true
D: 2 === '2' = false
E: true == 2 = false
F: true === Boolean(2) = true


Answer15:
== checks if two values are equal after type conversion, so '2' == 2 is true.
=== checks for both type and value, so '2' === 2 is false because one is a string and the other is a number.

Answer16:
21
45
5
2


Answer17:
Since there is no console.log() around the function call, nothing prints to the screen, but the function itself works correctly and returns the expected array. The result of modifyArray([1, 2, 3], doSomething) will be [2, 4, 6]. The modifyArray function loops through each element of the input array and applies the doSomething callback to it. In this case, the doSomething function simply doubles the input number (num * 2). So for the array [1, 2, 3], each value becomes 2, 4, and 6, which are collected into a new array and returned.


Answer18:
setInterval()=> can be use, implemented in part2-question18.js.


Answer19:
1
4
3
2

