# LOOPING A TRIANGLE

Write a loop that makes seven calls to console.log to output the following triangle:

<pre>#
##
###
####
#####
######
#######</pre>

It may be useful to know that you can find the length of a string by writing `.length` after it.

```javascript
var abc = "abc";
console.log(abc.length);
// → 3
```

## Steps to solve the challenge

1. Declare a variable to be the string that you print in each iteration

2. Write a loop that has seven iterations:
	2.1. Inside each iteration update your variable as you think is convinient.
	2.2. Print the updated variable.

## Implementation

```javascript
var outPut = "";

for (var i = 0; i < 7; i++) {
	outPut += "#"
	console.log(outPut);
}
```

## Extra

Modify your program output the following triangle:

<pre>
      #
     ##
    ###
   ####
  #####
 ######
#######</pre>

# FIZZBUZZ

Write a program that uses `console.log` to print all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, print `"Fizz"` instead of the number, and for numbers divisible by 5 (and not 3), print `"Buzz"` instead.

(This is actually an interview question that has been claimed to weed out a significant percentage of programmer candidates. So if you solved it, you’re now allowed to feel good about yourself.)

## Steps to solve the challenge

1. Write a loop that starts from 1 and go up to 100 included.

2. At each iteration check for the two exceptions

	2.1. If the iteration number is divisible by 3 print `"Fizz"`
	2.2. If the iteration number is divisible by 5 (and not 3) print `"Buzz"`
	2.3. Otherwise print the iteration number.

## Implementation

```javascript
for (var i = 1; i <= 100; i++) {
	if (i % 3 === 0) {
		console.log("Fizz");
	}
	else if (i % 5 === 0) {
		console.log("Bazz")
	}
	else {
		console.log(i)
	}
}
```

Modify your program to print `"FizzBuzz"`, for numbers that are divisible by both 3 and 5 (and still print `"Fizz"` or `"Buzz"` for numbers divisible by only one of those).

## Steps to solve the change

1. Write a loop that starts from 1 and go up to 100 included.

2. At each iteration check for the two exceptions
	2.1. If the iteration number is divisible by both 2 and 3 print `FizzBuzz`
	2.2. If the iteration number is divisible by 3 print `"Fizz"`
	2.3. If the iteration number is divisible by 5 (and not 3) print `"Buzz"`
	2.4. Otherwise print the iteration number.

## Implementation

```javascript
var isDivisibleBy3 = false;
var isDivisibleBy5 = false;

for (var i = 1; i <= 100; i++) {
	isDivisibleBy3 = (i % 3) === 0;
	isDivisibleBy5 = (i % 5) === 0
	if (isDivisibleBy3 && isDivisibleBy5) {
		console.log("FizzBuzz");
	}
	else if (isDivisibleBy3) {
		console.log("Fizz");
	}
	else if (isDivisibleBy5) {
		console.log("Buzz");
	}
	else {
		console.log(i)
	}
}
```

# Chess board

Write a program that creates a string that represents an `8×8 grid`, using newline characters to separate lines. At each position of the grid there is either a space or a `“#”` character. The characters should form a chess board.

## Steps to solve the change

// To do

## Implementation

```javascript
var lineType1 = " # # # #";
var lineType2 = "# # # # ";

for (var i = 1; i <= 8; i++) {
	if (i % 2 == 0) {
		console.log(lineType2)
	}
	else {
		console.log(lineType1)
	}
}
```

define a variable size = 8 and change the program so that it works for any size, outputting a grid of the given width and height.

## Steps to implement

// To do

## Implementation

```javascript
var size = 8;
var line;

for (var i = 1; i <= size; i++) {
	line = "";
	for (var j = 1; j <= size; j++) {
		if ( (i+j) % 2 == 0) {
			line += " ";
		}
		else {
			line += "#";
		}
	}
	console.log(line + "\n");
}
```