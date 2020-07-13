# F# notes

Notes while learning f# that might be of interest in the future

### Triple double-quoted strings

String literals can be written using triple double-qoutes, e.g. `"""Hello"""`, which allows to include double quotes without escaping them. However, it does not allow to include a pair of double quotes. That is, `""""Hello""""` will produce `"Hello"`, but `""""""""` will produce an error instead or `""`.
