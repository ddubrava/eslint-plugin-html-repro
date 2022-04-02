### Expected

`npm run lint` should emit these:

```shell
0:1  error  Missing `<!DOCTYPE HTML>`               @html-eslint/require-doctype
1:2  error  Missing `alt` attribute at `<img>` tag  @html-eslint/require-img-alt
```

### Actual

`npm run lint` emits nothing. If we remove `'html'` from `plugins` in `.eslintrc`,
eslint will emit these errors.

I suppose that `eslint-plugin-html` breaks something in the linter,
so we can't set any rules or plugins.