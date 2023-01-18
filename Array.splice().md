The ==splice()== method changes the content of an array by removing or replacing exisiting elements and/or adding new elements in place.

to access part of an array without modifying it, try <u>slice()</u>

## Syntax
	splice(start)//zero-based index at which ot start changing the array (if negative index, counts back from the end of the array.)
	splice(start, deleteCount)//(optional) an integer indicating the number of elements in the array to remove from *start*. If 0 or negative, no elements are removed.
	splice(start, deleteCount, item 1)//(optional)the elements to add to the array, beginning from *start*. If you do not specify any elements, splice() will only remove elements from the array.
splice(start, deleteCount, item1, item 2, itemN)

## In practice

```
const phoneNum = [3, 2, 3, 4, 7, 6, 2, 1, 8, 1];
phoneNum.splice(1, 0 , 'hi')
//inserting at index 1, removing 0 elements, inserting 'hi'

console.log(phoneNum); 
//expected output: Array [3, 'hi', 2, 3, 4, 7, 6, 2, 1, 8 ,1]

-------------------------------------------------------------
cont int = [3, 2, 3]

int.splice(1, 1, 'error')
//insert at index 1, delete 1 element, insert 'error'

console.log(int);
//expected output : array [ 3, 'error', 3]

```
