# Plan — Volumen II

Reglas generales, asignación de modelos y convenciones de estilo en
[`../ROADMAP.md`](../ROADMAP.md) y en `CLAUDE.md` (local, no versionado) —
se aplican sin cambios a este volumen.

## Fuente

*Théorie mathématique de la lumière II — Nouvelles études sur la
Diffraction. Théorie de la dispersion de Helmholtz.* Lecciones del primer
semestre 1891-1892, redactadas por M. Lamotte y D. Hurmuzescu.
`../fuentes-originales/TheorieMathematiqueDeLaLumiere_2.pdf`.

- 318 páginas de PDF en total. El texto principal termina en la página
  impresa 306 ("FIN"); le siguen la tabla de materias (impresas 307-310,
  sin numerar en la portada de esa sección) y contraportada/guardas.
- Frente de materia original: portada, e "Introduction" (sin "Préface"
  separada como en el Volumen I) — Poincaré explica ahí que estas lecciones
  completan las del primer volumen, con los temas que el tiempo no le
  permitió tratar antes (Helmholtz, Kirchhoff, Maxwell/Hertz), y agradece a
  Lamotte y Hurmuzescu por redactarlas.

### ⚠️ Correspondencia de páginas: NO es constante, a diferencia del Volumen I

En el Volumen I, página de PDF = página impresa + 16 en todo el libro. En
este volumen **eso no se cumple de principio a fin**:
- Confirmado: PDF 17 = impresa 1 (inicio del Capítulo I) → offset +16 ahí.
- Confirmado: PDF ~305-308 = impresas ~305-308 (cerca del final, tabla de
  materias) → offset ~0 ahí.

El offset se reduce en algún punto intermedio del escaneo (probablemente
páginas insertadas o duplicadas por Google Books). **Cada capítulo debe
confirmar por su cuenta, leyendo el PDF directamente, dónde empieza y
termina su tramo** — no asumir ningún offset fijo para todo el volumen.
Las páginas de PDF que se dan más abajo junto a cada capítulo son solo una
estimación de partida (calculada con el offset +16 confirmado al inicio);
verificarlas y corregirlas al empezar cada capítulo.

## Capítulos (confirmados contra la tabla de materias original)

Páginas impresas y tamaño aproximado de cada capítulo:

0. **Frente de materia** — Portada, Introducción (sin Prefacio separado).
1. ✅ **Teoría elástica de la luz** — impresas 1-18 (≈18 pp., offset +16
   confirmado en todo el capítulo). Movimiento del éter, fuerza viva,
   energía potencial, ecuaciones del movimiento, ondas planas, intensidad
   luminosa. Traducido, verificado ecuación por ecuación (un error de
   traducción corregido, siete erratas del propio original de 1892
   documentadas con nota), 3 figuras. Sin caja `enunciado` — es un
   recapitulado sin principio nuevo con nombre propio.
2. **Teoría electromagnética de la luz. Comparación con la teoría
   elástica** — impresas 19-33 (≈15 pp.). Ecuaciones de Maxwell, ecuaciones
   de Hertz, comparación, propagación de ondas planas.
3. **Integración de las ecuaciones: caso particular de las ondas planas**
   — impresas 34-47 (≈14 pp.). Ondas evanescentes, intensidad.
4. **Estudio de las interferencias** — impresas 48-64 (≈17 pp.). Teoría
   elástica y electromagnética de las interferencias.
5. **Teoría de la reflexión. Reflexión vítrea** — impresas 65-96 (≈32 pp.).
   Teoría de Maxwell, reflexión total, experiencias de Wiener, anillos de
   colores, reflexión metálica, oscilaciones hertzianas.
6. **Propagación rectilínea de la luz** — impresas 97-122 (≈26 pp.). Ondas
   esféricas, haces muy delgados, luz no paralela.
7. **Principio de Huygens** — impresas 123-183 (≈61 pp., **el más extenso
   del volumen** — dividir en 2-3 partes secuenciales). Ecuación
   fundamental, aplicación a ondas reflejadas/refractadas, líneas focales
   y focos, ondas esféricas/cilíndricas/de forma cualquiera.
8. **Problema general de la difracción. Hipótesis de Kirchhoff** —
   impresas 184-198 (≈15 pp.). Experiencias de Gouy, integrales de Fresnel.
9. **Difracción de las ondas convergentes** — impresas 199-228 (≈30 pp.).
   Ondas cilíndricas/esféricas, polarización por difracción.
10. **Teoría de la dispersión de Helmholtz** — impresas 229-256 (≈28 pp.).
    Hipótesis de Helmholtz, explicación de la existencia de las rayas
    espectrales, relación absorción/emisión, teoría electromagnética.
11. **Dispersión y absorción de la luz por los medios anisótropos** —
    impresas 257-274 (≈18 pp.). Leyes de M. Becquerel (tres leyes).
12. **Polarización rotatoria. Teoría de M. Mallard** — impresas 275-306
    (≈32 pp.). Pilas de Reusch, hipótesis de M. Quesneville, superficie de
    onda en una pila de láminas.

Total: ≈306 páginas impresas, comparable en extensión al Volumen I.

## Al empezar cada capítulo

Mismo pipeline que el Volumen I (ver `ROADMAP.md`, Etapa 2, y `CLAUDE.md`):

1. Confirmar el rango real de páginas de PDF del capítulo (ver advertencia
   de offset arriba) y leer el original.
2. Traducción fiel, con `\tag{N}` para la numeración de ecuaciones de
   Poincaré (reinicios documentados con nota al pie, nunca inventados).
3. Extender en prosa, sin caja ni pasos numerados, los cálculos que el
   original da por evidentes.
4. Notas al pie del traductor con `~(N.~del T.)`; las de Poincaré, sin
   marcar.
5. Figuras vectorizadas en Inkscape, paleta azul (`#14315D`) / rojo
   (`#9E1B32`), mismo estilo que el Volumen I.
6. Cajas `enunciado` solo para hipótesis fundamentales y resultados
   culminantes con nombre propio (ya hay precedentes claros: Capítulo VII
   es el "Principio de Huygens" de este volumen, con tratamiento mucho más
   extenso que el Capítulo III del Volumen I — probablemente amerite su
   propia caja de enunciado, distinguida si hace falta).
7. Verificación matemática del 100% del capítulo con un subagente Opus,
   igual que en el Volumen I.
8. Capítulos grandes (Cap. VII, posiblemente IX/X/XII) se dividen en 2-3
   forks secuenciales, nunca paralelos — ver la lección ya documentada en
   `CLAUDE.md`.

**Orden sugerido**: secuencial, I → XII, salvo que se decida lo contrario.
No hay necesidad de un "capítulo piloto" nuevo — el estilo y el flujo ya
están validados en el Volumen I; se reutilizan sin cambios.

## Infraestructura ya creada

- `volumen-2/main.tex` — reutiliza `../volumen-1/preambulo/estilo.tex`
  (misma paleta, mismas cajas, mismo índice de figuras).
- `volumen-2/00-frontmateria/` — para portada e introducción (pendientes
  de traducir).
- `volumen-2/0N-nombre-capitulo/` — una carpeta por cada uno de los 12
  capítulos, vacías, listas para su `capitulo.tex`.
- `volumen-2/figuras/svg/` y `volumen-2/figuras/pdf/` — figuras del
  volumen, numeradas `capNN-figM` para evitar colisión con las del
  Volumen I.
- `recursos/GLOSARIO.md` — compartido con el Volumen I; se amplía, no se
  duplica.

Este archivo se actualiza (marcando ✅ cada capítulo) a medida que avanza
la traducción, igual que se hizo con `ROADMAP.md` para el Volumen I.
