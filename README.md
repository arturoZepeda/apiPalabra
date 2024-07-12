CRUD API en Go

Esta es una API sencilla en Go que permite realizar operaciones CRUD (Crear, Leer, Actualizar y Eliminar) en una base de datos. Esta API está diseñada para ser fácil de usar y extender.
Requisitos

    Go 1.16 o superior
    Una base de datos compatible (MySQL, PostgreSQL, etc.)

Instalación

    Clona el repositorio:

    bash

git clone https://github.com/tu-usuario/tu-repo.git
cd tu-repo

Instala las dependencias:

bash

go mod download

Configura la base de datos en el archivo config.yaml:

yaml

database:
  host: "localhost"
  port: 3306
  user: "tu-usuario"
  password: "tu-contraseña"
  name: "tu-base-de-datos"

Ejecuta la aplicación:

bash

    go run main.go

Endpoints
Crear

    URL: /items

    Método: POST

    Cuerpo de la solicitud:

    json

{
  "nombre": "Nombre del item",
  "descripcion": "Descripción del item"
}

Respuesta exitosa:

json

    {
      "id": 1,
      "nombre": "Nombre del item",
      "descripcion": "Descripción del item",
      "creado_en": "2024-07-11T00:00:00Z"
    }

Leer

    URL: /items

    Método: GET

    Respuesta exitosa:

    json

[
  {
    "id": 1,
    "nombre": "Nombre del item",
    "descripcion": "Descripción del item",
    "creado_en": "2024-07-11T00:00:00Z"
  }
]

URL: /items/{id}

Método: GET

Parámetros de URL:

    id (integer): ID del item

Respuesta exitosa:

json

    {
      "id": 1,
      "nombre": "Nombre del item",
      "descripcion": "Descripción del item",
      "creado_en": "2024-07-11T00:00:00Z"
    }

Actualizar

    URL: /items/{id}

    Método: PUT

    Parámetros de URL:
        id (integer): ID del item

    Cuerpo de la solicitud:

    json

{
  "nombre": "Nombre actualizado del item",
  "descripcion": "Descripción actualizada del item"
}

Respuesta exitosa:

json

    {
      "id": 1,
      "nombre": "Nombre actualizado del item",
      "descripcion": "Descripción actualizada del item",
      "actualizado_en": "2024-07-11T00:00:00Z"
    }

Eliminar

    URL: /items/{id}

    Método: DELETE

    Parámetros de URL:
        id (integer): ID del item

    Respuesta exitosa:

    json

    {
      "mensaje": "Item eliminado exitosamente"
    }

Contribuir

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request.
Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
