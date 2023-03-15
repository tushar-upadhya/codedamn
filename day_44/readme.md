# Count the divisors of a number

## Instructions

- Count the number of divisors of a positive integer n.
- Examples (input --> output)

```
4 --> 3 (1, 2, 4)
5 --> 2 (1, 5)
12 --> 6 (1, 2, 3, 4, 6, 12)
30 --> 8 (1, 2, 3, 5, 6, 10, 15, 30)
```

## Challenges (0/2 done)
- [ ] getDivisorsCnt(10) should return 4
- [ ] getDivisorsCnt(11) should return 2
- [ ] getDivisorsCnt(54) should return 8

```function getDivisorsCnt(num) {
  // code below
  let arr = []
  for(let i=1;i<=num;i++){
    if(num%i==0) arr.push(i)
  }
  return arr.length;
}
console.log(getDivisorsCnt(10));

```
