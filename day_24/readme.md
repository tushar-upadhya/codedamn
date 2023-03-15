# Write Number in Expanded Form

## Instruction
- You will be given a number and you will need to return it as a string in Expanded Form.
- For example:
- expandedForm(12); // Should return '10+2'
- expandedForm(42); // Should return '40+2'

## Challenges (0/3 done)
- [ ] expandedForm(12) should return '10+2'
- [ ] expandedForm(42) should return '40+2'
- [ ] expandedForm(734) should return '700+30+4'

```function expandedForm(num) {
	// Your code here
	num = num.toString();
    let temp = []
    let multiplier = 1;
    for(let i=1;i<=num.length;i++){
        const digit = num[num.length - i]
        digit > 0 && temp.unshift(digit*multiplier)
        multiplier *= 10 
    }
    return temp.join('+')
  }

  console.log(expandedForm(734));
  
```
