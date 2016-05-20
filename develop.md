## 初始化
npm -> v6.1
electron -> v1.1

```
mkdir electron-works
cd electron-works

npm init
eslint --init

mkdir app
mkdir fonts
mkdir styles
mkdir scripts
mkdir images

touch index.html
```

## 基础库
```
npm install electron-prebuilt --save-dev
npm install electron-packager --save-dev
npm install electron-debug --save-dev
```

## 目录结构
```
cd app

mkdir actions
mkdir components
mkdir containers
mkdir reducers
mkdir store
mkdir utils

touch index.js
touch index.html
touch global.css

cd ..
```

## 开发库
```
npm install font-awesome  --save
npm install electron-json-storage  --save
npm install electron-localshortcut  --save

npm install react react-dom react-router  --save
npm install redux react-redux redux-thunk  --save
npm install redux-actions redux-promise react-router-redux  --save

npm install bluebird lodash query-string  --save

npm install webpack babel-core babel-eslint babel-loader babel-register  --save-dev
npm install babel-plugin-add-module-exports babel-plugin-webpack-loaders  --save-dev
npm install babel-polyfill babel-preset-es2015 babel-preset-react babel-preset-react-hmre babel-preset-stage-0  --save-dev
npm install css-loader html-loader style-loader json-loader  --save-dev
npm install eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react  --save-dev
npm install webpack-dev-middleware webpack-hot-middleware redux-logger  --save-dev
npm install css-modules-require-hook electron-debug postcss source-map-support  --save    

sudo npm install redux-devtools redux-devtools-dock-monitor redux-devtools-log-monitor  --save-dev  
```

## 辅助库
```
npm install asar babel-register chai chromedriver co-mocha  --save-dev 
npm install concurrently cross-env del  --save-dev 
npm install express extract-text-webpack-plugin  --save-dev 
npm install fbjs-scripts jsdom minimist mocha  --save-dev 
npm install node-libs-browser react-addons-test-utils  --save-dev 
npm install selenium-webdriver sinon  --save-dev 

npm update npmconf cross-spawn-async jade graceful-fs  --save-dev
```

## 第一步
```
touch webpack.config.js

```
