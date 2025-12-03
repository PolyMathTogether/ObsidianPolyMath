`==`, `!=` compares between only the values but `===`, `!==` compares both the values and their types

```js
var a = "42";
var b = 42;
a == b; // true
a === b; // false 
```

In the `a == b` statement, JS realizes that their types are not the same, so it performs **[[Explicit and Implicit Coercion|implicit type coercion]]** until both values have the same type.