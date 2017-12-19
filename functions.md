# Functions

Functions are declared with an arrow and a return expression.

```
let greet = (name) => "Hello " ++ name;
```

- In reason every function takes an argument, apparently no argument function are passed a unit `()`.
- Labels can be attached to function arguments:

```
let addCoordinates = (~x, ~y) => {
  /* function body */
};

addCoordinates(~x = 5, ~y = 6);
```

## Currying
- Reason functions can automatically be called partially.
```
var add = (a, b) => a + b;
var addFive = add(5);
var ten = addFive(5);
var eleven = addFive(6);
```

## Optional labeled arguments
- Labeled function arguments can be made optional during declaration.
```
lat drawCircle = (~color, ~radius=?, ()) => {
  colorCircle(color);
  switch radius {
    | NONE => startAt(1,1)
    | SOME(r_) => startAt(r_,r_)
  }
};
```

- Radius is wrapper in standard library's option type defaulting to `None` and is some value is provided its wrapped in type `Some`.
- Optional labeled arguments can be provided a default value.
```
let drawCircle = (~radius?=1, ~color, ()) => {
}
```

- `rec` keyword can be used to create recursive function:
```
let rec neverTerminate => neverTerminate();
```

