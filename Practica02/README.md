# 🌸 Práctica 02 — Boceto de Arquitectura del Proyecto Integrador

<p align="center">
  💗✨ <strong>Materia: Integradora</strong> ✨💗
</p>

<p align="center">
  <em>Primer boceto interactivo de la arquitectura del Proyecto Integrador</em>
</p>

---

## 🎀 Descripción

En esta práctica se realizó un **primer boceto de la arquitectura del Proyecto Integrador**, utilizando **Archify** como herramienta de modelado arquitectónico y **Codex** como apoyo para la generación del modelo.

El objetivo principal fue representar de manera visual e interactiva los diferentes componentes del sistema, sus relaciones y los principales flujos de información.

🌷 **Herramientas utilizadas:**

* 💻 Archify
* 🤖 Codex
* 🐙 Git
* 🌐 GitHub
* 🐳 Docker
* 📱 Flutter
* ⚡ FastAPI
* 🗄️ PostgreSQL
* 🍃 MongoDB

---

## 💗 Diagrama de Arquitectura

El resultado de la práctica se encuentra disponible como un **diagrama interactivo en HTML**.

<p align="center">

### 🌸 [✨ Ver Diagrama de Arquitectura Interactivo ✨](https://diegomiguel04.github.io/Practicas-INTEGRADORA/Practica02/index.html)

</p>

---

## 🎀 Evidencia

A continuación se muestra una captura del modelo arquitectónico generado durante la práctica:

<p align="center">
  <img src="mobile-system-architecture.visual-check.1440x900.dark.png" alt="Diagrama de arquitectura del sistema" width="900">
</p>

---

## 🌷 Actividades realizadas

Durante el desarrollo de la práctica se realizaron las siguientes actividades:

* 💻 Verificación de la instalación de **NPM**.
* 🤖 Instalación de **Codex CLI**.
* 🌸 Instalación de **Archify**.
* 🔗 Vinculación de la cuenta de **Codex con ChatGPT**.
* ✍️ Ingreso del prompt para generar el modelo arquitectónico.
* 🏗️ Generación del diagrama de arquitectura interactivo en **HTML**.
* 📂 Carga de los documentos generados en la rama `Practica02`.
* 📝 Realización de commits utilizando buenas prácticas.
* ☁️ Publicación de los cambios en el repositorio remoto.
* 🌐 Habilitación de **GitHub Pages** para consultar el modelo interactivo.
* 📄 Elaboración del documento de evidencias en PDF.
* 📚 Actualización de la tabla de prácticas con la **Práctica 02**.
* 🔀 Fusión de la rama `Practica02` con `main`.

---

## 💕 Arquitectura propuesta

El modelo representa una aplicación móvil desarrollada con **Flutter**, conectada con diferentes servicios encargados de la autenticación, procesamiento de información, almacenamiento de datos y servicios externos.

### 🌸 Componentes principales

| Componente                     | Descripción                                                      |
| ------------------------------ | ---------------------------------------------------------------- |
| 📱 **Flutter Mobile App**      | Aplicación móvil utilizada como cliente del sistema.             |
| 🔐 **Keycloak**                | Servicio utilizado para la autenticación.                        |
| ⚡ **FastAPI REST API**         | Capa encargada de proporcionar los servicios de la API.          |
| 🐘 **PostgreSQL**              | Base de datos utilizada para almacenar información estructurada. |
| 🍃 **MongoDB**                 | Base de datos orientada a documentos.                            |
| 🗺️ **Leaflet / Maps Service** | Servicio utilizado para funcionalidades relacionadas con mapas.  |
| 🐳 **Docker**                  | Herramienta utilizada para la contenerización de los servicios.  |
| 🐳 **Docker Compose**          | Utilizado para administrar los diferentes contenedores.          |
| 🐙 **Git / GitHub**            | Control de versiones y almacenamiento del código.                |

---

## 🎀 Prompt utilizado

El siguiente prompt fue utilizado para generar el modelo arquitectónico mediante **Archify**:

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

## 🌸 Flujo general del sistema

La arquitectura propuesta sigue un flujo general donde la aplicación móvil funciona como cliente principal.

```text
📱 Flutter Mobile App
          │
          ▼
🔐 Keycloak Authentication
          │
          ▼
⚡ FastAPI REST API
       │       │
       ▼       ▼
 🐘 PostgreSQL  🍃 MongoDB
          │
          ▼
🗺️ Leaflet / Maps Service
```

La infraestructura de desarrollo se complementa con **Docker y Docker Compose**, mientras que **Git y GitHub** permiten administrar y almacenar el código del proyecto.

---

## 💖 Resultado

Como resultado de esta práctica se obtuvo un **modelo arquitectónico interactivo en HTML**, acompañado de su evidencia visual y documentación correspondiente.

El modelo permite visualizar los principales componentes del sistema, sus conexiones, flujos de información y límites de confianza.

---

## 🌷 Evidencias de la práctica

* 💗 Diagrama arquitectónico interactivo.
* 💗 Captura del modelo generado.
* 💗 Documento de evidencias en PDF.
* 💗 Commits realizados durante el desarrollo.
* 💗 Publicación mediante GitHub Pages.

---

<p align="center">
  🌸━━━━━━━━━━━━━━━━━━━━🌸
  <br>
  💗 <strong>Práctica 02 — Integradora</strong> 💗
  <br>
  <em>Diseñando la arquitectura del Proyecto Integrador paso a paso</em>
  <br>
  🌸━━━━━━━━━━━━━━━━━━━━🌸
</p>
