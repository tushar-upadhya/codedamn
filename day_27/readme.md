# Vowel Count

## Instructions
- Return the number (count) of vowels in the given string.
- We will consider a, e, i, o, u as vowels
- The input can consit of Lower case and upper case letters so make sure to count both of them.

## Challenges (0/3) done
- [ ] getCount("abracadabra") should return 5
- [ ] getCount("THe Strings are SOO COOL") should return 8
- [ ] getCount("There exists only 5 vowels") should return 7

```function getCount(str) {
  let vowelsCount = 0;
  // enter your magic here
  str = str.toLowerCase();
  let strChar = str.split("");
  for(let i = 0; i< strChar.length; i++) {
      if(strChar[i] === 'a' || strChar[i] === 'e' || strChar[i] === 'i' || strChar  [i] === 'o' || strChar[i] === 'u') {
          vowelsCount++;
      }
  }

  return vowelsCount;
}

console.log(getCount("abracadabra"));

```
