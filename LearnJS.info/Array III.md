## Array to string - HTML trick
Here's a neat trick: Let's say you have an array of [label, value], and you'd like to get the <font color="#f79646">value</font> of each <font color="#f79646">label</font> separated by a comma. Like a CSV (Comma Separated Values) export. How would you do that?

You already know the 2 methods that you need for such operations:  
First, you start with a `.map()` call to extract the `name` from the `users` array , and then you use **.join()** to join the array elements into one string.


Applying it to HTML
```javascript
const users = [{       //users is an array of objects, each object
    id: 1,             //has a property of name.
    name: "Sam Doe"
}, {
    id: 2,
    name: "Alex Blue"
}];

const userNamesArray = users.map(user => user.name)//gets names
console.log(userNamesArray); // ["Sam Doe", "Alex Blue"];

	const csv = userNamesArray.join(", ");//makes string with names
console.log(csv); // "Sam Doe, Alex Blue"
```
```
```

You can also chain these 2 commands and write it on one line:


```javascript
const csv = users.map(user => user.name).join(", ");
console.log(csv); // "Sam Doe, Alex Blue"
```

### Applying it to HTML

The above trick is often used to generate an HTML string from an array. Let's say we'd like to return an unordered list (a `tr` with `td` items) from the `rows` array. Instead of writing it with `.forEach`, you can use the above trick as follows:

```javascript
const html = `<ul>
    ${users.map(user => `<li>${user.name}</li>`).join("")}
    </ul>`;
console.log(html); // <ul> <li>Sam Doe</li><li>Alex Blue</li> </ul>
```

Notice how for every `user`, we return an `<li>...</li>` with the user's name inside.  
What's very important here is the `.join("")`. If you forget this, you will get the following HTML:
> This means that .join("") is what makes it a string without seperating via commas.

```html
<ul><li>Sam Doe</li>,<li>Alex Blue</li></ul>
```

That's because the array returned from `.map()` will automatically be converted to a string by the browser. It will automatically call the `.toString()` method which will insert a comma after every array item.  
Instead, you want to convert the array into a string yourself. You can do that by calling `.join("")` with an empty string as glue.

Finally, you have to wrap the whole string with the opening `<ul>` and the closing `</ul>`.