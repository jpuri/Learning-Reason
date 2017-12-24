# Let Bindings

- Let binds values to name.
- The values can be seen and used by code after them.
- Bindings canbe scopes throught `{}`.
- Bindings are immutable, they can not refer to anything else. But a binding by same name can shadow previous one:
```
let message = "Hello";
print_endline(message); /** hello here */
let message = "World";
print_endline(message); /** world here */
```

- anonymous scope can be created around bindings to prevet their misuse:
```
let test = {
  let t1 = 10;
  let t2 = 20;
  print_endline(t1 + t2);
}
```
