# Find the odd int

## Instruction
- Given an array of integers, find the one that appears an odd number of times.
- There will always be only one integer that appears an odd number of times.
- For example:
- [7] should return 7, because it occurs 1 time (which is odd). [0] should return 0, because it occurs 1 time (which is odd). [1,1,2] should return 2, because it occurs 1 time (which is odd). [0,1,0,1,0] should return 0, because it occurs 3 times (which is odd). [1,2,2,3,3,3,4,3,3,3,2,2,1] should return 4, because it appears 1 time (which is odd).

## Challenges (0/3 done)
- [ ] findOdd([20,1,-1,2,-2,3,3,5,5,1,2,4,20,4,-1,-2,5]) should return 5
- [ ] findOdd([1,1,1,1,1,1,10,1,1,1,1]) should return 10
- [ ] findOdd([5,4,3,2,1,5,4,3,2,10,10]) should return 1

```function findOdd(arr) {
    //happy coding!
    arr = arr.sort((a, b) => a-b);
    let obj = createObj(arr);
    //console.log(obj);

   for(let key in obj) {
   	if(obj[key]%2 !== 0) {
    	return parseInt(key);
    }
   }
    return 0;
}

function createObj(ar) {
    let obj = {};

    for(let i=0; i<ar.length; i++) {
        let ele = ar[i];
        //console.log(ele)
        if(obj.hasOwnProperty(ele)) {
            obj[ele] = obj[ele]+1;
        } else {
            obj[ele] = 1; 
        }
    }

    return obj;
}

```
