<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">FUNCIONALIDADES README</h1>

Funciones principales de Platinum explicadas y documentadas.

# Contenidos

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Contenidos](#contenidos)
- [Introducción](#introducción)
- [Autenticación de usuarios](#autenticación-de-usuarios)
- [Vinculación de cuenta con Steam](#vinculación-de-cuenta-con-steam)
- [Sincronización de biblioteca de juegos](#sincronización-de-biblioteca-de-juegos)
- [Visualización de juegos almacenados](#visualización-de-juegos-almacenados)

<!-- /code_chunk_output -->

# Introducción

Este documento recoge las funciones mas importantes de Platinum. Cada funcionalidad estará explicada en profundidad en un docuemnto a parte enlazado en cada punto.

Se explican 4 de las funciones mas importantes y complejas de Platinum. Ademas de ser complejas e importantes, estas funcionalidades comparten un flujo claro entre sí:

> Login con autenticación → Vinculación de cuenta → Sincronización de biblioteca → Visualización de juegos

# Autenticación de usuarios

**Descripción**: Encargada de verificar la identidad del usuario que accede al servicio Platinum para, posteriormente, autorizar su acceso a los recursos que se le permite acceso.

**Tecnologías**: `JWT`, `Spring Security`

**Detalles**: [README](/docs/funcionalidades/func1/README.md)

# Vinculación de cuenta con Steam

**Descripción**: El proceso mediante el cual Platinum es capaz de vincular una cuenta existente de Steam con una cuenta propia de Platinum. Necesario para poder vincular bibliotecas y que el usuario tenga juegos y logros registrados a su nombre con estadísticas personales.

**Tecnologías**: `JWT`, `Steam API`, `Spring Security`,

**Detalles**: [README](/docs/funcionalidades/func2/README.md)

# Sincronización de biblioteca de juegos

**Descripción**: Si el usuario tiene una cuenta de Steam activa vinculada Platinum se encargará de revisar si existen cambios en la misma para vincular la información entre Steam y Platinum. Este proceso permite realizar cambios en la información de un usuario como su nombre de usuario, foto de perfil, juegos adquiridos... de forma automática y periódica.

**Tecnologías**: `Steam API`, `Java Threads`, `Spring Boot`, `PostgreSQL`, `Repositories`

**Detalles**: [README](/docs/funcionalidades/func3/README.md)

# Visualización de juegos almacenados

**Descripción**: Permite acceder de forma controlada a todos los juegos almacenados en Platinum haciendo uso de paginación.

**Tecnologías**: `Spring Boot`, `Angular`, `Angular Stores`, `Repositories`

**Detalles**: [README](/docs/funcionalidades/func4/README.md)
