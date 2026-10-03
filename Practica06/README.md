# 🎬 Práctica 06 – Diagrama de Secuencia de Pantallas (Sketches) de Netflix

**Persona / Autor:** Jennifer Bautista Barrios · **Modalidad:** Individual

## 📖 Descripción

En esta práctica se realizó un **diagrama interactivo de secuencia de pantallas** de la aplicación móvil de **Netflix**, utilizando sketches de baja fidelidad para representar el flujo de navegación.

El diagrama cuenta con **2 roles principales**: espectador y titular de la cuenta, además de **16 pantallas principales** y **3 estados alternos**.

Cada pantalla puede seleccionarse para abrir un panel con información sobre su propósito, elementos principales y la acción que permite continuar con el flujo.

### 🌐 Ver el proyecto

**[Ver el diagrama en GitHub Pages]()**

<p align="center">
  <img src="netflix-secuencia-pantallas.preview.dark.png" alt="Vista previa del diagrama" width="90%">
</p>

<p align="center">
  <img src="netflix-logo.svg" alt="Netflix" height="40">
</p>

---

## 🎯 Objetivo

Representar de forma visual y ordenada el flujo de navegación de una aplicación móvil, identificando las pantallas, acciones del usuario, roles y diferentes situaciones que pueden presentarse durante el uso de la aplicación.

---

## 👥 Roles y pantallas

### 🔴 Compartidas – 4 pantallas

1. Bienvenida
2. Inicio de sesión
3. Elegir perfil
4. Notificaciones

### 🎬 Espectador – 6 pantallas

5. Inicio
6. Buscar
7. Detalle del título
8. Reproductor
9. Descargas
10. Mi lista

### 👤 Titular de la cuenta – 6 pantallas

5. Cuenta
6. Membresía y plan
7. Pagos y facturación
8. Administrar perfiles
9. Dispositivos
10. Actividad de visualización

### ⚠️ Estados alternos

* Sin conexión
* Búsqueda sin resultados
* Contenido no disponible

Las **flechas numeradas** indican la acción que permite pasar de una pantalla a otra. También se incluye una conexión entre los roles para representar cómo la actividad de los perfiles puede reflejarse en la **Actividad de visualización** del titular.

---

## 🖱️ Interactividad

El diagrama incluye diferentes elementos interactivos:

* Panel de información por pantalla.
* Selección de rol.
* Desplazamiento entre carriles.
* Tema claro y oscuro.
* Botón para restablecer.
* Flechas con acciones de navegación.
* Diseño responsive.

También se consideraron aspectos de accesibilidad como **navegación mediante teclado, foco visible, `aria-live` y `prefers-reduced-motion`**.

---

## 🛠️ Herramientas utilizadas

* **Archify** – Generación del diagrama.
* **HTML, CSS y JavaScript** – Estructura e interactividad.
* **SVG** – Logotipo utilizado en la práctica.
* **GitHub** – Control y almacenamiento del proyecto.
* **GitHub Pages** – Publicación del diagrama.

---

## 🤖 Prompt usado con Archify

```text
Usa Archify para generar el Diagrama de Secuencia de Pantallas (Sketches) de la aplicación móvil de Netflix, con 2 roles: espectador y titular de la cuenta, y al menos 15 pantallas entre compartidas y específicas.

- Carril "Compartidas": bienvenida, inicio de sesión, elegir perfil, notificaciones.
- Carril "Espectador": inicio, buscar, detalle del título, reproductor, descargas, Mi lista.
- Carril "Titular de la cuenta": cuenta, membresía y plan, pagos y facturación, administrar perfiles, dispositivos, actividad de visualización.
- Flechas numeradas con la acción que dispara cada cambio.
- Estados alternos: sin conexión, búsqueda sin resultados y contenido no disponible.
- Panel de detalle por pantalla, selección de rol, tema claro/oscuro y restablecer.
- Paleta de Netflix (#E50914, #141414), accesible y responsive.
Salida: un HTML autocontenido para GitHub Pages.
```

---

## ✅ Revisión del resultado

| Requisito                   | Resultado |
| --------------------------- | --------- |
| 2 roles                     | ✅         |
| 15+ pantallas               | ✅ 16      |
| Estados alternos            | ✅ 3       |
| Flechas numeradas           | ✅         |
| Interactividad              | ✅         |
| Tema claro/oscuro           | ✅         |
| Diseño responsive           | ✅         |
| Accesibilidad               | ✅         |
| Publicación en GitHub Pages | ✅         |

---

## 📚 Aprendizaje

Esta práctica permitió comprender mejor cómo organizar el **flujo de navegación de una aplicación**, identificando las acciones que realiza el usuario y la relación entre las diferentes pantallas.

También permitió trabajar con roles, estados alternos y elementos interactivos, además de conocer la importancia de realizar sketches antes de desarrollar una interfaz completa.

---

## 🎓 Conclusión

El resultado final representa de manera visual e interactiva la secuencia de pantallas de una aplicación similar a Netflix. La separación por roles facilita comprender las funciones disponibles para cada usuario y las flechas permiten identificar claramente el flujo de navegación.

La práctica también permitió reforzar conocimientos sobre **diseño de interfaces, navegación, accesibilidad y representación de sistemas mediante diagramas**.

---

## ⚠️ Nota académica

Ejercicio académico, no afiliado a Netflix. La marca y el logotipo pertenecen a Netflix, Inc. y se utilizan únicamente con fines educativos.

Los archivos `netflix-logo.svg` y `netflix-icon.svg` son recreaciones vectoriales realizadas para esta práctica. Los bocetos, nombres y datos utilizados son ejemplos propios con fines académicos.

---

## 👩‍💻 Persona / Autor

**Jennifer Bautista Barrios**
