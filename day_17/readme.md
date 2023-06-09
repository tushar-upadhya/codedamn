# Longest Consecutive Sequence

- Given an array of elements, find a subsequence in the array such that all the elements in the sequence are consecutive irrespective of their order.

## Example

- Input: [100,4,200,1,3,2]

- Output: 4 // LCS [1, 2, 3, 4]

## Conceptually this is how it should work.
- Copy all the elements of the array in a set. Iterate the array and in each iteration determine if the current element will lead to new subsequence by checking if there is no element less than the current, present in the set. 

- Then find how long this subsequence can be by incrementing the count till there is consecutive elements in the set. In the end return the longest consecutive sequence.

## Challenges (0/2 done)
- [ ] longestConsecutiveSequence([100,4,200,1,3,2]) returns 4
- [ ] longestConsecutiveSequence([0,3,7,2,5,8,4,6,0,1]) returns 9

```/**
 *
 * @param {number[]} inputArray Array of numbers
 */
 const longestConsecutiveSequence = (inputArray) => {
    let sortedArr = inputArray.sort(function(a, b){return a-b});
    let currSeq = 0;
    let maxSeq = 0;
    mySet = new Set([...sortedArr])
    sortedArr = [...mySet]
    if(sortedArr.length === 0) return 0;
    for(let i=0;i<sortedArr.length-1;i++){
        if(sortedArr[i+1] - sortedArr[i] === 1) {
            currSeq = currSeq+1;
            maxSeq = Math.max(maxSeq,currSeq)
        }else{
            currSeq = 0;
        }
    }
    return maxSeq+1;
}
```
