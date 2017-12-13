# Tuples

Tuples are:
1. immutable
2. ordered
3. fix-sized
4. heterogenous

```
let tup1 = (1, "test");
let 3dCoords = (1, 2, 3);
```

- There is no tuple of size 1.
- fst, snd can be used to access first and second member of the tuple.
- Tuple members are generally accessed by destructuring.

```
let (_, y, _) = 3dCoords;
```

- `_` is used to ignore member at that position.
- Tupes are not modified, destructuring is used to create new tuples from old ones.
- Tupes should be used for local access, for long living values prefer record.

Uses:
- Pass around multiple values.
- Pattern matching, `tuple + switch` combinatin is very powerful:

```
switch(condition1, condition2) {
| (true, true) => ...
| (true, false) => ...
| (false, true) => ...
| (false, false) => ...
}
```

- Reason types are types "structurally". Unlike lists they are heterogenous and more performant.