<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">DOCS README</h1>

Este documento recopila la documentación mas critica y necesaria para entender el funcionamiento interno de Platinum.

# Contenidos

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Contenidos](#contenidos)
- [Vista rápida](#vista-rápida)
  - [Objetivo](#objetivo)
  - [Tech stack principal](#tech-stack-principal)
  - [Arquitectura](#arquitectura)
  - [Estado](#estado)
- [¿Por donde empezar?](#por-donde-empezar)
- [Estructura de docs](#estructura-de-docs)
  - [Overview](#overview)
  - [Arquitectura](#arquitectura-1)
  - [Tecnologias](#tecnologias)
  - [Funcionalidades](#funcionalidades)
  - [Código](#código)

<!-- /code_chunk_output -->

# Vista rápida

## Objetivo

El objetivo de Platinum es el de proporcionar una **plataforma web eficiente y moderna** que permita a los usuarios consultar sus **juegos y logros** obtenidos en Steam además de proporcionar una funcionalidad social para interactuar con otros usuarios.

## Tech stack principal

<div>
<img src="https://img.shields.io/badge/springboot-59cc31?logo=spring&logoColor=ffffff&style=for-the-badge" />
<br>
Framework principal para el Backend usado por su versatilidad y soporte en desarrollo web.
</div><br>

<div>
<img src="https://img.shields.io/badge/angular-d7002f?logo=angular&logoColor=ffffff&style=for-the-badge" />
<br>
Framework escogido para construir el frontend, moderno, optimizado y ligero.
</div><br>

<div>
<img src="https://img.shields.io/badge/postgresql-2f6792?logo=postgresql&logoColor=ffffff&style=for-the-badge" />
<br>
Base de datos potente y robusta capaz de mantener grandes cantidades de datos.
</div>

## Arquitectura

Aplicacion web basada en filosofía **SPA** _(Single Page Application)_, con separación del Backend, Frontend y base de datos mediante capas siguiendo un modelo MVC.

## Estado

El proyecto se encuentra en constante desarrollo y evolución para las entregas.

Se proporciona una **demo** funcional en `/src`. Para preparar el entorno se recomienda leer el [README](/src/README.md) adjunto de `/src`.

# ¿Por donde empezar?

Para la evalucación del proyecto se recomienda primero hacer una lectura de los puntos mas importantes de `/docs` mostrados mas en adelante. Tras ello ejecutar la **demo** y revisar el resto de documentación en conjunto a la demo.

Los contenidos recomendados son:

- **Overview**: Una vista general y resumida del proyecto como conjunto.
- **Arquitectura**: Explicación de la arquitectura de Platinum.
- **Funcionalidades Clave**: Que es capaz de hacer Platinum y cómo.

# Estructura de docs

## Overview

**Carpeta:** `/docs/overview/`<br>
**Enlace:** [click aquí](/docs/overview/)<br>
**Resumen**: Descripción general y resumida del proyecto incluyedo objetivos, alcance decisiones importantes...

## Arquitectura

**Carpeta:** `/docs/arquitectura/`<br>
**Enlace:** [click aquí](/docs/arquitectura/)<br>
**Resumen**: Explicación de la arquitectura principal del proyecto incluyendo diagramas.

## Tecnologias

**Carpeta:** `/docs/tecnologias/`<br>
**Enlace:** [click aquí](/docs/tecnologias/)<br>
**Resumen**: Explicación de las tecnologias utilizadas y sus justificaciones.

## Funcionalidades

**Carpeta:** `/docs/funcionalidades/`<br>
**Enlace:** [click aquí](/docs/funcionalidades/)<br>
**Resumen**: Funciones principales de Platinum explicadas y documentadas.

## Código

**Carpeta:** `/docs/codigo/`<br>
**Enlace:** [click aquí](/docs/codigo/)<br>
**Resumen**: Explicación tecnica de bloques de codigo coplejas y relevantes.
