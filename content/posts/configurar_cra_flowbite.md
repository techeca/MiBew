---
title: "Configurar CRA + Flowbite"
subtitle: "Como configurar create react app con Flowbite."
tags: ["Configurar"]
date: 2022-09-28T00:59:58-03:00
description: "Como configurar create react app con Flowbite."
draft: false
---

# Create React App
Para crear una app limpia
{{< highlight bash >}}
npx create-react-app miapp
{{< / highlight >}}

# Tailwind + Flowbite
Instalar Tailwind con Flowbite
{{< highlight bash >}}
npm install -D tailwindcss flowbite
npx tailwindcss init
{{< / highlight >}}

Configurar `tailwind.config.js`
{{< highlight bash >}}
module.exports = {
  darkMode: 'media',
  content: [
    "./src/**/*.{js,jsx,ts,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [require('flowbite/plugin')],
}
{{< / highlight >}}

Agregar en `src/App.css`
{{< highlight bash >}}
@tailwind base;
@tailwind components;
@tailwind utilities;
{{< / highlight >}}

Agregar script tag para animaciones, funciones, etc en `public/index.html`
{{< highlight bash >}}
<script src="https://unpkg.com/flowbite@1.5.3/dist/flowbite.js"></script>
{{< / highlight >}}

o

Instalar Flowbite-react
{{< highlight bash >}}
npm i flowbite flowbite-react
{{< / highlight >}}
