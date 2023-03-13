# Write a program to reverse a given integer number
The remainder of the number can be fetched and the number can be divided by 10 to remove the the digit in loop till number becomes 0
A simple approach to reverse a number could also be to convert it in to a string and then reverse it



# Write a program to reverse a given integer number
* The remainder of the number can be fetched and the number can be divided by 10 to remove the the digit in loop till number becomes 0
* A simple approach to reverse a number could also be to convert it in to a string and then reverse it

#
<h2>Challenges (0/3 done)</h2>


 - [X] reverseGivenInteger(3849) returns 9483
 - [X] reverseGivenInteger(2222) returns 2222
 - [X] reverseGivenInteger(1002) returns 2001

```
const num = 3849;

function reverseGivenInteger(num) {
    // write your solution here
    let st = num.toString();
    let rev_num = st.split('').reverse().join('');
    return Number(rev_num);
}

console.log(`Reversed integer is: ${reverseGivenInteger(num)}`)


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
