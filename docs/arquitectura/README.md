<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">ARQUITECTURA README</h1>

Explicación de la arquitectura principal del proyecto incluyendo diagramas.

# Contenidos

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Contenidos](#contenidos)
- [Introducción](#introducción)
- [Diagrama](#diagrama)
- [Flujo de una petición](#flujo-de-una-petición)
- [Capas Backend](#capas-backend)
  - [Controlador](#controlador)
  - [Servicios](#servicios)
  - [Repositorios](#repositorios)
- [Comunicacion Cliente-Servidor](#comunicacion-cliente-servidor)

<!-- /code_chunk_output -->

# Introducción

Platinum se ha desarrollado como una aplicación web SPA (Single Page Application) siguiendo una arquitectura cliente-servidor para la separación del Frontend y Backend.

En el Backend se implementa la arquitectura MVC (Modelo Vista Controlador) que separa la logica por controladores, servicios, respositorios... Este enfoque es el mas adecuado para el framework del backend Springboot y permite estructurar el código de forma modular.

Para el Frontend, desarrollado en Angular, se enfoca el desarrollo como una capa independiente que se encarga de la presentación y la interacción.

Para las comunicaciones entre Frontend y Backend se hace uso de la comunicación Cliente-Servidor mediante una API REST desarrollada en el Backend. El frontent consume la API del backend mediante peticiones HTTP y el backend se hace responsable de conectarse a la base de datos para recopilar o modificar los datos que el cliente necesita.

# Diagrama

<div align="center">
<img src="/misc/docs/arquitectura/platinum_diagrama_de_arquitectura.png" width=500>

Platinum - Diagrama de Arquitectura

</div>

# Flujo de una petición

El flujo de una petición en Platinum es sencilla y sigue las convenciones de una arquitectura Cliente-Servidor basada en una comunicación HTTP.

1. El usuario interactúa con la interfaz del Frontend - <small>Acceder a un título de la lista</small>
2. El Frontent envía una petición HTTP a la API en el Backend
3. El Backend recibe la petición
4. El Controlador identifica la petición y relega la lógica
5. El Servicio procesa la lógica, apoyandose de otros servicios si es necesario
6. El Repositorio accede a la base de datos mediante la comunicacion de JPA
7. Se prepara la respuesta en el Backend
8. El Backend devuelve una respuesta mediante HTTP
9. El Frontend recibe y procesa el JSON de la respuesta
10. Se actualiza el Frontend

# Capas Backend

El Backend sigue una arquitectura MVC marcada por el framework de Springboot. Esto le obliga a separar el codigo identificando 3 piezas importantes:

## Controlador

Es la capa encargada de:

- Exponer endpoints de la API REST
- Recibir y gestionar peticiones HTTP

## Servicios

Son los encagrados de:

- Contener y ejecutar lógica de negocio
- Orquestrar operaciones y relaciones entre el controlador y otras partes críticas del Backend

## Repositorios

La capa responsable de:

- Acceder a los datos mediante la comunicacion JPA
- Interactuar con PostgreSQL

# Comunicacion Cliente-Servidor

La comunicación cliente servidor se lleva a cabo mediante el protocolo HTTP haciendo uso de una API REST. Esta comunicacion API REST esta gestionada mediante tokens JWT para la autorización y autenticación a la hora de acceder a los datos.

La comunicación establecida se mantiene "stateless", es decir, no se guarda información entre peticiones, cada petición envia toda la información necesaria y son independientes entre sí.
