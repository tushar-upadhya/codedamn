# Given a number from 0 to 999,999,999,999, spell out that number in English.

## Step 1:

Handle the basic case of 0 through 99.

If the input to the program is 22, then the output should be 'twenty-two'.

Your program should complain loudly if given a number outside the blessed range.

Some good test cases for this program are:

* 0
* 14
* 50
* 98
* -1
* 100

## Step 2:
Implement breaking a number up into chunks of thousands.

So 1234567890 should yield a list like 1, 234, 567, and 890, while the far simpler 1000 should yield just 1 and 0.

The program must also report any values that are out of range.

## Step 3:
Now handle inserting the appropriate scale word between those chunks.

So 1234567890 should yield '1 billion 234 million 567 thousand 890'

The program must also report any values that are out of range. It's fine to stop at "trillion".

## Step 4:
Put it all together to get nothing but plain English.

12345 should give twelve thousand three hundred forty-five.

The program must also report any values that are out of range.

## Challenges (0/2 done)
* [ ] 14 becomes "fourteen".
* [ ] 1323 becomes "one thousand three hundred twenty-three".
```
const ones = [
  "","one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen",  "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen",
];
const tens = [
  "", "", "twenty", "thirty", "fourty", "fifty", "sixty", "seventy", "eighty", "ninety",
];
const sep = [
  "", " thousand ", " million ", " billion ", " trillion ", " quadrillion ", " quintillion ", " sextillion ",
];
  
const sayNumberInEnglish = (number) => {
    let arr = [], str = "", i = 0;
    if (number.length === 0) {
      return;
    }

    number = parseInt(number, 10);
    if (isNaN(number)) {
      return;
    }

    while(number){
      arr.push(number%1000)
      number = parseInt(number/1000,10)
    }

    while(arr.length){
      str = calc(arr.shift()) + sep[i++] + str;
    }
  
    return str;
  };

  function calc (num) {
    let x = Math.floor(num/100);
    let y = Math.floor(num/10)%10
    let z = (num%10)
    let word = (x > 0 ? ones[x] + ' hundred ' : "") + (y >= 2 ? tens[y] + '-' + ones[z] : ones[10*y+z])
    return word;
  }
  
  console.log(`5635 in english is: ${sayNumberInEnglish(5635)}`);
  


```

<!--  - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a> -->
