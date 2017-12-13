# Destructuring

Way of extracting fileds from data structures.

```
let someInts = (10, 20);
let (ten, twenty) = someInts;

type person = {name: string, age: int};
let someguy = {name: "john", age: 30};
let {name, age} = someguy;

let {name: n, age: a} = someguy;

someFunction(~person as {name}) {
  /* use name here */
}
someOtherFunction(~person as {name} as firstPerson) {
  /* use name, firstPerson here */
}
```

- Never abuse destructuring to make code overly nested.
- If definition of record is not in current file it would require to be annotated.
