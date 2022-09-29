---
title: "Como Instalar GIT"
subtitle: "Guía para instalar GIT en Windows, Linux y Mac."
tags: ["Instalar"]
date: 2022-09-29T03:07:18-03:00
description: "Guía para instalar GIT en Windows, Linux y Mac."
draft: false
toc:
  enable: true
  auto: true
---

# Como Instalar GIT
Como instalar GIT en Windows, Linux y Mac.

> Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente.

## Windows
Descargar desde [la página oficial de GIT](https://git-scm.com/download/win) y descargar la versión que nos corresponda, ya sea 32-bit o 64-bit.

Después de instalar, revisar versión con:
{{< highlight shell >}}
git --version
{{< / highlight >}}

Salida esperada:
{{< highlight shell >}}
git version 2.33.1.windows.1
{{< / highlight >}}

## Linux
En Linux va a depender la distro que se está utilizando, aquí está la [web de GIT con todos los comandos para instalación según la distro](https://git-scm.com/download/linux).\

Igual dejo la versión de Ubuntu como ejemplo.
Actualizar lista de paquetes con `apt-get update` y con `sudo` si es necesario.
{{< highlight bash >}}
sudo apt-get install git
{{< / highlight >}}

Revisar versión con:
{{< highlight bash >}}
git --version
{{< / highlight >}}

Salida esperada:
{{< highlight bash >}}
git version 2.25.1
{{< / highlight >}}

## Mac
En los sistemas Mac se puede utilizar Homebrew, ver [como instalar Homebrew aquí](/posts/instalar_homebrew/).

Instalar GIT utilizando Homebrew con el siguiente comando:
{{< highlight bash >}}
brew install git
{{< / highlight >}}

Revisar versión con:
{{< highlight bash >}}
git --version
{{< / highlight >}}

Salida esperada:
{{< highlight bash >}}
git version 2.25.1
{{< / highlight >}}


:link:[Web Oficial de GIT](https://git-scm.com) para documentación más detallada.
