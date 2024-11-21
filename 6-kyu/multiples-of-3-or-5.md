# Multiples of 3 or 5

**Difficulty**: 6 kyu  
**Link**: [Kata Link](https://www.codewars.com/users/hectorlil48/completed_solutions)

---

### Problem Description

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

Additionally, if the number is negative, return 0.

Note: If the number is a multiple of both 3 and 5, only count it once.

---

### Plan

1.  Create a function that takes a number.
2.  Check number if its a negative return a 0.
3.  Set up a sum variable to equal 0.
4.  Loop through the number.
5.  Each number in the range is checked to determine whether it is divisible by 3 or 5.
6.  If either condition is satisfied, the number will get added to sum.
7.  Return the sum

---

### Code

```javascript
function solution(number) {
  if (number < 0) {
    return 0;
  }

  let sum = 0;

  for (let i = 0; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
}
```

---

### Explanation

The function takes a number as input and first checks if it is less than zero. If this condition is true, the function returns 0. Next, it initializes a variable named sum to store the running total, starting at 0. The function then loops through all numbers from 0 up to (but not including) the given number. During each iteration, it checks if the current number is a multiple of 3 or 5. If the condition is satisfied, the number is added to sum.

---

### Reflection

Through this problem, I learned how to use loops and conditions to solve real-world challenges. I practiced checking if numbers met specific criteria, like being divisible by 3 or 5, and adding them to a total. I also learned the importance of handling edge cases, such as returning 0 for negative numbers. This problem helped me improve my coding skills and write cleaner, more efficient code.
