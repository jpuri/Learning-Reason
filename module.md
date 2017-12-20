# Module

Modules are like mini files. They can contain type definitions, let bindings and other modules.

- To create module use `module` keyword, name must start with capital letter and definition enclosed in `{}`.

```
module School = {
  type profession = Teacher | Director;

  let person1 = Teacher;
  let getProfession = (person) =>
    switch person {
      | Teacher => "A Teacher"
      | Director => "A Director"
    };
}
```

- Module's content can be accessed using `.` notation.

## Opening a module
Local opening of module

```
let message = 
  School.(
    switch person1 {
      | Teacher => "Hello teacher!"
      | Director => "Hello director!"
    }
  );
```

- `include` can be used to statically spread the content of one module in another.
- Every `.re` file is a module.
