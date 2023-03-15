# Ask the Bob

## Instructions

- Bob is a lackadaisical teenager. In conversation, his responses are very limited.
- Bob answers 'Sure.' if you ask him a question, such as "How are you?".
- He answers 'Whoa, chill out!' if you YELL AT HIM (in all capitals).
- He answers 'Calm down, I know what I'm doing!' if you yell a question at him.
- He says 'Fine. Be that way!' if you address him without actually saying anything.
- He answers 'Whatever.' to anything else.
- Bob's conversational partner is a purist when it comes to written communication and always follows normal rules regarding sentence punctuation in English.

## Challenges (0/2 done)
- [ ] Any random string will be passed, it should work as asked
- [ ] Any random string will be passed, it should work as asked

```
const isUpper = (string) => {
    return !/[a-z]/.test(string) && /[A-Z]/.test(string)
}

function hey(message) {
	// Code here
    let pureLetterString = ""
    message.split("").forEach(character => {
        if(/[a-zA-Z]/.test(character)){
            pureLetterString += character
        }
    })

    console.log(pureLetterString);

    if(isUpper(pureLetterString) && message.trim().charAt(message.length-1) === '?'){
        return "Calm down, I know what I'm doing!"
    }
    else if(isUpper(pureLetterString)){
        return "Whoa, chill out!"
    }
    else if(message.trim().charAt(message.length-1) === '?'){
        return "Sure."
    }
    else if(message === ""){
        return "Fine. Be that way!"
    }

	return "Whatever."
}

function hey1(message) {

    let pureLetterString = ""
    message.split("").forEach(character => {
        if(/[a-zA-Z]/.test(character)){
            pureLetterString += character
        }
    })
    console.log(pureLetterString);
	if(pureLetterString == pureLetterString.toUpperCase() && message.slice(-1) === '?') return "Calm down, I know what I'm doing!";
    else if(pureLetterString == pureLetterString.toUpperCase()) return 'Whoa, chill out!'; 
    else if(message.slice(-1) == '?') return "Sure";
    else if(message === "") return 'Fine. Be that way!'; 
	return 'Whatever.' 
}


console.log(hey('HASDFASDF ASDF23423 ASDF ?'));
```

```
