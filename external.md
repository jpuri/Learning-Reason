# External

- `external` is how reason communicates with other languages like `c` and `javascript`.

```
external myCFunction : int => string = "theCFunction";
```

```
[@bs.val] external getELementByClassName: string => array(Dom.element) = "document.getElementByClassName";
```

- Externals can only be at top level or inside modules.
