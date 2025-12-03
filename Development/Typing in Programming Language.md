# Weak/Strong Typing
---

> Strong typing means that the type of a value doesn’t **suddenly** change.


Example of **weak typing** language:
- **PHP**:
```php
$a = "3" + "5"; // $a === 8
$b = 101 . " dogs"; // $b === "101 dogs"
```
- **Javascript**:
```js
let a = "abc" + 123; // 123 is implicitly converted to string "123"
console.log(a); // "abc123"
```

Basically if a type of object is converted **implicitly** to another type then that language is **weak typing**

# Static/Dynamic Typing
---
In **static typing** language, each variable has its own specific type linked to it. So when you declare a variable, you have to specific its type before using it. The type of variable is checked in **compile-time**

Example in **C**:
```C
int a;  // the type of a is integer
a = 3;  // OK, assign 3 to a
a = "Hello"; // Error, cannot assign string value to int
```

Conversely in **dynamic typing**, each variable is simply one label linked to one object. Each object has its own type (e.g., in Python, we have the type `int`, `str`, ...) but the variable itself does not.The type of variable is checked in **runtime**

**Dynamic typing** in **Python**:
```python
b = 3   # variable b is bound to integer object
isinstance(b, int)  # True

b = 'hello world!'   # Now b is bound to string object
isinstance(b, str)   # True

b = ['blue', 'black', 'brown'] # Now b is a list

```

