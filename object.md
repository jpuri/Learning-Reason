# Object

- Pure reason objects are not used much, most often records are useful.
- BuckleScript objects are used often for JS interoperatibility.
- Reason gives BS object value `[%bs.obj {foo: bar}]` a special syntax `{"foo": bar}` and to types `{. "foo": bar}`.