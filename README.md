# Teoría Matemática de la Luz — Henri Poincaré

Traducción al español latino, edición y reformato como libro guía de
*Théorie mathématique de la lumière*, las lecciones de física matemática que
Henri Poincaré dictó en la Facultad de Ciencias de París (Cours de la
Faculté des Sciences de Paris), publicadas originalmente en dos volúmenes:

- **Volumen I** (1889) — teoría ondulatoria de la luz: pequeños movimientos
  en un medio elástico, interferencia, principio de Huygens, difracción,
  polarización rotatoria y dispersión, doble refracción, reflexión y
  aberración astronómica.
- **Volumen II** (1892) — nuevos estudios sobre difracción y la teoría de la
  dispersión de Helmholtz.

Ambas obras son de dominio público. Las fuentes originales en francés
(digitalizadas por Google Books a partir de ejemplares de las bibliotecas de
la Universidad de Michigan y del Observatorio de Harvard) se conservan en
[`fuentes-originales/`](fuentes-originales/) como referencia de la
traducción.

## Qué es este proyecto

No es solo una traducción literal: es una edición pensada para leerse como
libro guía de física matemática en español, manteniendo el rigor y la
notación del original pero:

- desarrollando explícitamente, paso a paso, los cálculos que Poincaré y sus
  redactores dan por evidentes, con el nivel de detalle que necesita un
  estudiante de pregrado;
- rehaciendo todas las figuras del libro como ilustraciones vectoriales
  (Inkscape → PDF), con una paleta de color propia (azul y rojo) consistente
  en todo el libro;
- conservando el espíritu de las portadillas tipográficas originales de cada
  capítulo, adaptadas al español.

## Estado del proyecto

🚧 En progreso — Volumen I. El Volumen II no se inicia hasta terminar el
Volumen I. El plan de trabajo completo, capítulo por capítulo, está en
[`ROADMAP.md`](ROADMAP.md).

**Avance actual:**

- ✅ **Etapa 0-1 (infraestructura y piloto)** — plantilla LaTeX, paleta
  azul/rojo, portadillas de capítulo y de volumen al estilo del original,
  cajas de "enunciado importante" (solo para principios y resultados
  centrales, nunca para demostraciones) y "nota histórica", figuras
  vectoriales en Inkscape, y flujo de verificación matemática con Opus,
  todo validado con el **Capítulo III — Principio de Huygens** como
  capítulo piloto completo.
- ⏳ **Etapa 2 (traducción capítulo por capítulo)** — en curso:
  - ✅ Capítulo I — Estudio de los pequeños movimientos en un medio
    elástico (traducido y verificado ecuación por ecuación).
  - ✅ Capítulo II — Propagación de una onda plana. Interferencias.
  - ✅ Capítulo III — Principio de Huygens (piloto).
  - ✅ Capítulo IV — Difracción (el más extenso del volumen).
  - ✅ Capítulo V — Polarización rotatoria. Dispersión.
  - ⬜ Capítulo VI — Doble refracción (siguiente paso; es el segundo
    capítulo más extenso, con las subteorías de Fresnel, Cauchy,
    Neumann, Sarrau y Boussinesq, más la superficie de onda).
  - ⬜ Capítulos VII, VIII — pendientes.
- ⬜ **Etapa 3** — integración y maquetación final del Volumen I.
- ⬜ **Etapa 4** — publicación del Volumen I.
- ⬜ **Volumen II** — sin iniciar; plan de alto nivel en
  [`volumen-2/PLAN.md`](volumen-2/PLAN.md).

## Estructura del repositorio

```
fuentes-originales/   Escaneos originales en francés (dominio público)
volumen-1/            Fuente LaTeX, figuras y capítulos del Volumen I
volumen-2/            Plan de trabajo del Volumen II (aún sin iniciar)
recursos/             Glosario de terminología francés–español
ROADMAP.md            Plan de trabajo detallado por etapas
```

## Licencia

El texto original de Henri Poincaré es de dominio público. Esta traducción y
edición se publica para fines educativos y de divulgación.
