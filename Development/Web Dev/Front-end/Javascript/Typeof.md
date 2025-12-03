`typeof` is a **unary operator** that checks a value and tells you its type (the return value is string type).

```js
var a; 
typeof a; // "undefined"
 
a = "hello world"; 
typeof a; // "string" 

a = 42; 
typeof a; // "number" 

a = true; 
typeof a; // "boolean" 

a = null; 
typeof a; // "object" -- weird, bug 

a = undefined; 
typeof a; // "undefined" 

a = { b: "c" }; 
typeof a; // "object"
```
