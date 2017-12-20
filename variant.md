# variant

- A varint allows us to express `this or that`.

```
type myResponseVariant = 
  | Yes
  | No
  | PrettyMuch;

let yesYouAreCrushingIt = Yes;
```

- `Yes`, `No` and `PrettyMuch` are caled constructors and always capatilized.
- They are separated by `|`.
- `switch` are very useful with `variant`. 

```
let message = 
  switch areYouCrushingIt {
    | No => "No worries. Keep going!"
    | Yes => "Great!"
    | PrettyMuch => "Nice!"
  }
```

- Variants have extremely rich type assitance. It will complain if you miss a type or specify a redundant one.
- If variant is in a different file, you need to brong it to scope.

```
/* zoo.re */
type anumal = Dog | Car | Bird;
```

```
/* example.re */
let pet: Zoo.animal = Dog;
/* or */
let pet = Zoo.dog;
```

## Constructor Arguments

- A variant constructor can contain extra data separated by commas.

```
type account =
  | None
  | Instagram(name)
  | Facebook(name, id);
```

- this data is called constructor arguments and can be used in pattern matching.
```
let greeting =
  switch myAccount {
    | None => "Hi!"
    | Instagram(name) => "Hi !" ++ name
    | Facebook(name, id) => "Hello !" ++ name ++ id
  };
```

- A useful variant exposed by standard library is `option`.

```
type option('a) = None | Some('a);
```
- `int` will always be int. But `option(int)` can be `None` or `Some('a)`.
- Switch with variant is very fast operation of linear order.