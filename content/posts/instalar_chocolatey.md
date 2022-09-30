---
title: "Como Instalar Chocolatey"
subtitle: "Guía para instalar Chocolatey en Windows."
tags: ["Instalar"]
date: 2022-09-28T00:59:58-03:00
description: "Guía para instalar Chocolatey en Windows."
draft: false
toc:
  enable: true
  auto: true
---

# Chocolatey
Como instalar Chocolatey en Windows (la única forma que he probado :clown_face:).

> Chocolatey es un gestor de paquetes de línea de comandos para Microsoft Windows. Utiliza la infraestructura de empaquetado de NuGet y PowerShell para simplificar el proceso de descarga e instalación de software.

Se puede utilizar `CMD` o `PowerShell`

## CMD
Abrir `CMD` con permisos de administrador y ejecutar:
{{< highlight bash >}}
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
{{< / highlight >}}

## PowerShell
Con `PowerShell`, ejecutar el siguiente comando:
{{< highlight shell >}}
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
{{< / highlight >}}

Revisar versión con:
{{< highlight bash >}}
choco --v
{{< / highlight >}}

Salida esperada:
{{< highlight bash >}}
Chocolatey v0.11.2
{{< / highlight >}}

:link:[Web oficial de Chocolatey](https://chocolatey.org/install) para documentación más detallada.
