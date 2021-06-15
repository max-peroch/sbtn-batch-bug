> sbt compile

Works as expected, ie. it fails to load the project, ask for an input about what to do about it, but because of the `batch` mode exit right away.

> SBT_NATIVE_CLIENT=true sbt compile

Starts the thin client, fails to load the project and then get stuck into an infinite loop of:
```
[warn] Project loading failed: (r)etry, (q)uit, (l)ast, or (i)gnore? (default: r)
Invalid response: 'ÿ'
```
