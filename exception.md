# Exception

- Exceptions are just special kind of "variant" thrown in exceptional cases.
```
let getItem = (theList) =>
  if(...) {
    /** code changes */
  } else {
    raise(Not_Found);    
  };
let result =
  try getItem([1,2,3]) {
  | Not_Found => 0 /** default if exception is thrown */
  }
```

- Custom exception can also be made:
```
exception InputClosed(string);

raise(InputClosed("The stream has closed!"));
```
