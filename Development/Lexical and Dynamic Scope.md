Lexical and dynamic scopes are normally used in [[Garbage Collector]] to indentify that if a variable is never used or expired. 

# Lexical Scope
---
“Lexical” refers to the way code is written, so in **lexical scope**, the scope of a variable is determined by **where it is defined** in the source code.

```js
var dog = 'alive'

function foo() {
     var cat = 'alive'
     console.log(dog)  // 'alive'
}
console.log(cat)  // out of scope
```

# Dynamic Scope
---
In **dynamic scope**, the lifetime of a variable is determined by the call stack, which means it depends not on where the variable is written in the code, but on **how the program is executed**.

# Block Scope
---
```js
for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 0);
}
```

The result of the code above is:
```
3
3
3
```

This may seem wrong at first, but it happens because the variable `i` has **function scope**, so each iteration uses the **same** `i` variable. When the loop finishes, `i` has the value `3`, and all the `setTimeout` callbacks **reference** that same variable. To solve this problem, we use `let` instead of `var` to create **block scope**, which ensures that a different `i` is created for each iteration of the loop.

```js
for (let i = 0; i<3; i++) {
    setTimeout(() => console.log(i), 0)
}
```

The result:
```
0
1
2
```

>So basically, if you use `var`, it will reference only one `i` variable, and if you use `let`, it will reference a different `i` for each iteration.