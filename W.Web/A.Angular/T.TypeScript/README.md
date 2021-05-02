# TypeScript

## :one: Install TypeScript via `npm`

```
$ npm install typescript --global
```

* Test TypeScript

```
$ tsc --version
Version 3.7.4
```

## :two: REPL

```
$ npm install ts-node --global
```

* Test TS-NODE

```
$ ts-node --version
v8.5.4
```

* Run the REPL using [npx: an npm package runner](https://blog.npmjs.org/post/162869356040/introducing-npx-an-npm-package-runner)

```
% npx ts-node 
>
```

* Type some sample code

```typescript
> function f(x: number) { return x + 1 }
undefined
> f(0)
1
```


* Exit from the REPL

```
> .exit
```



# References

| Link                                 | Description          |
|--------------------------------------|----------------------|
| https://www.typescriptlang.org/      |  Doc                 | 
| https://www.typescriptlang.org/play  | Playground           |
| https://fireship.io/lessons/ts-decorators-by-example/ | TS Decorators |
