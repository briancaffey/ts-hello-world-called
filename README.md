## Purpose

The purpose of this repo is to demonstrate how to write a node module that can be **called** used by another node project without publishing that project to NPM, but instead just using the GitHub reference.

This project is called `ts-hello-world-called` because it will be called by another repo called `ts-hello-world-caller` which will have a reference to `ts-hello-world-called` in `package.json`.

To get started, follow these steps:

### npm init

```
npm init
```

I have selected all of the default options for this project

### install typescript

```
npm install typescript --save-dev
```

### .gitignore

Create a `.gitignore` file with the following:

```
node_modules
```

### `tsconfig.json`

Create the following file that will control the options of the TypeScript compiler:

```json
{
    "compilerOptions": {
        "strict": true,
        "outDir": "dist",
        "target": "ES2020",
        "module": "NodeNext",
        "moduleResolution": "NodeNext",
        "sourceMap": true,
        "experimentalDecorators": true,
        "pretty": true,
        "noFallthroughCasesInSwitch": true,
        "noImplicitReturns": true,
        "forceConsistentCasingInFileNames": true
    },
    "include": ["src/**/*"]
}
```

### index.ts

Create a directory `src` and inside of it create an `index.ts` file:

```ts
const message = "Hello, World!";

export default message;
```
