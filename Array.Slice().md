The slice() method returns a shallow copy of a portion of an array into a new array object selected from *start* to *end* (end not included) where start and end represent the index of items in that array. The original array will not be modified.

## Syntax
	slice() //if parameters are ommitted, will just copy the entire array
	slice(start)// //(optional) zero-based index at which to start extraction, converted to an integer.
	slice(start, end) //end:(optional): zero based index and which to end extraction, extracting up to but not including end. Negative index counts back form the end of the array.

## Try it

```
const phone = [3, 2, 3, 4, 7, 6, 2, 1, 8, 1]

console.log(phone.slice(2));
//expected output: array [3, 4, 7, 6, 2, 1, ,8, 1]

console.log(phone.slice(0,3))
//expected output: array [3,2,3]

console.log(phone.slice(3,-4))
//expected output: array [4, 7, 6]

console.log(phone.slice(-4)) //remember *start* includes index, while *end* does not.
//expected output : array [2, 1, 8, 1]
```
