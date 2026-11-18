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
  vectoriales en Inkscape, índice de figuras, y flujo de verificación
  matemática con Opus, todo validado con el **Capítulo III — Principio de
  Huygens** como capítulo piloto completo.
- ✅ **Etapa 2 (traducción capítulo por capítulo) — completa.** Los 8
  capítulos del Volumen I, más las Conclusiones finales del libro, están
  traducidos y verificados ecuación por ecuación:
  - Capítulo I — Estudio de los pequeños movimientos en un medio elástico.
  - Capítulo II — Propagación de una onda plana. Interferencias.
  - Capítulo III — Principio de Huygens (piloto).
  - Capítulo IV — Difracción (el más extenso del volumen).
  - Capítulo V — Polarización rotatoria. Dispersión.
  - Capítulo VI — Doble refracción (el capítulo más extenso del volumen,
    con las subteorías de Fresnel, Cauchy, Neumann, Sarrau y Boussinesq,
    más la superficie de onda y los medios hemiedros).
  - Capítulo VII — Reflexión (vítrea, cristalina y metálica; tres
    enunciados distintos del Teorema de Mac-Cullagh).
  - Capítulo VIII — Aberración astronómica (coeficiente de arrastre de
    Fresnel).
  - Conclusiones (unidad propia, sin número de capítulo, como en el
    original).
- ⏳ **Etapa 3 (en curso)** — integración y maquetación final del Volumen I:
  - ✅ Frente de materia: prólogo del traductor, prefacio e introducción
    originales de Poincaré, numeración de capítulos unificada en números
    romanos en toda la portadilla y el índice.
  - ✅ Revisión global de consistencia entre los 8 capítulos (terminología,
    estilo de cajas y notas, referencias cruzadas) — encontró dos párrafos
    que habían quedado sin traducir y los tradujo, corrigió una figura mal
    dibujada, y confirmó tres referencias cruzadas que ya vienen erróneas
    en el propio original de 1889.
  - ✅ Las notas al pie distinguen con "(N. del T.)" las que son nuestras
    de las que son del propio Poincaré.
  - ⬜ Revisión tipográfica final de lectura corrida.
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
