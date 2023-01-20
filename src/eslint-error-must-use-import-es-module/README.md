# How to fix ESlint Error: Must use import to load ES Module


In `package.json`. inside `devDependecies`, Add this line
```json
  "@babel/eslint-parser": "^7.5.4",
```
Then, in `.eslintrc.js` file, Add this line
```json
  parser: '@babel/eslint-parser',
```
