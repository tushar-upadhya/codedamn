# Write a function to truncate a string to a certain number of words
* String can be reversed by iterating it and storing it in reverse order
* String can also be reversed by converting it to array, then joining it after reversing

#
<h2>Challenges (0/3 done)</h2>


 - [X] truncateWithWordLimit("JavaScript is simple", 3) returns "JavaScript is simple"
 - [X] truncateWithWordLimit("Codedamn is the best place to learn to code", 5) returns "Codedamn is the best place"
<!--  - [X] reverseAString("codedamn") should return "nmadedoc" -->

```
const str = 'JavaScript is simple but not easy to master';
const wordLimit = 3

function truncateWithWordLimit(str, wordLimit) {
    str = " " + str; let k = 0; let s = "";
    for (let i = 0; i < str.length; i++) {
        if (str.charAt(i) == " ")
            k++;
        if (k > wordLimit)
            break;
        s = s + str.charAt(i);
    }
    return s.trim();
}

console.log(`Truncated string: ${truncateWithWordLimit(str, wordLimit)}`)


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
