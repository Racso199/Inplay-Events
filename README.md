# Inplay-Events

### Plataforma web para la gestión integral de un club de pádel

**Inplay-Events** es una aplicación web diseñada para centralizar y automatizar la gestión de un club de pádel.

El sistema permite administrar reservas de pistas, ligas, resultados, clases deportivas y comunicaciones internas, sustituyendo procesos manuales y dispersos por una plataforma única accesible desde el navegador.

El proyecto está orientado a entornos reales de clubes deportivos y ofrece funcionalidades diferentes dependiendo del perfil de cada usuario.

---

## Objetivos del proyecto

- Digitalizar la gestión diaria de un club de pádel.
- Facilitar la reserva de pistas y clases.
- Implementar un sistema de ligas con categorías y divisiones.
- Permitir a los usuarios registrar resultados.
- Actualizar automáticamente las clasificaciones.
- Centralizar las noticias y avisos del club.
- Ofrecer una interfaz moderna, responsive y accesible.

---

## Funcionalidades principales

- Registro e inicio de sesión.
- Gestión de usuarios y roles.
- Reserva y administración de pistas.
- Gestión de clases, profesores y grupos de alumnos.
- Creación y administración de ligas.
- Registro de resultados.
- Actualización de clasificaciones.
- Publicación de noticias y comunicaciones.
- Página pública de contacto.
- Acceso diferenciado según el perfil del usuario.

---

## Perfiles de usuario

### Administrador

Dispone del control global del sistema: usuarios, roles, ligas, pistas, contenidos y configuración general.

### Profesor

Puede gestionar clases, grupos de alumnos y horarios.

### Usuario básico

Puede reservar pistas, inscribirse en ligas, registrar resultados, consultar clasificaciones y gestionar su actividad deportiva.

### Usuario invitado

Puede consultar el contenido público de la plataforma, como noticias, ligas y disponibilidad de pistas.

---

## Tecnologías empleadas

### Frontend

- HTML5
- CSS3
- JavaScript
- React
- React Router
- Bootstrap
- React Bootstrap
- Vite

### Backend

- Java 17
- Spring Boot
- Spring Security
- Spring Data JPA
- API REST
- Arquitectura MVC
- Maven

### Base de datos

- MariaDB

### Herramientas

- Git
- GitHub
- IntelliJ IDEA
- Visual Studio Code
- Eclipse
- Postman
- npm

---

## Estructura del proyecto

```text
Inplay-Events/
├── backend/
│   └── InplayEvents/
├── database/
├── documentacion_proyecto/
├── frontend/
├── .github/
│   └── workflows/
├── .gitignore
├── LICENSE
└── README.md
```

---

## Cómo ejecutar el proyecto

### Requisitos previos

Para ejecutar la aplicación es necesario tener instalado:

- Java 17
- Maven 3.8 o superior
- Node.js 20.19 o superior
- npm
- MariaDB
- Git

---

### 1. Clonar el repositorio

```bash
git clone https://github.com/Racso199/Inplay-Events.git
cd Inplay-Events
```

---

### 2. Configurar la base de datos

Acceder a MariaDB y crear la base de datos:

```sql
CREATE DATABASE club_padel
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;
```

Importar el script incluido en el proyecto:

```bash
mysql -u root -p club_padel < database/clubpadel.sql
```

La configuración de conexión se encuentra en:

```text
backend/InplayEvents/src/main/resources/application.properties
```

El usuario y la contraseña deben adaptarse a la configuración local de MariaDB.

---

### 3. Ejecutar el backend

Desde la raíz del repositorio:

```bash
cd backend/InplayEvents
mvn clean install
mvn spring-boot:run
```

También puede generarse y ejecutarse el archivo JAR:

```bash
mvn clean package
java -jar target/InplayEvents-0.0.1-SNAPSHOT.jar
```

---

### 4. Ejecutar el frontend

En otra terminal, desde la raíz del repositorio:

```bash
cd frontend
npm install
npm run dev
```

Vite mostrará en la terminal la dirección local desde la que se puede abrir la aplicación.

---

## Mi contribución al proyecto

Este proyecto fue desarrollado de forma colaborativa como proyecto académico del ciclo de Desarrollo de Aplicaciones Web.

Mi principal responsabilidad fue el diseño y desarrollo del frontend de la aplicación, del que realicé prácticamente la totalidad.

Mi aportación incluyó:

- Diseño y desarrollo de la interfaz de usuario.
- Organización y estructuración del frontend con React.
- Creación de componentes y páginas reutilizables.
- Implementación de rutas y navegación mediante React Router.
- Desarrollo de las interfaces correspondientes a los diferentes perfiles de usuario.
- Creación y adaptación de formularios.
- Desarrollo de la página pública de contacto.
- Implementación de la ruta pública de contacto.
- Diseño de accesos rápidos y elementos de navegación.
- Maquetación responsive mediante HTML, CSS y Bootstrap.
- Aplicación de estilos y mejoras en la experiencia de usuario.
- Integración del frontend con los servicios proporcionados por el backend.
- Corrección de errores y adaptación de contenidos e interfaces.
- Participación en el prototipado y diseño general de la aplicación.
- Trabajo colaborativo y control de versiones mediante Git y GitHub.

Durante el desarrollo trabajé principalmente con React, JavaScript, HTML, CSS, Bootstrap, React Router, Vite, Git y GitHub, además de colaborar en la integración con el backend desarrollado mediante Java y Spring Boot.

Las contribuciones realizadas pueden consultarse en el historial de commits del repositorio.

---

## Desarrollo colaborativo

El proyecto fue desarrollado conjuntamente por:

- [Óscar Hernández — Racso199](https://github.com/Racso199): responsable principal del diseño y desarrollo del frontend.
- [Luisma34](https://github.com/Luisma34): responsable principal del desarrollo del backend y la base de datos.

Ambos participantes colaboraron en la planificación, integración y evolución general del proyecto. El historial de Git conserva la autoría individual de las diferentes contribuciones.

---

## Documentación

El repositorio incluye documentación adicional relacionada con el análisis, diseño y prototipado de la aplicación en el directorio:

```text
documentacion_proyecto/
```

---

## Estado del proyecto

El proyecto dispone de una versión funcional desarrollada con fines académicos y de aprendizaje.

Entre sus posibles mejoras futuras se encuentran:

- Ampliación de las pruebas automatizadas.
- Mejora de la gestión de errores.
- Refuerzo de la seguridad y validación de datos.
- Incorporación de nuevas estadísticas para las ligas.
- Despliegue completo en un entorno de producción.
- Mejora continua de la experiencia de usuario.

---

## Licencia

Este proyecto incluye un archivo `LICENSE` en el que se especifican sus condiciones de uso.