# React Native Error: decorators-legacy

Experimental syntax 'decorators-legacy' isn't currently enabled

1.Install decorator in package.json

```bash
  install decorator in package.json
	 "@babel/plugin-proposal-decorators": "^7.3.0",
    	 "@babel/preset-flow": "^7.0.0"
```

2.update babe.config.js with this

```bash
module.exports = {
  "presets": [
    "module:metro-react-native-babel-preset",
    "@babel/preset-flow"
  ],
  "plugins": [
    ["@babel/plugin-proposal-decorators", { "legacy" : true }],
    ["@babel/plugin-proposal-class-properties", { "loose" : true }],
  ]
}
```
