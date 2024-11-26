# Create Phone Number

**Difficulty**: 6 kyu  
**Link**: [Kata Link](https://www.codewars.com/users/hectorlil48/completed_solutions)

---

### Problem Description

Write a function that accepts an array of 10 integers (between 0 and 9), that returns a string of those numbers in the form of a phone number.

Example
createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]) // => returns "(123) 456-7890"
The returned format must be correct in order to complete this challenge.

Don't forget the space after the closing parentheses!

---

### Plan

1. Create a function that takes an array of 10 numbers between 0 and 9.
2. Set an empty string named phoneNumber.
3. Loop through the array passed in.
4. Set a num variable to the array's current index value.
5. Check if the index is 0:
   - If true, add the starting parenthesis "(" and the current index value to the phoneNumber variable.
6. Check if the index is 2:
   - If true, add the current index value to the phoneNumber variable, followed by the closing parenthesis ")" and a space " ".
7. Check if the index is 5:
   - If true, add the current index value to the phoneNumber variable, followed by a dash "-".
8. Otherwise:
   - Just add the current index value to phoneNumber.
9. Return phoneNumber.

---

### Code

```javascript
function createPhoneNumber(numbers) {
  let phoneNumber = "";

  for (let i = 0; i < numbers.length; i++) {
    let num = numbers[i];

    if (i === 0) {
      phoneNumber += "(" + num;
    } else if (i == 2) {
      phoneNumber += num + ") ";
    } else if (i === 5) {
      phoneNumber += num + "-";
    } else {
      phoneNumber += num;
    }
  }
  return phoneNumber;
}
```

---

### Explanation

This function formats an array of 10 digits into a U.S. phone number format (XXX) XXX-XXXX by iterating through the array and building the formatted string step by step.

Function Declaration
The function is designed to accept an array of 10 numbers as its parameter. These numbers must be between 0 and 9.

Initialize an Empty String
A variable named phoneNumber is initialized as an empty string. This will be used to construct the formatted phone number.

Loop Through the Array
The function iterates through the array using a loop. At each step of the loop, the function:

Retrieves the current index value from the array.
Checks specific conditions based on the index position.
Formatting the Phone Number

Index 0:
If the current index is 0, the function adds an opening parenthesis ( and the current number to the phoneNumber string.
Example: "(1"

Index 2:
If the current index is 2, the function adds the current number, followed by a closing parenthesis ) and a space " ".
Example: "(12)" becomes "(12) "

Index 5:
If the current index is 5, the function adds the current number, followed by a dash "-".
Example: "(123) 45" becomes "(123) 45-"

Other Indices:
For all other indices, the function simply appends the current number to the phoneNumber string.

Return the Result
After the loop completes, the fully formatted phoneNumber string is returned.

---

### Reflection

This exercise helped me practice logical thinking and string manipulation in JavaScript. Breaking the task into steps made the code organized and easy to follow. Using conditionals within a loop effectively handled different parts of the phone number format, ensuring clarity.

What worked well:

The logic was straightforward, and the code was readable.
The conditions for specific indices ensured the correct formatting.
What could improve:

Adding input validation for exactly 10 digits.
Making the function more flexible to handle other phone number formats.
Overall, this was a valuable exercise that reinforced core programming skills while showing areas for potential enhancement.
