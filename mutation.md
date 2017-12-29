# Mutation

- This feature should be used only sparingly.

- To create mutable `let` binding `ref` can beused like:
```
let foo = ref(5);
```

- Actual value of ref can be obtained using postfix operator:
```
let six = foo^ + 1;
```

- Assign new value to foo like:
```
foo := 7;
```

- A workaround for not using mutation is overriding let binding:
```
let foo = 10;
let foo = someCondition ? foo + 100 : foo;
print_int(foo);
```
