# Who likes it

**Difficulty**: 6 kyu  
**Link**: [Kata Link](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/solutions/javascript?filter=me&sort=best_practice&invalids=false)

---

### Problem Description

You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

[] --> "no one likes this"
["Peter"] --> "Peter likes this"
["Jacob", "Alex"] --> "Jacob and Alex like this"
["Max", "John", "Mark"] --> "Max, John and Mark like this"
["Alex", "Jacob", "Mark", "Max"] --> "Alex, Jacob and 2 others like this"
Note: For 4 or more names, the number in "and 2 others" simply increases.

---

### Plan

1.  Create a function that takes an array.
2.  Check if the array is empty.
    - if empty return "no one likes this".
3.  Check if the array length is 1.
    - return array[0] likes this.
4.  Check if the array length is 2.
    - return array[0] and array[1] like this.
5.  Check if the array length is 3.
    - return array[0], array[1] and array[2] like this.
6.  Check if the array length is 4.
    - return array[0], array[1] and array.length - 2 others like this

---

### Code

```javascript
function likes(names) {
  if (names.length === 0) return "no one likes this";
  else if (names.length === 1) return `${names[0]} likes this`;
  else if (names.length === 2) return `${names[0]} and ${names[1]} like this`;
  else if (names.length === 3)
    return `${names[0]}, ${names[1]} and ${names[2]} like this`;
  else
    return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
}
```

---

### Explanation

The function determines and returns the appropriate text describing who likes a post based on the input array of names:

Empty Array: If the array is empty (names.length === 0), it returns "no one likes this".
One Name: If the array has one element (names.length === 1), it returns the name with "likes this", e.g., "Peter likes this".
Two Names: If the array has two elements (names.length === 2), it returns both names separated by "and", followed by "like this", e.g., "Jacob and Alex like this".
Three Names: If the array has three elements (names.length === 3), it returns the first two names separated by a comma, then the third name with "and", followed by "like this", e.g., "Max, John and Mark like this".
Four or More Names: If the array has four or more elements (names.length > 3), it returns the first two names, followed by the count of additional people (names.length - 2) with "and X others like this", e.g., "Alex, Jacob and 2 others like this".

---

### Reflection

Reflecting on my implementation of the likes function, I feel it effectively addresses the problem requirements and handles all edge cases systematically. Each conditional statement serves a specific purpose, ensuring the appropriate message is returned based on the length of the input array.

Through writing this function, I reinforced the importance of clear and concise logic when solving problems with multiple scenarios. Breaking down the conditions based on array length made the code more readable and straightforward. Additionally, utilizing string interpolation (${}) made the output dynamic and clean, enhancing both efficiency and readability.

One area for improvement is the ability to streamline the explanation and code for greater clarity. For instance, I could consider using a switch statement or mapping lengths to specific formats for added elegance. Furthermore, thinking ahead to how this logic might scale—such as supporting different languages or customizing the output—could make the solution even more versatile.

Overall, this exercise helped me sharpen my problem-solving skills and practice writing robust, reusable functions. It's a reminder of how important it is to write code that not only works but is easy to understand and maintain.
