the join() method creates and returns a new string by concatenating all of the elements in an array ( or array-like object) seperated by commas, or a specified separator string. 

If the array has only one item then that item will be returned without using the separator.


```
const intsPhone= [ 1, 2, 3, 4, 5, 6, 7, 8 , 9 , 0];

console.log(intsPhone.join()); //by default ',' is the character inbetween joins

console.log(intsPhone.join(''))
//expected outputs: "1234567890"

console.log(intsPhone.join('-'));
//expected output: "1-2-3-4-5-6-7-8-9-0"

```

## Syntax

```
join()
join(seperator)

```
