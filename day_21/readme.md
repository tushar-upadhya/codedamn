# Union of Two Arrays

## Instruction
- Write the code for the function which returns the the union of the two given arrays

## Challenges (0/2 done)
- [ ] unionOfArrays(['a','b','c'],['a',1,2,'d']) should return ['a','b','c',1,2,'d']
- [ ] unionOfArrays(['array','object'],['value','object','key']) should return ['array','object', 'value', 'key']
- [ ] unionOfArrays([1, 2, 34, 45, 3], [3, 24, 21]) == [1,2,34,45,3,24,21]) should return [1,2,34,45,3,24,21]

```const unionOfArrays = (arr1, arr2) => {
	// code below here
	let union = [...new Set([...arr1,...arr2])]
	return union;
  };
  
  console.log(`The union is ${unionOfArrays([1, 2, 34, 45, 3], [3, 24, 21])}`);\
```
