# Lists

Lists are :
  - immutable
  - homogenous
  - fast at pre-pending items
  - internally they are single linked list

```
let myList = [1, 2, 3];
```

## Usage:
  - Lists should be used for its resizeability, fast prepend, fast split (all of which are immutable).

### Immutable Prepend

```
let anotherList = [0, ...myList];
```

- myList here does not mutate. This is efficient, constant time.
- Adding item in middle of list is discouraged due of performance overhead.
- `switch` can also be used to access list item:

```
let message =
  switch mylist {
    | [] => "This is empty"
    | [a, ...rest] => "Head of this list is" ++ a
  }
```

- to access arbitrary list item `List.nth`.

# Array

Array are:
  - mutable
  - fast at random access and update
  - fixed sized on native (flexible size on JavaScript, they map exactly to javascript array).

```
let myArray = [|"Hello", "world", "how are you!"|];
let firstItem = myArray[0];
myArray[0] = "array";
```
