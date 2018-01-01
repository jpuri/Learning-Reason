# String

- reason strings are delimited using double quotes.
```
let greeting = "Hello world!";
let multiplineGreetings = "Hello
  world!";
```

- Special characters in the strings need to be escaped `\\`.

- Strings can be added using `++`. Natively concatening many strings is performance overhead, for eg, `"ab" ++ "bc" ++ "cd"`. Instead of this `String.concat` ca be used.

# Char

- This is reason's type for a string with a single character. `'a'`.
- It does not supports UTF-8 or unicode.
