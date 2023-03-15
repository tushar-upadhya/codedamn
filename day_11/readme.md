# Return the N-th value of the Fibonacci sequence
* Return the N-th value of the Fibonacci sequence
<!-- * String can also be reversed by converting it to array, then joining it after reversing -->

#
<h2>Challenges (0/3 done)</h2>


 - [X] function fibonacci(n) returns the N-th value of the Fibonacci sequence
<!--  - [X] reverseAString("Peter Parker is Spiderman") should return "namredipS si rekraP reteP" -->
<!--  - [X] reverseAString("codedamn") should return "nmadedoc" -->

```
function fibonacci(n) {
    if (n == 0)
        return 0;
    if (n <= 2)
        return 1;

    var a = 1, b = 1, c;
    for (var i = 3; i <= n; i++) {
        c = a + b;
        a = b;
        b = c;
    }
    return c;
}
console.log(`fibonacci value at position 5: ${fibonacci(5)}`)



```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
