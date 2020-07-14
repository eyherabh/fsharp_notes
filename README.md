# F# notes

Notes while learning f# that might be of interest in the future

### Triple double-quoted strings

String literals can be written using triple double-qoutes, e.g. `"""Hello"""`, which allows to include double quotes without escaping them. However, it does not allow to include a pair of double quotes. That is, `""""Hello""""` will produce `"Hello"`, but `""""""""` will produce an error instead or `""`.

### Functions cannot end with `let`
The following causes an error because `let` cannot be the last element of a block
```
let addx x =
    let addy y = x + y
```
For returning `addy`, it must be added explicitly as the last line, namely
```
let addx x =
    let addy y = x + y
    addy
```
The additional line and identifier may not be desirable for small functions, let alone when many exist, because it reduces the amount of information presented in the same screen ([Linux kernel coding style](https://www.kernel.org/doc/html/v4.10/process/coding-style.html), section 6). To avoid them, a lambda can be used, namely
```
let addx x =
    fun y -> x + y
```

