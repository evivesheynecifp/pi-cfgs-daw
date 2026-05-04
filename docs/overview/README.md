<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">OVERVIEW README</h1>

# Contenidos

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Contenidos](#contenidos)
- [Introducción](#introducción)
- [Motivación](#motivación)
- [Objetivos](#objetivos)
  - [Funcionalidades](#funcionalidades)
  - [Backend](#backend)
  - [Base de datos](#base-de-datos)
  - [Frontend](#frontend)

<!-- /code_chunk_output -->


# Introducción

Platinum se trata de una aplicación web de arquitectura SPA con el principal objetivo de diseñar y proponer una plataforma web que permita a los usuarios gestionar, discutir y visualizar información relevante sobre los juegos y logros de Steam que ellos posean o estén disponibles en la web.

El funcionamiento de Platinum depende en gran medida de la API pública de Steam, la cual permite obtener la informacion necesaria sobre los juegos, logros, desarrolladores, clasificaciones...

# Motivación

La principal motivación de este proyecto es personal, debido a mi uso constante de plataformas de compraventa de videojuegos tales como Steam, Epic Games, Origin y GoG, entre otros, siempre he tenido una necesidad y curiosidad de ver de forma centralizada los logros que yo obtengo en todos mis juegos adquiridos en diversas plataformas.

Este proyecto tambien se centra en resolver el problema de la falta de centralización de gestión de logros indiferentemente de las plataformas de donde provengan los títulos. Otro de los problemas que se identifican es la falta de intuitividad en las herramientas existentes para gestionar y visualizar los logros, por lo que el proyecto también se enfoca en gran medida a desarrollar un producto fácil e intuitivo para los usuarios.

# Objetivos

El principal objetivo de Platinum es proponer una aplicación web que permita a los usuarios gestionar y visualizar información específica y relacionada a los videojuegos, como logros, mediante una interfaz intuitiva y ligera que se alimente parcialmente por datos externos de la API de Steam.

Como objetivos específicos encontramos:

## Funcionalidades

- Permitir registrarse e iniciar sesión como usuario regular.
- Permitir vincular la cuenta de Platinum con una cuenta existente y vacante de Steam.
- Visualizar una lista de los juegos almacenados.
- Visualizar datos concretos de un videojuego almacenado.
- Visualizar logros globales de un videojuego almacenado.
- Visualizar los logros de un usuario sobre un videojuego almacenado.
- Visualizar perfiles de usuarios registrados.
- Separar funcionalidades para usuarios invitados, registrados y administradores.
- Gestionar perfil de usuario.

## Backend

- Diseñar, desarrollar y documentar una API REST.
- Gestionar peticiones HTTP.
- Tratar datos correctamente, tomando como referencia la API de Steam y la Base de Datos.
- Implementar lógica para controlar errores.

## Base de datos

- Diseñar modelos de entidad relación.
- Asegurar la relación de los datos con la lógica de negocio.

## Frontend

- Diseñar frameworks y bocetos de la interfaz.
- Desarrollar una UI siguiendo la lógica de una SPA.
- Mantener coherencia visual en todas las vistas.
- Mantener la simplicidad por encima de la complejidad.
