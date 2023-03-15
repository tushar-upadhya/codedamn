# Write a program to find the most frequent item of an array

## Instructions

- Input : const arr = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];
- Output : a 5

## Challenges (0/2 done)
- [ ] mostFreq([1, 2, 2, 4, 5, 6, 6]) returns 2 2
- [ ] mostFreq([3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3]) returns a 5

```function mostFreq(arr) {
	// write your code here
    let maxCount = 0;
    let mapArr = new Map()
    const unique = arr.filter((ele,index) => arr.indexOf(ele) === index)
    
	for(let i=0;i<arr.length;i++) {
        let count = 0;
        for(let j=0;j<arr.length;j++){
            if(unique[i] === arr[j]) count++
        }
        if(count>1){
            maxCount = Math.max(maxCount,count)
            mapArr.set(unique[i],maxCount) 
        }
    }
    const result = [...mapArr.entries()].reduce((a, e ) => e[1] > a[1] ? e : a)
    return result.join(' ')
}

const arr = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];

console.log(mostFreq(arr));
```
