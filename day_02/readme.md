# Write a program to reverse a string
# String can be reversed by iterating it and storing it in reverse order
# String can also be reversed by converting it to array, then joining it after reversing


<h2>Challenges (0/3 done)</h2>


 - [X] reverseAString("JavaScript is awesome") should return "emosewa si tpircSavaJ"
 - [X] reverseAString("Peter Parker is Spiderman") should return "namredipS si rekraP reteP"
 - [X] reverseAString("codedamn") should return "nmadedoc"

```
const str = "JavaScript is awesome"

function reverseAString(str) {
    // write your solution here

    let reversed =""
    for(let i =str.length -1; i>=0;i--){
        reversed += str[i];
    }
    return reversed

}

console.log(`Reversed string is: ${reverseAString(str)}`)


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
