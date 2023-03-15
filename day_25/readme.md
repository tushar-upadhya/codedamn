# Stop gninnipS My sdroW!

## Instruction
- Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed (Just like the name of this Kata). Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.

- Examples: spinWords( "Hey fellow warriors" ) => returns "Hey wollef sroirraw" spinWords( "This is a test") => returns "This is a test" spinWords( "This is another test" )=> returns "This is rehtona test"

## Challenges (0/3 done)
- [ ] spinWords("Hey fellow warriors") should return"Hey wollef sroirraw"
- [ ] spinWords("You are almost to the last test") should return "You are tsomla to the last test"
- [ ] expandedForm(734) should return '700+30+4'

```function spinWords(str) {
    //TODO Have fun :)
    let strSplit = str.split(" ");

    for(let i = 0; i < strSplit.length; i++) {
        if(strSplit[i].length >= 5) {
            let rev = reverseString(strSplit[i]);
            strSplit[i] = rev;
        }
    }

    return strSplit.join(" ");

}

function reverseString(str) {
    return str.split('').reverse().join('');
}

```
