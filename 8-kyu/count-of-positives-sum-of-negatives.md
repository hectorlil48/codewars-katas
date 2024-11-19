# Count of Positives / sum of negatives

**Difficulty**: 8 kyu  
**Link**: [Kata Link](https://www.codewars.com/kata/576bb71bbbcf0951d5000044/solutions/javascript?filter=me&sort=best_practice&invalids=false)

---

### Problem Description

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers. 0 is neither positive nor negative.

If the input is an empty array or is null, return an empty array.

Example
For input [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15], you should return [10, -65].

---

### Plan

1. Check to see if input array is empty or a null value. If it is either, return empty array.
2. Set countOfPositives and sumOfNegatives equal to zero.
3. Loop through the length of the input array.
4. Check each number in the array to see if it is greater than zero.
   - If greater, add one to countOfPositives.
5. Check each number in the array to see if it is less than zero.
   - If less, then add the number of the array to sumOfNegatives.
6. Return the countOfPositives and sumOfNegatives in a new array.

---

### Code

```javascript
// Your solution code
function countPositivesSumNegatives(input) {
  if (!input || input.length === 0) {
    return [];
  }

  let countOfPositives = 0;
  let sumOfNegatives = 0;

  for (let i = 0; i < input.length; i++) {
    if (input[i] > 0) {
      countOfPositives++;
    } else if (input[i] < 0) {
      sumOfNegatives += input[i];
    }
  }

  return [countOfPositives, sumOfNegatives];
}

let testData = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15];

console.log(countPositivesSumNegatives(testData));
```

---

### Explanation

The function takes an array as input. It first checks if the input is either empty or not an array. If either condition is true, it returns an empty array. Next, the function loops through the array to examine each number. It checks whether the numbers are greater than zero or less than zero. If a number is greater than zero, it increments the countOfPositives variable by one. If a number is less than zero, it adds the value of that number to the sumOfNegatives variable. After completing the loop, the function returns an array containing countOfPositives and sumOfNegatives.

---

### Reflection

I practiced working with arrays and learned how to loop through them to examine each number. I also gained experience using conditionals to perform various checks within the array. I want to continue practicing to improve my skills and become more proficient.
