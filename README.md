# literalura-catalog


Crea una aplicación de consola llamada LiterAlura utilizando Java y Spring Boot. Esta aplicación será un catálogo de libros que permitirá a los usuarios registrar libros en una base de datos y obtener información sobre los libros registrados. Sigue estas especificaciones:

1. Configuración del proyecto:
   - Utiliza Maven como sistema de gestión de proyectos
   - Lenguaje: Java
   - Versión de Spring Boot: 3.3.1
   - Group: pa.com.alura
   - Artifact: literalura
   - Package name: pa.com.alura.literalura
   - Packaging: JAR
   - Versión de Java: 17

2. Dependencias principales:
   - Spring Data JPA
   - PostgreSQL Driver

3. Base de datos:
   - Utiliza PostgreSQL como sistema de gestión de base de datos y con estos datos en application.properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/literalura
spring.datasource.username=postgres
spring.datasource.password=qwqw

4. Funcionalidades principales:
   a. Buscar libro por título:
      - El usuario ingresa el nombre del libro
      - La aplicación busca la información en la API Gutendex (https://gutendex.com/)
      - Si el libro se encuentra, se registra en la base de datos local
      - Muestra la información del libro: título, autor (apellido, nombre), idioma y número de descargas

   b. Listar libros registrados:
      - Muestra todos los libros almacenados en la base de datos local

   c. Listar autores registrados:
      - Muestra todos los autores de los libros almacenados en la base de datos local
      - Evita duplicados (un autor con múltiples libros solo aparece una vez)

   d. Listar autores vivos en un año específico:
      - El usuario ingresa un año
      - La aplicación muestra los autores que estaban vivos en ese año

   e. Listar libros por idioma:
      - El usuario ingresa un código de idioma (ES, EN, FR, PT)
      - La aplicación muestra los libros en ese idioma

5. Manejo de errores:
   - Si el libro no se encuentra en la API, mostrar un mensaje apropiado
   - Evitar la inserción de libros duplicados en la base de datos

6. Interfaz de usuario:
   - Implementar un menú de consola que permita al usuario seleccionar entre las diferentes funcionalidades

7. Consumo de API:
   - Utilizar la API Gutendex (https://gutendex.com/) para obtener información de los libros
   - Implementar métodos para parsear y manejar la respuesta JSON de la API

8. Modelado de datos:
   - Crear entidades JPA para Libro y Autor con los campos necesarios
   - Implementar relaciones apropiadas entre las entidades

9. Repositorios y servicios:
   - Crear repositorios Spring Data JPA para las entidades
   - Implementar servicios que manejen la lógica de negocio y las operaciones con la base de datos

10. Manejo de excepciones:
    - Implementar un manejo adecuado de excepciones para errores de API, base de datos y entrada de usuario

11. Logging:
    - Implementar logging para registrar operaciones importantes y errores

12. Consideraciones adicionales:
    - Seguir las mejores prácticas de programación en Java y Spring
    - Utilizar nombres de variables y métodos descriptivos en español
    - Documentar el código adecuadamente
    - Implementar pruebas unitarias para las funcionalidades principales

13. Funcionalidades opcionales (si el tiempo lo permite):
    - Implementar paginación para las listas de libros y autores
    - Agregar funcionalidad de búsqueda avanzada (por autor, año de publicación, etc.)
    - Implementar un sistema de calificación para los libros
    - Agregar la capacidad de exportar la lista de libros a un archivo CSV o JSON

14. Recursos adicionales:
    - Consultar el tablero de Trello del desafío para obtener más detalles y consejos
    - Utilizar el servidor de Discord para resolver dudas y compartir avances

Recuerda que la aplicación debe ser solo de consola, sin necesidad de implementar una interfaz gráfica. Enfócate en la correcta implementación de las funcionalidades y en la interacción con la API y la base de datos. 

## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with React with shadcn-ui and Tailwind CSS.

- Vite
- React
- shadcn/ui
- Tailwind CSS

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/literalura-catalog.git
cd literalura-catalog
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
