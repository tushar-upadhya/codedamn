# Highest Scoring Word

## Instructions
- Given a string of words, you need to find the highest scoring word.
- Each letter of a word scores points according to its position in the alphabet: a = 1, b = 2, c = 3 etc.
- You need to return the highest scoring word as a string.
- If two words score the same, return the word that appears earliest in the original string.
- All letters will be lowercase and all inputs will be valid.

Chanllenges (0/2) done
- [ ] high('man i need a taxi up to ubud') should return 'taxi'
- [ ] high('what time are we climbing up the volcano') should return 'volcano'

```function high(x) {
  //code your magic here
  x = x.split(' ')
  let theWord = ''
  let max = 0;
  x.map((ele) => {
    let score = 0
    for(let i=0;i<ele.length;i++){ 
      score += ele.charCodeAt(i)- 96
      if(score > max) {
        max = score
        theWord = ele
      }
    }
  })
  return theWord
} 
console.log(high('what time are we climbing up the volcano'));


```
