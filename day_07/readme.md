# Create a regular expression to validate if the given input is valid Indian mobile number or not
* Regular expression check has to have an optional +91 or 0 in the beginning, then an optional space and 10 digits
* test method of regular expression can be used to validate if the mobile number pattern matches or not


<h2>Challenges (0/3 done)</h2>


  - [X] validateMobile('+919876543210') returns true
  - [X] validateMobile('+91 9876543210') returns true
  - [X] validateMobile('09876543210') returns true
  - [X] validateMobile('9876543210') returns true
  - [X] validateMobile('99876543210') returns false

```
const number = '+919876543210';

function validateMobile(number) {
    let s=number+"";
    if(s.substring(0,3)==="+91"||s.charAt(0)==="0"||s.length==10)
        return true;
    else
        return false;
}

console.log(`is a valid Indian mobile number: ${validateMobile(number)}`)

```
