# preval-use-strict-bug
Reproduction repository for [issue #47 in kentcdodds/babel-plugin-preval](https://github.com/kentcdodds/babel-plugin-preval/issues/47)

## Problem

"preval file comment" method has no effect on modules that use Strict Mode

For example, modules like the following will not be "prevaled", and there will be no error or warning:

```js
// @preval
'use strict';
// ...
```

## Reproduction

The files in the `dist` folder (committed for demonstration purposes) were generated from the `src` folder by running `npm run build`.

There are 3 examples, for 3 different preval usage methods. The only one that shows the problem is the `preval-file-comment` example.
