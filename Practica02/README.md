# 🌸 Práctica 02 — Boceto de Arquitectura del Proyecto Integrador

<p align="center">
  💗✨ <strong>Práctica 02 — Integradora</strong> ✨💗
</p>

<p align="center">
  🌷 Boceto inicial de la arquitectura del Proyecto Integrador 🌷
</p>

---
### 🌸 Diagrama interactivo

<p align="center">

**✨ [Ver Diagrama de Arquitectura Interactivo](https://diegomiguel04.github.io/Practicas-INTEGRADORA/Practica02/index.html) ✨**

</p>

El enlace permite acceder directamente al modelo arquitectónico generado durante la práctica.

---
## 🎀 Descripción

En esta práctica se realizó un **primer boceto de la arquitectura del Proyecto Integrador**, con la finalidad de representar de manera visual los principales componentes que formarán parte del sistema y la forma en que estos se relacionan entre sí.

Para la elaboración del modelo se utilizó **Archify** como herramienta de modelado arquitectónico, apoyándose en **Codex** para generar el diagrama a partir de un prompt con las características principales del sistema.

El resultado obtenido es un **diagrama de arquitectura interactivo en formato HTML**, en el cual se pueden identificar las diferentes capas del sistema, los servicios que participan en la aplicación, las bases de datos y algunos de los principales flujos de información.

Esta práctica permitió tener una primera representación de cómo podría estar organizado el Proyecto Integrador antes de comenzar con el desarrollo completo de sus diferentes componentes.

---

## 🌷 Objetivo de la práctica

El objetivo principal de esta práctica es **crear un primer modelo de la arquitectura del Proyecto Integrador**, identificando los componentes principales del sistema y la relación existente entre ellos.

También se busca:

* 💗 Conocer y utilizar **Archify** como herramienta de modelado.
* 💗 Utilizar **Codex** como apoyo para la generación del modelo arquitectónico.
* 💗 Representar visualmente los componentes del sistema.
* 💗 Identificar las diferentes capas que forman parte de la aplicación.
* 💗 Representar los principales flujos de información.
* 💗 Identificar los servicios externos utilizados por el sistema.
* 💗 Reconocer los límites de confianza entre los diferentes componentes.
* 💗 Generar un modelo arquitectónico en formato interactivo.
* 💗 Publicar el resultado mediante **GitHub Pages**.
* 💗 Documentar el proceso realizado durante la práctica.

---

## 🎀 Herramientas utilizadas

Durante el desarrollo de esta práctica se utilizaron diferentes herramientas y tecnologías relacionadas con el modelado, desarrollo y administración del proyecto.

| 🌸 Herramienta             | 💕 Utilidad                                                                       |
| -------------------------- | --------------------------------------------------------------------------------- |
| **Archify**                | Herramienta utilizada para generar y visualizar el modelo arquitectónico.         |
| **Codex CLI**              | Herramienta utilizada como apoyo para generar el diagrama mediante instrucciones. |
| **ChatGPT**                | Plataforma utilizada para la vinculación y apoyo durante el uso de Codex.         |
| **NPM**                    | Administrador de paquetes utilizado para verificar el entorno necesario.          |
| **Flutter**                | Tecnología considerada para el desarrollo de la aplicación móvil.                 |
| **Keycloak**               | Servicio considerado para la autenticación de usuarios.                           |
| **FastAPI**                | Framework utilizado para representar la API REST del sistema.                     |
| **PostgreSQL**             | Sistema de base de datos relacional considerado para el proyecto.                 |
| **MongoDB**                | Base de datos orientada a documentos considerada dentro de la arquitectura.       |
| **Leaflet / Maps Service** | Servicio considerado para las funciones relacionadas con mapas.                   |
| **Docker**                 | Tecnología utilizada para la contenerización de los servicios.                    |
| **Docker Compose**         | Herramienta considerada para administrar los diferentes contenedores.             |
| **Git**                    | Sistema utilizado para el control de versiones.                                   |
| **GitHub**                 | Plataforma utilizada para almacenar y administrar el repositorio.                 |
| **GitHub Pages**           | Servicio utilizado para publicar el diagrama interactivo.                         |

---

# 💗 Arquitectura del sistema

La arquitectura propuesta está compuesta por diferentes elementos que trabajan en conjunto para formar el sistema.

De manera general, la aplicación se plantea como una **aplicación móvil desarrollada con Flutter**, la cual se comunica con una API REST desarrollada con **FastAPI**.

Antes de acceder a los servicios principales del sistema, se considera una capa de autenticación mediante **Keycloak**, encargada de gestionar el acceso de los usuarios.

La API se comunica con diferentes sistemas de almacenamiento, principalmente **PostgreSQL** y **MongoDB**, dependiendo del tipo de información que sea necesario manejar.

También se contempla el uso de un servicio de mapas basado en **Leaflet / Maps Service** para las funcionalidades que requieran información geográfica.

Todo el entorno de desarrollo y ejecución puede ser administrado mediante **Docker y Docker Compose**, facilitando la organización de los diferentes servicios que forman parte del sistema.

---

## 🌸 Componentes principales

### 📱 Flutter Mobile App

La aplicación móvil representa el cliente principal del sistema.

Desde esta aplicación el usuario podrá interactuar con las diferentes funcionalidades que posteriormente serán conectadas con la API REST.

La aplicación será responsable de presentar la información al usuario y enviar las solicitudes correspondientes al servidor.

---

### 🔐 Keycloak Authentication

**Keycloak** se considera como el servicio encargado de la autenticación.

Su función dentro de la arquitectura es permitir la gestión del acceso de los usuarios al sistema y establecer una capa de seguridad antes de acceder a determinados recursos.

De esta manera, la aplicación móvil puede realizar el proceso de autenticación y posteriormente comunicarse con los servicios que requieren autorización.

---

### ⚡ FastAPI REST API

**FastAPI** representa la capa principal de servicios del sistema.

Esta API funciona como intermediaria entre la aplicación móvil y los diferentes recursos del backend.

A través de ella se podrán recibir solicitudes desde la aplicación, procesar información y comunicarse con las bases de datos correspondientes.

La API también permite organizar los diferentes endpoints que serán utilizados por la aplicación móvil.

---

### 🐘 PostgreSQL

**PostgreSQL** representa la base de datos relacional dentro de la arquitectura.

Se contempla para almacenar información que requiere una estructura organizada mediante tablas y relaciones.

La comunicación con PostgreSQL se realiza mediante la capa de la API, evitando que la aplicación móvil tenga acceso directo a la base de datos.

---

### 🍃 MongoDB

**MongoDB** representa la base de datos orientada a documentos.

Su inclusión dentro de la arquitectura permite contemplar información que pueda manejarse mediante documentos y estructuras más flexibles.

Al igual que PostgreSQL, la comunicación con MongoDB se realiza mediante la API.

---

### 🗺️ Leaflet / Maps Service

El servicio de mapas se contempla para las funcionalidades relacionadas con información geográfica.

**Leaflet** permite representar mapas de manera interactiva y puede utilizarse junto con diferentes servicios de mapas para mostrar ubicaciones, puntos o información geográfica.

Este componente se considera un servicio externo dentro de la arquitectura.

---

# 🎀 Infraestructura de desarrollo

Además de los componentes principales del sistema, se considera una infraestructura basada en contenedores.

### 🐳 Docker

Docker permite trabajar con los diferentes servicios del proyecto utilizando contenedores.

Cada servicio puede mantenerse aislado y configurado de acuerdo con sus propias necesidades.

Esto facilita la organización del entorno de desarrollo y permite que los componentes puedan ejecutarse de una manera más controlada.

### 🐳 Docker Compose

Docker Compose se considera para administrar varios contenedores al mismo tiempo.

De esta manera, los diferentes servicios que forman parte de la arquitectura pueden ser configurados y ejecutados como parte de un mismo entorno.

---

# 🌷 Control de versiones

Para llevar un control de los cambios realizados durante la práctica se utilizó **Git**.

El proyecto se almacenó en **GitHub**, permitiendo mantener un historial de los cambios realizados mediante diferentes commits.

Durante el desarrollo de la práctica también se trabajó con la rama:

```text
Practica02
```

Posteriormente, los cambios fueron integrados a la rama principal:

```text
main
```

Esto permitió mantener organizada la evolución del proyecto y conservar un registro de las modificaciones realizadas.

---

# 💕 GitHub Pages

Una de las actividades realizadas fue la publicación del diagrama arquitectónico mediante **GitHub Pages**.

Gracias a esto, el modelo generado en HTML puede consultarse directamente desde un navegador sin necesidad de descargar los archivos del repositorio.



# 🎀 Evidencia del trabajo realizado

Como evidencia del resultado obtenido se incluye una captura del diagrama arquitectónico generado.

<p align="center">
  <img src="mobile-system-architecture.visual-check.1440x900.dark.png" alt="Diagrama de arquitectura del Proyecto Integrador" width="950">
</p>

### 🌸 Descripción de la evidencia

En la imagen se pueden observar los principales componentes considerados para la arquitectura del sistema.

Entre ellos se encuentran:

* 📱 Aplicación móvil.
* 🔐 Servicio de autenticación.
* ⚡ API REST.
* 🐘 PostgreSQL.
* 🍃 MongoDB.
* 🗺️ Servicio de mapas.
* 🐳 Infraestructura de desarrollo.
* 🐙 Control de versiones.
* 🔗 Relaciones y flujos entre los diferentes componentes.

---

# 🌷 Actividades realizadas

Para completar la práctica se siguió una serie de actividades relacionadas con la preparación del entorno, generación del modelo y publicación de los resultados.

### 💗 1. Verificación de NPM

Se realizó la verificación de la instalación de **NPM**, con la finalidad de comprobar que el entorno contara con las herramientas necesarias para continuar con la configuración.

### 💗 2. Instalación de Codex CLI

Posteriormente se realizó la instalación de **Codex CLI**, herramienta utilizada para trabajar con las instrucciones necesarias para la generación del modelo.

### 💗 3. Instalación de Archify

Se instaló y configuró **Archify**, utilizado como herramienta para crear la representación visual de la arquitectura.

### 💗 4. Vinculación de Codex con ChatGPT

Se realizó la vinculación de la cuenta de **Codex con ChatGPT** para poder utilizar la herramienta durante el desarrollo del modelo.

### 💗 5. Elaboración del prompt

Se preparó un prompt especificando los principales componentes que debían aparecer en el modelo arquitectónico.

### 💗 6. Generación del modelo

A partir del prompt se generó el primer modelo arquitectónico utilizando Archify.

### 💗 7. Generación del HTML

El modelo fue generado en formato **HTML**, permitiendo contar con una versión interactiva que posteriormente podía ser publicada.

### 💗 8. Organización de los archivos

Los documentos generados fueron agregados al repositorio dentro de la rama correspondiente a la práctica.

```text
Practica02
```

### 💗 9. Realización de commits

Se realizaron diferentes commits para registrar los cambios efectuados durante el desarrollo de la práctica.

### 💗 10. Publicación en GitHub

Los cambios fueron enviados al repositorio remoto utilizando Git.

### 💗 11. Configuración de GitHub Pages

Se habilitó **GitHub Pages** para poder consultar el modelo arquitectónico directamente desde un navegador.

### 💗 12. Documento de evidencias

También se elaboró un documento en formato PDF para registrar las evidencias correspondientes a las actividades realizadas.

### 💗 13. Actualización del repositorio

Se actualizó la tabla general de prácticas para incluir la nueva **Práctica 02**.

### 💗 14. Fusión de ramas

Finalmente, se realizó la fusión de la rama:

```text
Practica02
```

con:

```text
main
```

De esta manera, los cambios realizados durante la práctica quedaron integrados en la rama principal del repositorio.

---

# 🌸 Prompt utilizado

El siguiente prompt fue utilizado para solicitar la generación del modelo arquitectónico:

```text
Use Archify to create an initial interactive architecture diagram.

System:
Flutter Mobile App
    -> Keycloak Authentication
    -> FastAPI REST API
        -> PostgreSQL
        -> MongoDB
    -> Leaflet / Maps Service

Development environment:
    -> Docker
    -> Docker Compose

Source control:
    -> Git
    -> GitHub

Show:
- Mobile client
- Authentication layer
- API layer
- Data layer
- External services
- Development infrastructure
- Main request/data flows
- Trust boundaries

Use an architecture diagram.
Generate it as interactive HTML.
```

---

# 💖 Flujo general de la arquitectura

De manera simplificada, el flujo principal de comunicación entre los componentes puede representarse de la siguiente manera:

```text
                    📱 Flutter Mobile App
                             │
                             ▼
                    🔐 Keycloak
                    Authentication
                             │
                             ▼
                    ⚡ FastAPI REST API
                       /          \
                      /            \
                     ▼              ▼
             🐘 PostgreSQL      🍃 MongoDB
                     
                             │
                             ▼
                    🗺️ Maps Service
```

Mientras que el entorno de desarrollo y administración se complementa con:

```text
              🐳 Docker / Docker Compose
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
       FastAPI       PostgreSQL      MongoDB

                         │
                         ▼
                  🐙 Git / GitHub
```

---

# 🎀 Capas representadas

Para facilitar la comprensión del modelo, la arquitectura puede dividirse en diferentes capas.

### 📱 Capa de cliente

Está representada por la aplicación móvil desarrollada con **Flutter**.

Es la parte con la que interactúa directamente el usuario.

### 🔐 Capa de autenticación

Está representada por **Keycloak**.

Su función dentro del modelo es gestionar los procesos relacionados con la autenticación y el acceso de los usuarios.

### ⚡ Capa de servicios

Está representada por **FastAPI REST API**.

Esta capa recibe las solicitudes realizadas desde el cliente y se encarga de comunicarse con los diferentes recursos del sistema.

### 🗄️ Capa de datos

Está formada principalmente por:

* PostgreSQL
* MongoDB

Estas tecnologías representan las diferentes opciones de almacenamiento consideradas para el proyecto.

### 🌐 Capa de servicios externos

En esta parte se encuentra el servicio relacionado con:

* Leaflet
* Maps Service

Estos componentes permiten contemplar las funcionalidades relacionadas con mapas.

### 🐳 Infraestructura

Está representada por:

* Docker
* Docker Compose

Estos elementos permiten organizar el entorno donde se ejecutan los diferentes servicios.

---

# 🌷 Flujo de información

Uno de los objetivos del diagrama es representar los principales flujos de información existentes entre los componentes.

De forma general, el flujo comienza desde la aplicación móvil.

```text
Usuario
   ↓
📱 Aplicación Flutter
   ↓
🔐 Autenticación
   ↓
⚡ API REST
   ↓
🗄️ Bases de datos
```

Dependiendo de la funcionalidad solicitada, la API puede comunicarse con PostgreSQL, MongoDB o con los servicios relacionados con mapas.

La aplicación móvil no necesita comunicarse directamente con las bases de datos, ya que las solicitudes pasan primero por la API.

---

# 💕 Límites de confianza

Dentro del modelo también se consideran los **Trust Boundaries**, utilizados para representar los límites entre diferentes zonas o componentes del sistema.

Estos límites ayudan a identificar dónde existe una separación entre diferentes servicios y dónde pueden requerirse mecanismos de seguridad o autenticación.

Por ejemplo, la comunicación entre la aplicación móvil y los servicios del backend requiere considerar mecanismos de autenticación y autorización.

---

# 🌸 Resultado de la práctica

Como resultado de esta práctica se obtuvo un **primer boceto de arquitectura del Proyecto Integrador**, representado mediante un diagrama interactivo.

El modelo permite visualizar:

* 💗 Los componentes principales del sistema.
* 💗 La aplicación móvil.
* 💗 La capa de autenticación.
* 💗 La API REST.
* 💗 Las bases de datos.
* 💗 Los servicios externos.
* 💗 La infraestructura de desarrollo.
* 💗 Los principales flujos de información.
* 💗 Los límites de confianza.

Además, el diagrama fue generado en formato HTML y publicado mediante **GitHub Pages**, permitiendo consultar el resultado de forma interactiva.

---

# 🎀 Evidencias de la práctica

Las evidencias generadas durante esta práctica incluyen:

| 🌸 Evidencia                | 💗 Descripción                               |
| --------------------------- | -------------------------------------------- |
| 📐 Diagrama de arquitectura | Modelo interactivo generado con Archify.     |
| 🖼️ Captura                 | Evidencia visual del modelo generado.        |
| 📄 PDF                      | Documento con las evidencias de la práctica. |
| 💻 Commits                  | Registro de los cambios realizados.          |
| 🌐 GitHub Pages             | Publicación del modelo interactivo.          |
| 🔀 Fusión                   | Integración de `Practica02` con `main`.      |

---

# 🌷 Conclusión

La realización de esta práctica permitió obtener una primera representación de la arquitectura que se plantea para el Proyecto Integrador.

El uso de **Archify** facilitó la creación de un modelo visual en el que se pueden identificar los principales componentes del sistema y la relación existente entre ellos.

También se tuvo la oportunidad de utilizar **Codex** como herramienta de apoyo para generar el modelo a partir de una descripción de la arquitectura.

La publicación mediante **GitHub Pages** permitió disponer de una versión interactiva del diagrama, mientras que el uso de **Git y GitHub** ayudó a mantener un registro de los cambios realizados durante el desarrollo de la práctica.

Este primer boceto servirá como referencia para continuar con las siguientes etapas del Proyecto Integrador y para tener una idea más clara de cómo estarán organizados sus diferentes componentes.

---

## 💗 Estado de la práctica

<p align="center">

🌸 **Práctica 02 — FINALIZADA ✅** 🌸

<br><br>

💗 Archify   •   Codex   •   Git   •   GitHub 💗

</p>

---

<p align="center">
  🌷━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━🌷
  <br>
  💕 <strong>Práctica 02 — Integradora</strong> 💕
  <br>
  <em>Boceto de Arquitectura del Proyecto Integrador</em>
  <br>
  🌷━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━🌷
</p>
