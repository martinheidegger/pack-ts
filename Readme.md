# @martinheidegger/pack-ts

Package script for typescript libraries. Prepares a `./dist` folder with reduced `package.json` that can then be published


```bash
npx @martinheidegger/pack-ts
```

## Warning: very opinionated built tool

This tool:

- runs `npm run build-ts` to build the typescript code
- removes unnecessary parts from the package.json like `private` or `devDependencies` in the dist folder.
- removes compiled versions of `__tests__`
- makes `./dist` a root which makes deep require statements easier
- adds `./src` to the `./dist` folder _(without the `__tests__`!)_ 
- subsequentally fixes all the sourcemap entries to to point to the right sources.
- copies a `Readme.md` and `LICENSE` file into the distribution

## License

[MIT](./LICENSE)
