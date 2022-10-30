---
title: "Configurar React + Webpack + Babel"
subtitle: "Como configurar React más Webpack y Babel"
tags: ["Configurar"]
date: 2022-10-30T01:00:42-03:00
description: "Como configurar React más Webpack y Babel"
draft: false
toc:
  enable: true
  auto: true
---

# Crear directorios y archivos base
Crear `index.html`, `src/index.js` y `webpack.config.js`

+ index.html
+ /src
  + index.js
+ webpack.config.js

Inicializar proyecto
```bash
npm init
```

## Instalar Webpack
```bash
npm i --save-dev webpack webpack-cli webpack-dev-server html-webpack-plugin
```

### Configurar webpack
Agregar en `webpack.config.js`
```js
const HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
  mode: 'development',
  entry: './src/index.js',
  output: {
    filename: 'bundle.js'
  },
  plugins: [
  new HtmlWebpackPlugin({
    template: './index.html'
    })
  ]
}
```

## Instalar Babel
```bash
npm i --save-dev babel-loader @babel/core @babel/preset-env @babel/preset-react
```

### Configurar babel
Editar `webpack.config.js`
{{< highlight js "linenos=table,hl_lines=9-22,linenostart=1" >}}
const HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
  mode: 'development',
  entry: './src/index.js',
  output: {
    filename: 'bundle.js'
  },
  module: {
    rules: [
      {
      test: /\.js$/,
      exclude: /node_modules/,
        use:{
          loader: 'babel-loader',
          options:{
            presets: ['@babel/preset-env', '@babel/preset-react']
          }
        }
      }
    ]
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './index.html'
    })
  ]
}
{{< / highlight >}}

## Instalar React
```bash
npm i react react-dom
```

## Editar Index.html
```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
```

## Editar index.js
```js
import React from 'react';
import { createRoot } from 'react-dom/client';

const container = document.getElementById('root');
const root = createRoot(container);

root.render(<h1>Hola con React</h1>)
```

## Editar package.json
Remover `main` 

{{< highlight json "linenos=table,hl_lines=5 8-9,linenostart=1" >}}
{
  "name": "miWeb",
  "version": "1.0.0",
  "description": "simple app",
  "private": true,
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack",
    "dev": "webpack serve"
  },
  "author": "techeca",
  "license": "ISC",
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0"
  },
  "devDependencies": {
    "@babel/core": "^7.19.0",
    "@babel/preset-env": "^7.19.0",
    "@babel/preset-react": "^7.18.6",
    "babel-loader": "^8.2.5",
    "css-loader": "^6.7.1",
    "html-webpack-plugin": "^5.5.0",
    "style-loader": "^3.3.1",
    "webpack": "^5.74.0",
    "webpack-cli": "^4.10.0",
    "webpack-dev-server": "^4.11.0"
  }
}
{{< / highlight >}}

## Documentación
:link:[Web de Webpack](https://webpack.js.org/concepts/#entry)\
:link:[Web de Babel](https://babeljs.io/setup#installation)\
:link:[Web de React](https://reactjs.org/docs/react-dom-client.html)
