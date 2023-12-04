### Object concatenation and implicit coercions

When we call the + operator with objects and try to concatenate or perform addtion, the result will be "[object Object]".

To handle these scenarios we need to refactor the object by adding two methods
1. toString method
2. valueOf method

**Example**
```
const obj = {
    toString: function() {
        return "any string";
    },
};

console.log("concatenate " + obj);  // the toString method will be called
```

> output: concatenate any string  

**Example**
```
const obj = {
    toString: function() {
        return "any string";
    },
    valueOf: function() {
        return "any value";
    }
};

console.log("add " + obj);  // the valueOf method will be called
```

> output: add any value


*Note:* The moral of this story is that valueOf was really only designed to be used for objects that represent numeric values such as Number objects.


**Things to Remember**

- Type errors can be silently hidden by implicit coercions.
- The + operator is overloaded to do addition or string concatenation depending on its argument types.
- Objects are coerced to numbers via valueOf and to strings via toString.
- Objects with valueOf methods should implement a toString method that provides a string representation of the number produced by valueOf.
- Use typeof or comparison to undefined rather than truthiness to test for undefined values.