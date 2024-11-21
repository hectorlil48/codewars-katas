# Convert a Number to a String!

**Difficulty**: 8 kyu  
**Link**: [Kata Link](https://www.codewars.com/kata/5265326f5fda8eb1160004c8/solutions/javascript?filter=me&sort=best_practice&invalids=false)

---

### Problem Description

We need a function that can transform a number (integer) into a string.

Examples (input --> output):
123 --> "123"
999 --> "999"
-100 --> "-100"

---

### Plan

1.  Create a function that takes a number.
2.  Set a variable that holds the str using .toString() on num
3.  retrun the str

---

### Code

```javascript
// Your solution code
function numberToString(num) {
  let str = num.toString();
  return str;
}
```

---

### Explanation

The function takes a number as input. It creates a new variable called str, which serves as a container to hold the number converted to a string using the .toString() method. Finally, it returns str so it can be used elsewhere.

---

### Reflection

This one was a pretty easy one. Once I found out what .toString() method could do. All i needed was a new varaible to store the string.
