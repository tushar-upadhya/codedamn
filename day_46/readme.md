# A Needle in the Haystack

## Instructions
- Write a function findNeedle() that takes an array full of junk but containing one "needle"
- After your function finds the needle it should return a message (as a string) that says: "found the needle at position " plus the   index it found the needle, so:
findNeedle(['hay', 'junk', 'hay', 'hay', 'moreJunk', 'needle', 'randomJunk']) should return "found the needle at position 5"

## Examples
- [2, 4, 0, 100, 4, 11, 2602, 36] Should return: 11 (the only odd number)

- [160, 3, 1719, 19, 11, 13, -21] Should return: 160 (the only even number)

## Challenges (0/3 done)
- [ ] findNeedle(['3', '123124234', undefined, 'needle', 'world', 'hay', 2, '3', true, false]) should return 'found the needle at position 3'
- [ ] findNeedle(['283497238987234', 'a dog', 'a cat', 'some random junk', 'a piece of hay', 'needle', 'something somebody lost a while ago']) should return 'found the needle at position 5'
- [ ] findNeedle([1,2,3,4,5,6,7,8,8,7,5,4,3,4,5,6,67,5,5,3,3,4,2,34,234,23,4,234,324,324,'needle',1,2,3,4,5,5,6,5,4,32,3,45,54]) should return 'found the needle at position 30'

```function findNeedle(haystack) {
  // your code here
  let foundAt = 0;
  haystack.forEach((ele,index) => {
      if(ele == 'needle'){
        foundAt = index
        return;
      }
  })
  return `found the needle at position ${foundAt}`
}
```
