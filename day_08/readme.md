# Write a function which accepts two valid dates and returns the difference between them as number of days
* The difference between 2 dates in JavaScript will give the time difference in milliseconds
* Time difference can be converted in to days by dividing the 24Hrs time in milliseconds


<h2>Challenges (0/3 done)</h2>


  - [X] getDaysBetweenDates('10/15/2020', '12/1/2020') returns 47
  - [X] getDaysBetweenDates('11/10/2021', '11/12/2021') returns 2
  - [X] getDaysBetweenDates('11/01/2020', '11/05/2020') returns 4
<!--   - [X] validateMobile('9876543210') returns true -->
<!--   - [X] validateMobile('99876543210') returns false -->

```
const DAY_IN_MILLISECONDS = 1000 * 60 * 60 * 24;

function getDaysBetweenDates(dateText1, dateText2) {
    var date1 = new Date(dateText1);
    var date2 = new Date(dateText2);
    var diff = Math.abs(date2 - date1);

    return(diff/DAY_IN_MILLISECONDS);
}

console.log(`Days difference: ${getDaysBetweenDates('10/15/2020', '12/1/2020')}`)
```
