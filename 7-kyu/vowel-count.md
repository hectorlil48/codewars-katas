# Vowel Count

**Difficulty**: 7 kyu  
**Link**: [Kata Link](https://www.codewars.com/kata/54ff3102c1bad923760001f3/solutions/javascript?filter=me&sort=best_practice&invalids=false)

---

### Problem Description

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.

---

### Plan

1. Create a function that takes a string.
2. Check if the string is empty.
   - if empty return a 0.
3. Set a count variable set to 0.
4. Set an array of characters to check.
   - set charsToCheck = ["a", "e", "i", "o", "u"];
5. Loop through each letter in the string.
6. Check to see if any letter in the string is in the charsToCheck array.
   - If it is then add one to count.
7. Return count.

---

### Code

```javascript
function getCount(str) {
  if (str === "") {
    return 0;
  }

  let count = 0;
  let charsToCheck = ["a", "e", "i", "o", "u"];

  for (let char of str) {
    if (charsToCheck.includes(char)) {
      count++;
    }
  }

  return count;
}
```

---

### Explanation

This function takes a string. Checks to see if the string is empty, if it is then it returns 0. It sets up a variable called count that is set to 0. It sets an array of characters, that include ["a", "e", "i", "o", "u"]. Using a for of loop, it check's every letter inside the string. If any letter that matches any of the characters inside the array, then it adds one to the count variable. After the loop is finished, it returns the count variable.

---

### Reflection

While working on the getCount function, I deepened my understanding of fundamental programming concepts such as iteration, conditionals, and the use of helper methods like .includes(). I learned how to break down a problem into smaller, manageable steps, like identifying vowels and counting their occurrences in a string.

I also realized the importance of handling edge cases, such as checking for an empty string at the start. This made the function more robust and reliable. Using modern JavaScript features like the for...of loop improved readability, making the code cleaner compared to traditional for loops.

Additionally, this task highlighted how simple data structures like arrays can simplify logic. I learned that storing vowels in an array not only made the code flexible but also reduced hardcoding, which is a good coding practice.

Lastly, reflecting on potential improvements, such as case insensitivity, showed me how to evaluate my code critically for scalability and usability. This process reinforced the importance of writing adaptable and maintainable code.
