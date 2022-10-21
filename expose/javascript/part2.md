# Expose Part 2

1. console will log **3** because the for loop in line 6 will increment i 3 total times by the time the loop is finished. Since i is a var, not let, the variable stays accessible outside of the loop scope.
2. console will log **150** because the loop will in total calculates `100*0.5`, `200*0.5`, then `300*0.5`. The last data staying with `discountedPrice` is the third iteration of the loop, which gets us `150`.
3. console will log **150** because the loop will in total calculates `100*0.5*100/100`, `200*0.5*100/100`, then `300*0.5*100/100`. The last data staying with `discountedPrice` is the third iteration of the loop, which gets us `150`.
4. the function will return the list `[50, 100, 150]` because from the for loop in line 6, we calculate the three operations from question 3. They each equate to `50`, `100`, `150`. These numbers are pushed to the array `discounted` and this variable is then returned.
5. The function returns an Error: the variable i is not defined because it is outside of the for loop scope when it is called on line 12. `i` is instantiated by `let` and not `var`, so it is only accessible inside of the for loop.
6. The function returns an Error: the vairable `discountedPrice` was defined inside of the for loop with `let` which means it is not accessible outside of the for loop scope. So when we try to access this variable in line 13, JS doesn't know it exists.
7. The finalPrice console logs `150`. The scope of `finalPrice` is outside of the for loop which means it is still accessible by the console log. The computation is done the same as from question 3.
8. the function will return the list `[50, 100, 150]` because from the for loop in line 6, we calculate the three operations from question 3. They each equate to `50`, `100`, `150`. These numbers are pushed to the array `discounted` and this variable is then returned. Even with the `let`, the values are saved to `discounted` list while each iteration is calculated individually.
9. The function returns an Error: the vairable `i` is outside of the scope of the for loop where i is defined by a let on line 5. Same as question 5, i is only inside of the scope of the for loop.
10. The console will log **3**, which is the length of the prices array. We know that this is the length because the function in line 17 inputs an array of length 3.
11. The function returns the array `[50, 100, 150]`. The code multiplies each price input with 1 - discount which is 0.5. So the output array is just the input array where each value is divided by 2.
12. Notation
  A. `student.name`
  B. `student['Grad Year']`
  C. `student.greeting()`
  D. `student['Favorite Teacher'].name`
  E. `student.courseLoad[0]`
13. Arithmetic
  A. `'3' + 2 === '32'`. The string type in '3' takes precedence over the numeric value 2 because integers map to their exact string representation. The + is a concatenation for strings.
  B. `'3' - 2 === 1`. The subtraction tells Javascript that we are subtracting, so the string `'3'` will be then mapped back to numbers.
  C. `3 + null === 3`. The null is mapped to 0, so it becomes 3 + 0.
  D. `'3' + null === '3null'`. + is the concatenation operator for strings, so null literally maps to the word `'null'` and then '3' gets concatenated by null.
  E. `true + 3 === 4`. Since `true` can map to 1 for number arithmetic, we get `1 + 4`.
  F. `false + null === 0`. `false` is 0 and `null` is also 0 in the context of arithmetic, we get 0. It is arithmetic to Javascript because of the `+` operator.
  G. `'3' + undefined === '3undefined'`. Same as question 13D, undefined is mapped to the string version of itself because javascript sees `+` as a concatenator.
  H. `'3' - undefined === NaN`. The `-` operator tells javascript this is arithmetic. First `'3'` is converted to `3` the number, but `undefined` cannot be converted to a number. Instead it is a `NaN` (Not a Number). So the returned value also becomes `NaN`.
14. Comparison
  A. `'2' > 1 === true`. `>` operator with 1 on the right side will make `'2'` map to a number. Then comaprison continues.
  B. `'2' < '12' === false`. Now that the two sides are both strings, the values will be compared lexicographically. Since the '1' of '12' comes before '2', '12' is less than '2'.
  C. `2 == '2' === true`. the `==` checks the value of the two sides automatically mapping whichever side's type to match in order to compare. since `'2'` can map to the number `2`, the comparison is true.
  D. `2 === '2' === false`. The `===` checks the type as well as the value. Since the left side is a number and right side is a string, the types do not match so it is false.
  E. `true == 2 === false`. When compared, `true` is mapped to a number, 1. Since 1 does not equal 2, the comparison is false.
  F. `true === Boolean(2) == true`. Any number that is not 0 is considered "truthy", so if 2 is converted to a boolean, it is converted to true. So it is true.
15. The `==` is an operator that checks if two values are equal. This allows different types to be compared with the chance of them still being equal. The `===` operator checks the type of the two values, then checks the values if the types are the same.
16. Console logs `21, 45, 5, 2`
17. When `modifyArray([1,2,3], doSomething)` is called, the loop in line 3 will push the callback function with each element in the argument array `[1,2,3]`. The array with the callback functions is now returned in line 6. The callback functions that are pushed would be `[doSomething(1), doSomething(2), doSomething(3)]`. But returning this array won't actually call the callback functions yet.
18. Uses `setInterval()`
19. The console logs in the following order: `1`, `4`, `3`, `2`.