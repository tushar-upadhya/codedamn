# Sum of two lowest positive integers

## Instructions

- Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 positive integers. No floats or non-positive integers will be passed.
- For example, when an array is passed like [19, 5, 42, 2, 77], the output should be 7.

## Challenges (0/2 done)
- [ ] sumTwoSmallestNumbers([5, 8, 12, 19, 22]) should return 13
- [ ] sumTwoSmallestNumbers([15, 28, 4, 2, 43]) should return 6
- [ ] sumTwoSmallestNumbers([23, 71, 33, 82, 1]) should return 24

```function sumTwoSmallestNumbers(numbers) {
    //Code below
    numbers.sort((a,b)=>a-b)
    return numbers[0]+numbers[1]
  }
 console.log( sumTwoSmallestNumbers([19, 5, 42, 2, 77]));
```
