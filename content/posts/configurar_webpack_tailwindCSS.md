---
title: "Configurar Webpack TailwindCSS"
subtitle: "Como configurar Taildwind CSS con Webpack."
tags: ["Configurar"]
date: 2022-12-20T21:51:26-03:00
description: "Como configurar Taildwind CSS con Webpack."
draft: false
toc:
  enable: true
  auto: true
---

# Pre-Instalar CSS
```bash
npm i --save-dev css-loader style-loader postcss postcss-loader postcss-preset-env
```

## Configurar Webpack
Agregar `style-loader` y `css-loader` en `webpack.config.js`
```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.css$/,
        use: ["style-loader", "css-loader", "postcss-loader"],
      },
    ],
  },
};
```

### Configurar PostCSS
Crear archivo `postcss.config.js`
```js
const tailwindcss = require('tailwindcss');
module.exports = {
  plugins: [
    'postcss-preset-env',
    tailwindcss
  ],
};
```

## Instalar TailwindCSS
```bash
npm i -D tailwindcss
```

### Configurar TailwindCSS
Crear `tailwind.config.js` con:
```bash
npx tailwindcss init
```

Editar `tailwind.config.js`
{{< highlight js "linenos=table,hl_lines=2,linenostart=1" >}}
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
{{< / highlight >}}

Agregar `@taildwind` a CSS principal.
```CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Importar CSS en `index.js`.

## Documentación
:link:[Configurar React + Webpack + Babel](https://techeca.github.io/MiBew/posts/configurar_react_webpack_babel/)\
:link:[Web de Webpack](https://webpack.js.org/concepts/#entry)\
:link:[Web de TailwindCSS](https://tailwindcss.com/docs/installation)
