<div align="center">
<img src="/misc/readme/platinumBanner.png" style="width: 400px">
</div>

<h1 align="center">SRC README</h1>

Este fichero contiene toda la información para preparar su entorno de desarrollo y que este sea capaz de ejecutar Platinum de forma exitosa.

# Contenidos

- [Contenidos](#contenidos)
- [Preparativos](#preparativos)
  - [Requisitos](#requisitos)
  - [Dependencias NPM](#dependencias-npm)
  - [Dependencias Maven](#dependencias-maven)
  - [Demo Data Base](#demo-data-base)
  - [Application Secrets](#application-secrets)
  - [Checklist](#checklist)
- [Ejecución](#ejecución)
- [Acceso](#acceso)
  - [Usuarios Demo](#usuarios-demo)
  - [Crear Usuario](#crear-usuario)
- [Que hacer?](#que-hacer)

# Preparativos

Antes de ejecutar el proyecto Platinum es necesario realizar varios preparativos para que el entorno sea capaz de ejecutar el proyecto.

## Requisitos

| Tecnologia | Versión |
| ---------- | ------- |
| Node.js    | 18      |
| npm        | 11.11.1 |
| JDK        | 21      |
| SpringBoot | 4.0.1   |
| Maven      | 3.9.12  |
| PostgreSQL | 17      |

Una vez se tengan todos los requisitos preparados se puede continuar instalando dependencias.

## Dependencias NPM

Una vez se tenga **npm** operativo se deberá ejecutar el siguiente comando en la ruta `/src/frontend`:

```powershell
npm install
```

De esta forma se instalarán las dependencias del proyecto en el apartado de frontend.

## Dependencias Maven

Una vez se tenga **maven** operativo se deberá ejecutar el siguiente comando en la ruta `/src/backend`:

```powershell
mvn install
```

## Demo Data Base

Se provee al usuario con una base de datos de ejemplo. Dichos datos se encuentran en el archivo `/src/platinum.sql`.

Para su uso se debe acceder aal programa **pgAdmin** con la versión **v9.11** o posterior.

Una vez dentro:

- Crear la base de datos `platinum`
- - Username: `postgres`
- - Password: `root`
- Click derecho en la base de datos -> `Restore the file`
- - Formato: `Plain`
- - Seleccionar `/src/platinum.sql`

## Application Secrets

En el repositorio se incluye un archivo llamado `src/backend/src/main/resources/application-secrets-example.properties`.

Para que funcione correctamente será necesario renombrarlo a `application-secrets.properties`.

Dicho archivo es esencial para la correcta ejecución del backend ya que contiene, entre otros parametros, la clave privada para a **API de Steam**. Dicha clave puede ser obtenida de dos formas:

- Se envia la clave ya existente via email al comité para que estos la introduzcan en el código.
- Se pide una clave propia ya que son gratuitas y únicamente se requiere tener una cuenta válida de Steam.
> Para obtener la clave visita [Steam API Key](https://steamcommunity.com/dev/apikey)

> [!IMPORTANT]
> Es imperativo tener el archivo `application-secrets.properties` creado y con una **Steam API Key** válida para el correcto funcionamiento de la app.

## Checklist

A continuación se inncluye una checklist para ver si los preparativos se han seguido correctamente.

- [ ] Todos los [requisitos](#requisitos) están instalados y operativos.
- [ ] Las [dependencias](#dependencias-npm) de NPM están correctamente instaladas.
- [ ] Las [dependencias](#dependencias-maven) de Maven están correctamente instaladas.
- [ ] Se ha creado la [base de datos](#demo-data-base) correctamente y con los nombres exactos.
- [ ] Se ha creado el [application-secrets.properties](#application-secrets) con una clave para la API de Steam válida.

# Ejecución

Tras seguir los preparativos se podrá ejecutar la demo de Platinum.

> [!NOTE]
> Para que todo funcione correctamente **PostgreSQL** debe estar ejecutandose al momento de encender la aplicación.

En la carpeta `/src/frontend`:

```powershell
ng serve
```

En la carpeta `/src/backend`:

```powershell
mvn spring-boot:run
```

# Acceso

Tras acabar los preparativos se podrá acceder a la aplicación usando la URL http://localhost:4200.

## Usuarios Demo

Para iniciar sesión se puede hacer uso de una de las 3 cuentas por defecto que se proporcionan en el script de base de datos.

| Nombre de usuario | Contraseña    |
| ----------------- | ------------- |
| Luis              | Luis12345     |
| Cristian          | Cristian12345 |
| Erik              | Erik12345     |

## Crear Usuario

También es posible crear un usuario nuevo mediante la función de login. Dicho usuario **NO** tendrá una cuenta vinculada de Steam por defecto\* lo cual limitará sus funciones\*\*

<small>\* Para vincular una cuenta de Steam con la cuenta recién creada será necesario ser propietario de una cuenta de Steam y vincularla mediante el botón en el perfil de usuario.</small>
<small>\*\* Las cuentas de Platinum que no estén vinculadas con Steam no tendrán información en su perfil.</small>

# Que hacer?

Dentro de la aplicación se puede:

- Ver el catálogo de juegos registrados.
- Ver los logros de los juegos registrados.
- Buscar juegos.
- Ver juegos y logros propios.\*
- Buscar usuarios registrados.

<small>\* Únicamente si la cuenta está vinculada con Steam.</small>
