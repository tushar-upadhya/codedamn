# Write a function which can convert the time input given in 12 hours format to 24 hours format
* The check for 'AM' and 'PM' can be verified using endsWith String method
* An extra 0 would be needed if the hours have single digit

#
<h2>Challenges (0/3 done)</h2>


 - [X] convertTo24HrsFormat("12:10AM") returns "00:10"
 - convertTo24HrsFormat("5:00AM") returns "05:00"
 - [X] convertTo24HrsFormat("12:33PM") returns "12:33"
 - [X] convertTo24HrsFormat("01:59PM") returns "13:59"
 - [X] convertTo24HrsFormat("11:08PM") returns "23:08"
 - [X] convertTo24HrsFormat("10:02PM") returns "22:02"

```const time = '12:10AM';

function convertTo24HrsFormat(time) {
    // write your solution here
    if (time.length === 6) {
        if (time.charAt(2) == ':')
            time = time.slice(0, 3) + '0' + time.slice(3);
        else
            time = '0' + time;
    }

    let new_time;
    if (time.slice(-2) === 'AM') {
        if (time.slice(0, 2) === '12')
            new_time = '00' + time.slice(2, 5);
        else
            new_time = time.slice(0, 5);
    }
    else {
        if (time.slice(0, 2) === '12')
            new_time = time.slice(0, 5);
        else {
            let hr = (Number(time.slice(0, 2)) + 12).toString();
            new_time = hr + time.slice(2, 5);
        }
    }
    return new_time;
}

console.log(`Converted time: ${convertTo24HrsFormat(time)}`)


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
