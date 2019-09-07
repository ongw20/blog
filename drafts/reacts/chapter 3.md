# React - TypeScript Project

## Creating `package.json`
The `package.json` file defines our project name, description, build commands, dependent npm modules, and much more.  
Run the following command in a terminal window under the project root folder:
```
npm init -y
```

## Adding TypeScript
```
npm install typescript --save-dev
```
Creating `tsconfig.json`
```
npx tsc --init
```

## Adding TSLint
```
npm install tslint --save-dev
```
Add a basic `tslint.json` file at the root of our project, and enter the following:
```json
{
  "extends": ["tslint:recommended", "tslint-react", "tslint-config-prettier"],
  "linterOptions": {
    "exclude": ["node_modules/**/*.ts"]
  }
}
```

## Adding React with types
```
npm install react react-dom --save
npm install @types/react @types/react-dom
```

## Adding webpack
```
npm install webpack webpack-cli webpack-dev-server --save-dev
npm install ts-loader --save-dev
```
Create a file called `webpack.config.js` in the project root, and enter the following into it:
```js
const path = require('path')
module.exports = {
  entry: './src/index.tsx',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  },
  module: {
    rules: [
      {
        test: /\.tsx?$/,
        use: 'ts-loader',
        exclude: /node_modules/
      }
    ]
  },
  resolve: {
    extensions: ['.tsx', '.ts', '.js']
  },
  devServer: {
    contentBase: path.join(__dirname, 'dist'),
    compress: true,
    port: 9000
  }
}
```

## Project folders and files
```
|-- dist/
   |-- bundle.js
   |-- index.html
|-- node_modules/
|-- src/
   |-- index.tsx
|-- package.json
|-- tsconfig.json
|-- tslint.json
|-- webpack.config.js
```

## Creating start and build scripts
Open up `package.json`, find the `scripts` section, add `start` and `build`:
```json
{
  ...
  "scripts": {
    ...
    "start": "webpack-dev-server --env development",
    "build": "webpack --env production"
  },
  ...
}
```

## Run our project
In `index.tsx`, add the content:
```tsx
const App: React.SFC = () => {
  return <h1>My React and TypeScript App!</h1>
}
```
Enter the following command in the terminal:
```
npm start
```
If we browse to `http://localhost:9000/` we'll see our web app.
