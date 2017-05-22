# create-standalone

```sh
npm init

touch index.js
touch index.html

mkdir dist

npm install -g browserify
npm install -g watchify
npm install -g uglify-js

npm install --save-dev browserify watchify uglify-js

```

```
"scripts": {
  "build-debug": "browserify index.js -d --s pizza > dist/pizza.js",
  "build-min": "browserify index.js --s pizza | uglifyjs -c > dist/pizza.min.js",
  "build": "npm run build-debug && npm run build-min",
  "watch": "watchify index.js -d --s pizza -o dist/pizza.js -v"
},
```

```
npm run build
npm run watch
```