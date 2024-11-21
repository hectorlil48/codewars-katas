# Grasshopper - Grade book

**Difficulty**: 8 kyu  
**Link**: [Kata Link](https://www.codewars.com/users/hectorlil48/completed_solutions)

---

### Problem Description

Grade book
Complete the function so that it finds the average of the three scores passed to it and returns the letter value associated with that grade.

Numerical Score Letter Grade
90 <= score <= 100 'A'
80 <= score < 90 'B'
70 <= score < 80 'C'
60 <= score < 70 'D'
0 <= score < 60 'F'
Tested values are all between 0 and 100. Theres is no need to check for negative values or values greater than 100.

---

### Plan

1.  Create a function that takes 3 numbers.
2.  Find the average of the numbers.
3.  Check average.
4.  average >= 90: return "A"
5.  average >= 80: return "B"
6.  average >= 70: return "C"
7.  average >= 60: return "D"
8.  Else return "F"

---

### Code

```javascript
function getGrade(s1, s2, s3) {
  let average = parseInt((s1 + s2 + s3) / 3);

  if (average >= 90) {
    return "A";
  } else if (average >= 80) {
    return "B";
  } else if (average >= 70) {
    return "C";
  } else if (average >= 60) {
    return "D";
  } else {
    return "F";
  }
}
```

---

### Explanation

The function takes three numbers as input. It calculates the average of these numbers and stores it in the average variable. Then, it checks the average against a set of conditions. Based on the condition that the average meets, the function returns the corresponding letter associated with that condition.

---

### Reflection

This problem was pretty straightforward. I had to calculate the average and check if it matched any conditions. I got to work with functions and conditionals, and I can feel myself getting better at using them. It was a good exercise to reinforce these concepts.
