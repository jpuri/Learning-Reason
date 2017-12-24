# Pattern Matching

- Its one if the Best features of Reason.
- Here is Type/Switch with parameters:
```
type payload =
  | BadResult(int)
  | GoodResult(string)
  | Noresult;
```

- Using switch expression on it, it can be destructured:
```
let data = GoodResult("Product Shipped!");
let message =
  switch data {
    | GoodResult(theMessage) => "The result is" ++ theMessage
    | BadResult(errorCode) => "The error code is" ++ string_of_int(errorCode)
  };
```

- A couple of other switch scenario:
```
switch mylist {
  | [] => print_endline("Empty list")
  | [a, ...rest] => pront_endline("The first item in list is") ++ a
};

switch myarray {
  | [|1, 2|] => print_endline("Array with elements 1 and 2")
  | [||] => print_endline("Empty array")
  _ => print_endline("Its an array") /** special fall through case */
};
```

- `when` can be added to switch to add some clause:
```
let message =
  switch data {
    | GoodResult(theMessage) => "The result is" ++ theMessage
    | BadResult(errorCode) when isServerError(errorCode) => "It is server side error"
    | BadResult(errorCode) => "The error code is" ++ string_of_int(errorCode)
  };
```

- Match can be done even on exception:
```
switch(List.find(i => i.name === "John", items)) {
  | Item => print_endline("Item found !")
  | exception Not_Found => print_endline("Item not found !")
};
```

