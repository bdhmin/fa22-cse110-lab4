# Devtools Part 2

1. The bug was that the input datatype were strings, so when we added, the add operator was a concatenation of two strings rather than the addition of the numbers.
2. I would fix it by changing the type of the string numbers into numbers by using `parseInt()`