# Get the Middle Character

## Instructions
- You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

```
Kata.getMiddle("test") should return "es"

Kata.getMiddle("testing") should return "t"

Kata.getMiddle("middle") should return "dd"

Kata.getMiddle("A") should return "A"
```

## Challenges (0/3 done)
- [ ] getMiddle("testing") should return "t"
- [ ] getMiddle("middle") should return "dd"
- [ ] getMiddle("A") should return "A"

```function getMiddle(s) {
  // your code here
  const n = s.length
  const mid = Math.floor(n/2)
  if(n==1) return s
  if(n%2!=0) return s[mid]
  else return s.slice(mid-1,mid+1)
}

console.log(getMiddle("testing"));
```
