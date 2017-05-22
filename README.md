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
  "build-debug": "browserify index.js -d --s name > dist/pizza.js",
  "build-min": "browserify index.js --s name | uglifyjs -c > dist/name.min.js",
  "build": "npm run build-debug && npm run build-min",
  "watch": "watchify index.js -d --s name -o dist/name.js -v"
},
```

```
npm run build
npm run watch
```