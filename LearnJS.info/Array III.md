## Array to string - HTML trick
Here's a neat trick: Let's say you have an array of [label, value], and you'd like to get the <font color="#f79646">value</font> of each <font color="#f79646">label</font> separated by a comma. Like a CSV (Comma Separated Values) export. How would you do that?

You already know the 2 methods that you need for such operations:  
First, you start with a `.map()` call to extract the `name` from the `users` array , and then you use **.join()** to join the array elements into one string.