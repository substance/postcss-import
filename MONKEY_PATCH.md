# postcss-import [Substance]

This is a fork of [postcss/postcss-import](https://github.com/postcss/postcss-import), which disables that files get
inlined which are specified using the `url()` expression.

In some cases we want to be able to link to externally managed
CSS files. We think, the most intuitive way is to take
`url()` expressions as explicit user intention.

With our patched plugin the following does not get inlined

```
@import url('my-shared-library.css');
```

as opposed to

```
@import 'my-shared-library.css';
```
