# Prompt para el agente de Archify · Práctica 06

Pega todo lo siguiente en el agente de Archify y adjunta `secuencia-pantallas.workflow.json` como especificación base.

---

Eres un diseñador de experiencia de usuario y un ingeniero de diagramas. Genera con Archify un **diagrama interactivo de tipo workflow** (schema v2, idioma `es`, calidad `standard`) titulado **«Netflix · Secuencia de pantallas móviles»**, con el subtítulo **«Usuario / suscriptor (17 pantallas, con acceso) y Administrador académico (9) · 26 pantallas · Jennifer Bautista Barrios · Matrícula 230317»**. Salida: `PRACTICA_06/secuencia-pantallas.html`.

## Contexto
Práctica 06 (individual): diagrama de secuencia de pantallas, orientado a una app móvil, de la plataforma elegida para el modelo CANVAS (Netflix). Exige al menos 2 roles y al menos 15 pantallas compartidas y específicas. Propietaria: **Jennifer Bautista Barrios**, matrícula **230317**; debe verse en el título o subtítulo.

## Roles
- **Usuario / suscriptor:** 17 pantallas, incluido el acceso (S01–S17).
- **Administrador académico:** 9 pantallas propias (S18–S26). Entra por el mismo acceso (S01–S04). Es un módulo **conceptual y académico** para modelar permisos, derechos y publicación; no lo presentes como parte de la app pública de Netflix.

## Carriles (lanes)
1. `shared` · Acceso compartido (tipo `frontend`, leyenda «Acceso compartido»): S01–S04
2. `subscriber` · Usuario / suscriptor (tipo `backend`): S05–S17
3. `admin` · Administrador académico (tipo `security`): S18–S26
4. `decisions` · Decisiones y errores (variante `exception`, tipo `external`, leyenda «Verificaciones y estados»)

## Pantallas (nodos)
| ID | Pantalla | Rol | Propósito | Origen → destino |
|---|---|---|---|---|
| S01 | Bienvenida | Acceso | Presenta el servicio y lleva al acceso. | S13 / S18 → S02 |
| S02 | Inicio de sesión | Acceso | Captura las credenciales de la cuenta. | E1 / S01 → S03 |
| S03 | Verificación | Acceso | Valida credenciales y límite de dispositivos. | S02 → S04 / E1 (credenciales incorrectas) |
| S04 | Perfil o rol | Acceso | Dirige según el permiso: perfil de usuario o administración académica. | E2 / S03 / S13 → S05 / S18 / E2 (sin permiso de administrador) |
| S05 | Inicio | Usuario / suscriptor | Destacados, continuar viendo y tendencias. | E3 / S04 → S06 / S07 / S08 / S10 / S11 / S12 / S13 |
| S06 | Novedades | Usuario / suscriptor | Próximos estrenos y lo más visto. | S05 → S08 |
| S07 | Búsqueda | Usuario / suscriptor | Busca por título, género o persona. | S05 → S08 |
| S08 | Detalle | Usuario / suscriptor | Sinopsis, datos y acciones del título. | E4 / S05 / S06 / S07 / S10 / S11 → S10 / S09 / S11 / S12 / E3 (perfil con restricción) |
| S09 | Episodios | Usuario / suscriptor | Elige temporada y episodio. | S08 → S10 |
| S10 | Reproductor | Usuario / suscriptor | Reproducción con progreso, audio y subtítulos. | S05 / S08 / S09 / S12 → S08 / E4 (demasiadas pantallas activas) |
| S11 | Mi lista | Usuario / suscriptor | Títulos guardados por el perfil. | S05 / S08 → S08 |
| S12 | Descargas | Usuario / suscriptor | Contenido disponible sin conexión. | S05 / S08 → S10 |
| S13 | Mi perfil | Usuario / suscriptor | Puerta hacia cuenta, perfiles, ajustes y ayuda. | S05 / S14 / S15 / S16 / S17 → S14 / S16 / S17 / S04 / S01 |
| S14 | Cuenta y suscripción | Usuario / suscriptor | Consulta plan, próximo cobro y método de pago. | S13 → S15 / S13 |
| S15 | Perfiles y control | Usuario / suscriptor | Administra perfiles, clasificación y PIN. | S14 → S13 |
| S16 | Configuración | Usuario / suscriptor | Reproducción, subtítulos, audio y descargas. | S13 → S13 |
| S17 | Ayuda y soporte | Usuario / suscriptor | Busca respuestas o contacta a soporte. | S13 → S13 |
| S18 | Panel | Administrador académico | Resumen conceptual de catálogo y tareas pendientes. | S04 / S26 → S19 / S26 / S01 |
| S19 | Catálogo | Administrador académico | Lista de títulos con estado y acciones. | E7 / S18 / S21 → S20 / S21 |
| S20 | Alta de título | Administrador académico | Registra un título nuevo y valida los campos. | E5 / S19 → S22 / S23 / E5 (faltan campos) |
| S21 | Edición | Administrador académico | Edita metadatos y visibilidad de un título. | S19 → S23 / S22 / S19 |
| S22 | Episodios | Administrador académico | Carga temporadas y episodios de una serie. | S20 / S21 → S23 |
| S23 | Derechos y regiones | Administrador académico | Define regiones, vigencia y descargas permitidas. | E6 / S20 / S21 / S22 → S24 / E6 (conflicto de licencia) |
| S24 | Categorías | Administrador académico | Asigna géneros, filas y destacados. | S23 → S25 |
| S25 | Publicación | Administrador académico | Publica, programa o guarda como borrador. | S24 → S26 / E7 (guardar como borrador) |
| S26 | Historial | Administrador académico | Bitácora de quién cambió qué y cuándo. | S18 / S25 → S18 |

## Estados (nodos del carril decisions)
| ID | Estado | Se activa desde | Regresa a |
|---|---|---|---|
| E1 | Acceso incorrecto | S03 | S02 (corregir datos) |
| E2 | Rol sin autorización | S04 | S04 (elegir otro perfil) |
| E3 | Contenido restringido | S08 | S05 (elegir otro título) |
| E4 | Límite de pantallas | S10 | S08 (volver al detalle) |
| E5 | Formulario incompleto | S20 | S20 (completar campos) |
| E6 | Conflicto de licencia | S23 | S23 (ajustar regiones) |
| E7 | Borrador guardado | S25 | S19 (retomar desde catálogo) |

## Reglas de las flechas
- Cada flecha lleva **una etiqueta con la acción del usuario** (verbo + objeto), no el nombre de la pantalla.
- Flujo principal: `role: main` y `variant: emphasis` (en el carril administrador, `security`). Alternativas: `branch`. Volver o corregir: `return`. Errores y permisos: `error`.
- Bifurcaciones obligatorias: credenciales válidas o incorrectas (S03), usuario o administrador o sin permiso (S04), película o serie (S08 y S20), alta con campos completos o incompletos (S20), conflicto de licencia (S23), publicar o guardar borrador (S25).
- Ninguna pantalla sin entrada ni salida; no dejes nodos huérfanos.
- Evita cruces largos: acomoda las columnas por orden de aparición del flujo y mantén cada rol en su carril.

## Vistas guiadas
`usuario` (S01–S17, E1, E3, E4), `admin` (S04, S18–S26, E2, E5, E6, E7), `acceso` (S01–S04, S18, E1, E2) y `errores` (E1–E7), cada una con una nota de una línea.

## Tarjetas informativas (cards)
Dos roles, un acceso común · Recorrido del usuario · Administración académica (aclara que es propuesta académica) · Pantallas dibujadas (enlaza `sketches-moviles.html`, autoría y que los sketches son ilustrativos).

## Estilo visual
- Paleta inspirada en Netflix, colorida pero legible: negro #141414, rojo #E50914 y un acento por rol (azul claro para acceso, verde para usuario, ámbar para administrador).
- Prefiere el estilo visual más expresivo del visor y verifica el contraste en tema claro y oscuro.

## Calidad y entrega
- Textos en español; etiquetas de nodo cortas (`S05 · Inicio`).
- Leyenda visible y vistas guiadas funcionando.
- Ejecuta las compuertas del agente (validate, deliver, check y browser-check) y corrige hasta que pasen.
- No inventes cifras, precios ni capturas oficiales de Netflix.
