# Function which returns a random number in the given range
# Create a function which returns a random number in the given range of values both inclusive


<h2>Test Cases</h2>


  - [X] randomNumberGeneratorInRange(10, 50) should return a number between 10-50 (inclusive)
  - [X] randomNumberGeneratorInRange(100, 200) should return a number between 100-200 (inclusive)

```
function randomNumberGeneratorInRange(rangeStart, rangeEnd) {
	// write your solution here

	return Math.floor(Math.random() * (rangeEnd - rangeStart + 1)) + rangeStart;
}

console.log(`My random number: ${randomNumberGeneratorInRange(555, 100)}`)

```

 - <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random">Link</a>
  - <a href="https://stackoverflow.com/questions/1527803/generating-random-whole-numbers-in-javascript-in-a-specific-range">Link</a>
