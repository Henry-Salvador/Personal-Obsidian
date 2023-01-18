## Spread Syntax (...)
(...) syntax alows for an iterable, such as an array or string, to be expanded into places where zero or more arguements (for function calls) or elements (for array literals) are expected.

In an object literal, the spread syntax enumerates the properties of an object and adds the key-values to the object being created.

(Spread syntax looks like Rest syntax but does the opposite.)


```
function sum( x ,y , z) {
return x + y + z;
}

const numbers[1, 2, 3];

console.log(sum(...numbers)); //we call the function sum, and in place of the function arguement, we expand the elements of the array 'Numbers'.

```
