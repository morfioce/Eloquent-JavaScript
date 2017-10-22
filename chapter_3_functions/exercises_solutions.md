# Minimum

The previous chapter introduced the standard function `Math.min` that returns its smallest argument. We can do that ourselves now. Write a function `min` that takes two arguments and returns their minimum.

```javascript
console.log(min(0, 10));
// → 0
console.log(min(0, -10));
// → -10
```

## Implementation

```javascript
function min(a, b) {
	if (a < b) {
		return a;
	}
	else {
		return b;
	}
}
```

<strong>More compact version</strong>

```javascript
function min(a, b) {
	return a < b ? a : b;
}
```

# Recursion

We’ve seen that `%` (the remainder operator) can be used to test whether a number is even or odd by using `% 2` to check whether it’s divisible by two. Here’s another way to define whether a positive whole number is even or odd:

* Zero is even.

* One is odd.

* For any other number N, it's eveness is the same as N-2.

Define a recursive function `isEven` corresponding to this description. The function should accept a number parameter and return a Boolean.

Test it on 50 and 75. See how it behaves on -1. Why? Can you think of a way to fix this?

```javascript
console.log(isEven(50));
// → true
console.log(isEven(75));
// → false
console.log(isEven(-1));
// → ??
```

## Steps to solve the challenge

1. What are the base cases here ?

2. How can I reduce the problem to a smaller one (until I reach the base case)?

## Implementation

```javascript
function isEven(num) {
	if (num === 0) {
		return true;
	}
	else if (num === 1) {
		return false;
	}
	else {
		return isEven(num - 2);
	}
}
```

How to solve the problem for negative numbers ?

# Bean counting

You can get the Nth character, or letter, from a string by writing `"string".charAt(N)`, similar to how you get its length with `"s".length`. The returned value will be a string containing only one character (for example, "b"). The first character has position zero, which causes the last one to be found at position `string.length - 1`. In other words, a two-character string has length 2, and its characters have positions 0 and 1.

Write a function `countBs` that takes a string as its only argument and returns a number that indicates how many uppercase `“B”` characters are in the string.

## Steps to solve the challenge

// To do

## Implementation

```function
function countBs(str) {
	var counter = 0;
	for (var i = 0; i < str.length; i++) {
		if (str[i] === "B") {
			counter += 1;
		}
	}

	return counter;
}
```

Next, write a function called countChar that behaves like countBs, except it takes a second argument that indicates the character that is to be counted (rather than counting only uppercase `“B”` characters). Rewrite countBs to make use of this new function.

## Steps to solve the challenge

// To do

## Implementation

```javascript
function countChar(str, char) {
	var counter = 0;
	for (var i = 0; i < str.length; i++) {
		if (str[i] === char) {
			counter += 1;
		}
	}

	return counter;
}

function countBs(str) {
	return countChar(str, "B");
}
```