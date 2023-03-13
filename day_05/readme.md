# Write a function which accepts a string argument and returns the count of characters between the first and last character 'X'
* indexOf and lastIndexOf are the methods on String which returns the position of the given string in the input string from start and end respectively
* SIf the match is not found, these methods return -1

#
<h2>Challenges (0/3 done)</h2>


 - [X] getTheGapX('XeroX') returns 4
 - [X] getTheGapX('Xamarin') returns 0
 - [X] getTheGapX('JavaScript') returns -1
 - [X] getTheGapX("F(X) !== G(X) !== F(X)") returns 18

```

const str = 'XeroX';

function getTheGapX(str) {
    if( str.lastIndexOf('X')==-1&& str.indexOf('X')==-1)
        return -1;
    else
        return str.lastIndexOf('X') - str.indexOf('X');
}
console.log(`Gap between the X's: ${getTheGapX(str)}`)


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
