# Record

Records are like objects, features:
1. Immutable
2. Typed
3. Fast
4. Light
5. Fixed in field names and types.

## Using record

- declaring record type, this is mandatory

```
type person {
  name: string,
  age: int
};
```

- value is inferred to be of a type

```
let somePerson = {
  name: "john",
  age: 20
};
```

- access is done using dot notation

```
somePerson.name;
```

- If the type reside in other file it should be explicitly mentioned

```
let me: OtherFile.person = {name: "jyoti", age: 33};
```

- New records can be created from old records using spread notation `...`

```
let someOtherrecord = {...me, age: me.age + 1};
```

- Puning can be used a shorthand where name of the field matches its value. Puning does not works for single record.

```
let age = 20;
const somePerson = {name: "John", age};
```

- Record types are found by field name and cause unexpected results.
- Mandatory type declaration makes error detection and refactoring easy.