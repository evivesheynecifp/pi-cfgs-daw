<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">FUNCIONALIDAD README</h1>
<h2 align="center">Autenticación de usuarios</h2>

Funciones principales de Platinum explicadas y documentadas.

# Contenidos

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Contenidos](#contenidos)
- [Descripción](#descripción)
- [Flujo](#flujo)
- [Componentes](#componentes)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Base de Datos](#base-de-datos)
- [Detalles](#detalles)
- [Decisiones y comentarios](#decisiones-y-comentarios)

<!-- /code_chunk_output -->

# Descripción

Esta funcionalidad permite a los usuarios registrarse e iniciar sesión en Platinum con una cuenta propia. Esto les habilita a acceder a los contenidos protegidos bajo autorización.

Se hace uso de JWT (Java Web Tokens) para gestionar la autenticación y posterior autorización.

# Flujo

1. Se introducen las credenciales en la web (Frontend Angular)
2. Se envia una petición del Frontend al Backend mediante HTTP al endpoint `auth/login`
3. El Backend recibe la petición en el Controlador
4. El servicio de autenticación toma los datos y valida las credenciales mediante JWT
5. Se genera un token JWT en caso de validarse correctamente
6. Se devuelve una respuesta mediante HTTP con el token generado
7. El frontent guarda el token JWT para su posterior uso en las peticiones fuera de `auth`

# Componentes

## Frontend

- Formulario de login/registro
- Comunicación asíncrona mediante HTTP
- Gestión y almacenamiento de la respuesta `localstorage`

## Backend

- Controlador de autenticación
- Servicio de autenticación
- Implementación JWT

## Base de Datos

- Verificación de datos
- Almacenamiento de datos cifrados

# Detalles

- La autenticación se lleva a cabo mediante tokens JWT debido a su simpleza pero efectividad para esta tarea.
- Uso de contraseñas cifradas en la base de datos. La verificación se realiza mediante comparación de cifrados con JWT.
- Protección de rutas mediante interceptores haciendo uso del token y la tecnologia JWT.

# Decisiones y comentarios

- La base de todo el proceso se mantiene "stateless" gracias a JWT.
