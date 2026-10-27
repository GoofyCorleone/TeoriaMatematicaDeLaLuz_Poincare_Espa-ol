# Hoja de ruta — Teoría Matemática de la Luz (H. Poincaré)

Traducción al español latino, edición y reformato como libro guía de los dos
volúmenes de *Théorie mathématique de la lumière* de Henri Poincaré (Cours de
la Faculté des Sciences de Paris).

## Fuentes originales

- **Volumen I** — *Théorie mathématique de la lumière* (1889). Redactado por
  J. Blondin a partir de las lecciones de Poincaré (1er semestre 1887-1888).
  429 páginas. 8 capítulos + introducción + conclusiones.
  `fuentes-originales/TheorieMathematiqueDeLaLumiere.pdf`
- **Volumen II** — *Théorie mathématique de la lumière II — Nouvelles études
  sur la Diffraction. Théorie de la dispersion de Helmholtz* (1892).
  Redactado por M. Lamotte y D. Hurmuzescu. 318 páginas.
  `fuentes-originales/TheorieMathematiqueDeLaLumiere_2.pdf`

Ambas obras son de dominio público (Poincaré falleció en 1912).

## Decisiones de arquitectura

- **Producción**: LaTeX (clase `book`), compilado con `latexmk`/`pdflatex`.
- **Figuras**: cada figura original se rehace en Inkscape como SVG editable
  y se exporta a PDF vectorial para incluirse con `\includegraphics`.
  Ninguna figura se escanea ni se usa como imagen rasterizada.
- **Paleta**: azul profundo + rojo, consistentes en portadillas, cajas de
  cálculo y acentos tipográficos. Tonos exactos se fijan en la Etapa 1
  (capítulo piloto) y quedan documentados en `volumen-1/preambulo/estilo.tex`.
- **Estilo "libro guía"**: cajas diferenciadas para "Cálculo detallado paso a
  paso", "Nota histórica" y "Definición"; portadillas de capítulo que imitan
  la composición tipográfica de las portadas textuales originales (no la
  pasta física), traducidas.
- **Fidelidad**: la traducción sigue el texto y el orden de Poincaré; donde
  el original salta pasos algebraicos ("on obtient immédiatement", "il
  vient", "on démontre"), se añade una caja de **cálculo detallado** que
  desarrolla cada paso explícitamente, pensada para un estudiante de
  pregrado. El texto original nunca se altera en su contenido matemático,
  solo se expande pedagógicamente.

## Asignación de modelos (Sonnet vs. Opus)

| Tarea | Modelo | Motivo |
|---|---|---|
| Transcripción fiel del francés original | Sonnet | Trabajo mecánico de alta fidelidad |
| Traducción de prosa (narrativa, definiciones, contexto) | Sonnet | Traducción técnica estándar |
| Maquetación LaTeX, plantillas, estilos | Sonnet | Ingeniería de documento |
| Vectorización de figuras en Inkscape | Sonnet | Tarea gráfica/mecánica |
| Desarrollo explícito paso a paso de cálculos largos o no triviales | Opus | Razonamiento matemático profundo y pedagógico |
| **Verificación de absolutamente todos los cálculos de cada capítulo** (triviales y no triviales) | **Opus** | Control de calidad: confirmar signos, sustituciones y consistencia antes de cerrar el capítulo |
| Resolución de pasajes ambiguos (notación arcaica, convenciones de 1889) | Opus | Juicio técnico fino |
| Control de calidad global del volumen (consistencia de notación, referencias cruzadas) | Opus | Revisión holística final |

**Nivel de rigor acordado:** balanceado — Opus desarrolla paso a paso solo
los cálculos largos/no triviales, pero **revisa y verifica el 100% de los
cálculos** de cada capítulo (incluidos los triviales que Sonnet redacta
directamente), antes de dar el capítulo por cerrado.

**Mecanismo:** Sonnet orquesta todo el trabajo de principio a fin. Cuando una
tarea requiere Opus, se delega a un subagente con `model: opus` y un prompt
autocontenido (fragmento francés original, borrador en español, ecuaciones
involucradas, capítulo/sección) — ese subagente no hereda la conversación en
curso, así que cada delegación debe traer todo el contexto necesario.

## Etapas — Volumen I

### Etapa 0 — Preparación y auditoría
- Extracción capítulo por capítulo del texto y las ecuaciones del PDF
  original (OCR asistido, verificado contra el escaneo).
- Inventario de figuras: número, capítulo, página, descripción breve.
- Glosario inicial de terminología física/matemática de 1889
  (`recursos/GLOSARIO.md`), vivo durante todo el proyecto.

### Etapa 1 — Infraestructura del documento y capítulo piloto
- Plantilla LaTeX: clase, preámbulo, paleta de color, cajas de "cálculo
  detallado"/"nota histórica"/"definición", estilo de portadillas de
  capítulo, numeración de ecuaciones y figuras.
- Capítulo piloto completo de punta a punta: **Capítulo III — Principio de
  Huygens** (el más corto y autocontenido, ~18 páginas originales), para
  validar visualmente el estilo antes de comprometerse con los 8 capítulos.
- Aprobación del usuario sobre el estilo visual antes de continuar.

### Etapa 2 — Traducción capítulo por capítulo
Pipeline por capítulo (orden sugerido: I → II → IV → V → VI → VII → VIII,
dejando III ya resuelto como piloto):

1. Transcripción fiel del francés (Sonnet).
2. Traducción de prosa al español latino (Sonnet).
3. Marcado de los saltos de cálculo que requieren desarrollo explícito
   (Sonnet señala, Opus desarrolla paso a paso).
4. Verificación matemática del capítulo completo, cálculo por cálculo
   (Opus).
5. Maquetación LaTeX del capítulo con cajas y referencias cruzadas (Sonnet).
6. Vectorización en Inkscape de las figuras del capítulo (Sonnet).
7. Control de calidad final de lectura (Opus, spot-check de fidelidad y
   claridad pedagógica).

El **Capítulo VI — Doble refracción** es el más extenso (contiene las
subteorías de Fresnel, Cauchy, Neumann, Sarrau, Boussinesq y la superficie de
onda) y se trabaja en sub-bloques siguiendo esa misma subdivisión.

### Etapa 3 — Integración y maquetación final del volumen
- Ensamblaje completo: portada textual, prólogo del traductor (nuevo),
  prefacio original traducido, introducción, los 8 capítulos, conclusiones,
  índice de figuras, glosario final.
- Revisión tipográfica global (Sonnet) y revisión técnica global comparando
  contra el original, capítulo por capítulo (Opus).
- Validación de numeración de ecuaciones, referencias cruzadas y consistencia
  de notación en todo el volumen.

### Etapa 4 — Publicación
- PDF final del Volumen I.
- Commit y push al repositorio bajo la identidad del usuario (ver reglas de
  Git más abajo).

## Capítulos del Volumen I (confirmados contra la tabla de materias original)

0. Prólogo del traductor (nuevo) · Prefacio · Introducción
1. Estudio de los pequeños movimientos en un medio elástico
2. Propagación de los movimientos vibratorios. Interferencia *(título exacto
   a confirmar en la Etapa 0 de extracción)*
3. Principio de Huygens
4. Difracción
5. Polarización rotatoria. Dispersión
6. Doble refracción (Fresnel, Cauchy, Neumann, Sarrau, Boussinesq, superficie
   de onda)
7. Reflexión (vítrea, cristalina, metálica)
8. Aberración astronómica
9. Conclusiones

## Plan — Volumen II (no se inicia hasta terminar el Volumen I)

*Théorie mathématique de la lumière II — Nouvelles études sur la Diffraction.
Théorie de la dispersion de Helmholtz* (1892). Confirmado del original:
Capítulo I = "Teoría elástica de la luz".

Cuando se inicie, el Volumen II sigue exactamente el mismo pipeline de
Etapas 0-4 que el Volumen I:
1. Etapa 0 propia: extracción, inventario de figuras y ampliación del
   glosario compartido (`recursos/GLOSARIO.md` se reutiliza, no se duplica).
2. Reutiliza la plantilla LaTeX y la paleta de color del Volumen I
   (`volumen-1/preambulo/estilo.tex`) para mantener continuidad visual entre
   ambos volúmenes como una sola colección.
3. Traducción capítulo por capítulo con el mismo pipeline Sonnet/Opus.
4. Integración, maquetación final y publicación.

El desglose detallado de capítulos del Volumen II se documentará en
`volumen-2/PLAN.md` en cuanto empiece su Etapa 0.

## Reglas de Git / GitHub

- Autoría de commits y pushes: únicamente el usuario (`GoofyCorleone`). No se
  añade ninguna línea de co-autoría de IA.
- `CLAUDE.md` nunca se versiona ni se sube a GitHub (excluido vía
  `.git/info/exclude`, local únicamente).
- No se usa un `.gitignore` versionado; las reglas de exclusión viven en
  `.git/info/exclude` (local, nunca se publica).
- Los PDF originales en `fuentes-originales/` sí se versionan (dominio
  público, sirven como referencia de la traducción).
