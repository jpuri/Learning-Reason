# JSX

- An example showing most of features.

```
<MyComponent
  booleanAttribute={true}
  stringAttribute="Hello"
  intAttribute=1
  forcedOptional={someHello("hello")}
  onClick={reduce(handleClick)}>
  <div>{ReasonReact.stringToElement("Hello")}</div>
</MyComponent>
```

- Puning can be used as shorthand when label and value are same.
