# Type

- Types can accpet parameter and create new type. Parameter of type should start with a '.

```
type intCoordinates = (int, int, int);
type floatCoordinates = (float, float, float);

or

type coordinates('a) = ('a, 'a, 'a);
type intCoordinateAlias = coordnates(int);

let buddy: coordinates(float) = (10.50, 10.50, 10.50);
```

- In practice types are inferred:

```
let buddy = (10, 20, 30);

is inferred as type coordinates(int)
```

- Types can be composable.

```
type result('a, 'b) =
  | Ok('a)
  | Error('b);
```
