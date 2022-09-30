---
title: "Como Instalar Homebrew"
subtitle: "Guía para instalar Homebrew en Linux y Mac."
tags: ["Instalar"]
date: 2022-09-28T03:54:39-03:00
description: "Guía para instalar Homebrew en Linux y Mac."
draft: false
toc:
  enable: true
  auto: true
---

# Homebrew
Com instalar Homebrew en Linux y Mac.

> Homebrew es un sistema de gestión de paquetes que simplifica la instalación, actualización y eliminación de programas en los sistemas operativos Mac OS de Apple y GNU/Linux.

## Terminal
Abrir `Terminal` y ejecutar el siguiente comando para descargar Hombrew:
{{< highlight bash >}}
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
{{< / highlight >}}

Revisar la versión con:
{{< highlight bash >}}
brew -v
{{< / highlight >}}

Salida esperada:
{{< highlight bash >}}
Homebrew 3.6.3
Homebrew/homebrew-core (git revision 2c17277b7fb; last commit 2022-09-28)
{{< / highlight >}}

:link:[Página Web de Homebrew](https://brew.sh/) para documentación más detallada.
