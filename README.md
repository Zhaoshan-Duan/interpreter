# Interpreter
Building A Tree-walking Interpreter. It tokenized and parse source code into a REPL, building up an internal representation of code (abstract syntax tree), then evaluate this tree.

Major Parts;
- lexer
- parser
- Abstract Synatx Tree
- internal object system
- evaluator

Guided by "Writing An Interpreter in Go" by Thorsten Ball

## Features

### Variable Bindings 
Using a keyword `let` to bind values, functions to name
```
let name = 1;
let add = fn(a, b) { return a + b; };
```

### Functions

Functions are first-class, and support higher order functions.

Explicit `return` 
```
fn(f, x) {
  return f + x;
}
```

Implicit `return` 
```
let add = fn(a ,b) { a + b; };
```

calling function
```
add(1, 2);
```

Higher order function
```
let twice = fn(f, x) {
  return f(f(x));
}
let addTwo = fn(x) {
  return x + 2;
}
twice(addTwo, 2);
```



### Arithmetic Expressions
```
let result = 10 * (20 / 2);
```
### Data Structures 

#### Array
```
let array = [1, 2, 3];

array[0] // -> 1
```

#### String
```
let name = "Go";
```
#### Hash Table
```
let map = {"key": "stringVal", "keyInt": 3};
```



