a basic typescript setup

### what you need
- NVM (Node Version Manager)

### what I did
1. `npm init` and followed prompts
2. `nvm current > .nvmrc` to set up the `.nvmrc` file with my version of Node.
   1. so future people that clone the project can `nvm use` and `nvm install` to use the same version of Node
3. `npm install --save-dev typescript @types/node @tsconfig/node18-strictest-esm` to install a premade tsconfig to use
   1. https://github.com/tsconfig/bases
4. Made a `tsconfig.json` file, added the following

```json
{
	"extends": "@tsconfig/node18-strictest-esm/tsconfig.json",
	"compilerOptions": {
		"outDir": "dist"
	},
	"include": [ "src/**/*.ts" ],
	"exclude": [ "node_modules" ]
}
```

5. Created a `src` folder and a file `index.ts`.
6. `tsc` to build the project (`npm run build`).
7. `npm run dist/index.js` to run it (`npm run start`)


### to use this
`nvm install` and `nvm use`

`npm run build` to build the code

`npm run start` to run it