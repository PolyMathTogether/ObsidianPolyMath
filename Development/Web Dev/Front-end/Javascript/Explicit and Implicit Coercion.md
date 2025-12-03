>"**Implicitly**" means that the JS engine does it. "**Explicitly**" means that you must do it.

Here is **explicit coercion** example:
```js
var a = "42";
var b = Number( a );

a; // "42"
b; // 42 -- number!
```

And here is **implicit coercion**:
```js
var a = "42"; var b = a * 1; 
a; // "42" 
b; // 42 -- number!
```
