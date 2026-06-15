# TFG Juan de Mariana — Análisis Historiográfico de las Fuentes

> **Trabajo de Fin de Grado**  
> Estudio de las fuentes historiográficas utilizadas por Juan de Mariana (1536–1624) en los cuatro primeros libros de su *Historia General de España*, con metodología asistida por inteligencia artificial.

---

## ¿Qué es esto?

Este repositorio contiene el **rastro completo de investigación** de un TFG que intenta responder una pregunta sencilla en apariencia:

> ¿Tuvo Juan de Mariana acceso real a los autores clásicos que cita en su *Historia General de España*?

La pregunta es más compleja de lo que parece. Mariana escribía en el Colegio de Jesuitas de Toledo a finales del siglo XVI. Citaba a Plinio, a Tito Livio, a Polibio, a Estrabón, a San Isidoro… un total de **68 autores distintos** en solo los cuatro primeros libros de su obra. La cuestión es si los leyó directamente o los conoció a través de compilaciones, epítomes, florilegios y tradiciones indirectas — algo muy distinto.

Para responderla, este proyecto va acumulando datos estructurados, validaciones automatizadas y documentación metodológica que permitan responder no solo *si* existían las obras, sino *cómo* y *para qué* las usaba Mariana.

---

## La tesis del TFG

El trabajo partió de una pregunta binaria (tuvo acceso / no tuvo acceso), pero a mitad de investigación el equipo —con ayuda de un experto en historiografía— la reorientó hacia un análisis más fértil:

> **¿Para qué usa Mariana a cada autor?**

Esto transformó el estudio en una **tipología funcional de las citas**: no se trata solo de verificar existencias bibliográficas, sino de entender la **construcción historiográfica** de Mariana — qué autores usa para geografía, cuáles para guerras, cuáles para cronología, cuáles para materia mítica, cuáles cita con reservas y cuáles para desacreditar.

Y eso es precisamente lo que revelan los datos. Mariana no citaba al azar: tenía un **sistema**. Plinio va casi siempre para geografía. Tito Livio para guerras. Justino como epitomista de confianza para cronología. Y cuando entraba en terrenos dudosos (reyes fabulosos, falsificaciones), desplegaba múltiples autores en contraste — una muestra de su escepticismo humanista.

---

## ¿Qué encontrarás aquí?

### Las tablas de investigación (`data/`)

El núcleo del proyecto son **tres tablas estructuradas** que van ganando profundidad progresivamente:

| Archivo | ¿Qué contiene? |
|---------|----------------|
| `tabla_base.*` | **180 citas** extraídas de las notas de lectura del investigador, con libro, capítulo, autor, pasaje, función de la cita, tipo de fuente y observaciones |
| `validacion_1617.*` | Las mismas 180 citas, pero con el resultado de la validación automatizada contra el OCR de la edición de 1617 — indica si el nombre del autor se localizó o no en el texto impreso |
| `validacion_por_lotes.*` | La validación completa con los fragmentos OCR candidatos, organizada por lotes de capítulos para facilitar la revisión manual |
| `obras_explicitas.*` | Los **18 casos** donde Mariana nombra al autor **y** a la obra en el mismo pasaje — el estándar de oro de la identificación |

Cada tabla existe en tres formatos: `.xlsx` (editable), `.csv` (procesable) y `.md` (legible). Los scripts que las generan están en `scripts/`.

### El OCR de la edición de 1617 (`sources/`)

Se descargó de Internet Archive la edición latina ampliada de 1617 (tomo primero) y se ejecutó un OCR completo. El archivo de texto pesa **3.8 MB** y contiene aproximadamente **96.000 líneas** de texto del siglo XVII con tipografía de la época. Es una fuente primaria digitalizada, con todos los errores de OCR que eso implica.

### Los scripts de procesamiento (`scripts/`)

Seis scripts en Python que automatizan el proceso:

1. **`build_citation_use_table.py`** — Extrae las citas del documento Word original donde el investigador tomó notas
2. **`validate_table_against_1617.py`** — Busca cada nombre de autor en el OCR, segmentado por libro y capítulo
3. **`apply_explicit_works_phase2_complete.py`** — Identifica los pasajes donde autor + obra aparecen juntos
4. Scripts auxiliares de exportación y resumen

### La documentación académica (`docs/`)

- **`MEMORIA.md`** — La memoria completa del proyecto con la metodología, resultados fase por fase y contexto
- **`PLAN_REORIENTACION_METODOLOGICA.md`** — El documento que fija el cambio de eje desde "tuvo acceso" hacia "para qué lo usa"

---

## ¿Qué se ha descubierto hasta ahora?

### Sobre la existencia de los autores

El **85.3%** de los 68 autores tenían ediciones impresas **antes de 1592**, verificadas contra seis catálogos internacionales (VIAF, USTC, GW, BNE, CCPB, Biblioteca de Castilla-La Mancha). Esto significa que, en principio, Mariana **podía** haber tenido acceso a la mayoría de las obras que cita.

Pero hay matices importantes:

- **1 falsificación**: el Falso Beroso, una obra forjada en 1498 por Annio de Viterbo que Mariana usa precisamente para desacreditar las leyendas sobre los primeros reyes de España. Paradójicamente, cita una falsificación para hacer crítica de fuentes.
- **2 obras perdidas**: Filisto de Siracusa y Quinto Fabio Píctor, de las que solo se conservan fragmentos. Mariana los conocía probablemente a través de citas en otros autores.
- **Autores sin edición impresa**: al menos 5 autores (Moro Rasis, Miguel Sincelo, Braulio, San Ildefonso, Pelayo de Oviedo) circulaban solo en manuscritos, lo que hace más improbable que Mariana tuviera acceso directo.

### Sobre la validación contra el texto impreso

Del total de 180 citas extraídas de las notas de lectura, **113 (62.8%)** se localizaron automáticamente en el OCR de la edición de 1617. El resto no se encontró por razones diversas:

- Variantes ortográficas en el OCR (tipografía del XVII)
- Nombres que el OCR reconoció mal
- Menciones que dependen de contexto más amplio del pasaje
- Posibles errores en las notas del investigador

Todas las validaciones están marcadas como **"Pendiente de verificación visual"** — el OCR no reemplaza al facsímil, solo ayuda a localizar los pasajes.

### Sobre la función de las citas

Los datos revelan patrones claros en cómo usa Mariana a sus autores. Plinio es el más citado (13 veces), casi siempre para **geografía**. Tito Livio (10 veces) es la **autoridad narrativa** para guerras y conquistas. San Isidoro (9 veces) funciona como **puente entre el mundo clásico y el medieval**, especialmente para etimologías y transmisión textual. Y hay todo un grupo de autores de la Antigüedad tardía y el medievo (Orosio, Casiodoro, Beda, Sigiberto) que Mariana usa para anclar cronologías y tradiciones eclesiásticas.

La clasificación completa de las 180 citas está en `data/tabla_base.csv` — es la materia prima para el análisis historiográfico que está pendiente de redactar.

---

## El papel de la inteligencia artificial

Este proyecto se ha desarrollado con la asistencia de **agentes de IA** (Claude de Anthropic, ejecutándose en el entorno OpenCode). Merece una explicación transparente de cómo se usó y qué límites tuvo.

### ¿Para qué se usó la IA?

- **Escribir scripts Python** que automatizan el procesamiento de datos — desde la extracción de tablas del Word original hasta la validación contra 96.000 líneas de OCR
- **Realizar búsquedas sistemáticas** en los 6 catálogos internacionales, autor por autor, para verificar la existencia de ediciones pre-1592 — un proceso que manualmente habría llevado semanas
- **Procesar el OCR masivo** de la edición de 1617, segmentándolo por libros y capítulos para localizar cada mención de autor
- **Analizar los fragmentos** para identificar obras explícitas (donde autor + obra aparecen juntos)
- **Reestructurar el repositorio**, actualizar rutas en los scripts, redactar documentación

### ¿Qué NO hizo la IA?

- **No leyó la obra original**: el investigador leyó la edición de 1601 y tomó notas. La IA trabajó sobre esas notas.
- **No definió el criterio historiográfico**: la clasificación por función de cita la definió el investigador con el asesor.
- **No visitó la biblioteca**: la verificación de exlibris jesuitas requiere visita presencial.
- **No cotejó el facsímil**: la transcripción verificada de los fragmentos OCR es manual y está pendiente.

### Principios de verificación

Para mitigar el riesgo de alucinaciones (fabricación de referencias), se siguieron estos principios:

1. **Trazabilidad**: cada autor verificado tiene su ID VIAF documentado en las tablas
2. **Fuente primaria real**: el OCR de 1617 es un documento auténtico descargado de Internet Archive
3. **Criterio conservador**: las obras explícitas solo se asignan cuando el OCR muestra claramente autor + obra en el mismo pasaje
4. **Validación manual pendiente**: todas las entradas automatizadas están marcadas para verificación visual contra el facsímil

La IA actuó como **asistente de investigación**: ejecutó búsquedas sistemáticas, procesó grandes volúmenes de texto, generó tablas estructuradas y liberó al investigador para centrarse en el análisis crítico y la interpretación.

---

## Cómo usar este repositorio

```bash
# Clonar
git clone https://github.com/RRCarlos/TFG_JUAN_DE_MARIANA.git
cd TFG_JUAN_DE_MARIANA

# Instalar dependencias
pip install -r requirements.txt
```

Los scripts se pueden ejecutar individualmente para regenerar las tablas, pero **requieren el Word original** (`Historia general de España.docx`) que no está en el repo por derechos de autor. Las tablas pregeneradas en `data/` contienen el resultado completo del análisis.

---

## Estado del proyecto

| Área | Estado |
|------|--------|
| Extracción y verificación de autores | ✅ Completo |
| Validación contra OCR | ✅ Completo |
| Identificación de obras explícitas | ✅ Completo |
| Reorientación metodológica | ✅ Documentada |
| Transcripción verificada de fragmentos | 🔲 Pendiente |
| Análisis historiográfico | 🔲 Pendiente |
| Redacción de conclusiones | 🔲 Pendiente |

---

## Referencias

**Catálogos**: [VIAF](https://viaf.org) · [USTC](https://ustc.ac.uk) · [GW](https://gesamtkatalogderwiegendrucke.de) · [BNE](https://www.bne.es) · [CCPB](https://bvpb.mcu.es) · [Biblioteca CLM](https://patrimoniodigital.castillalamancha.es)

**Bibliotecas digitales**: [Gallica](https://gallica.bnf.fr) · [Cervantes Virtual](https://www.cervantesvirtual.com) · [Internet Archive](https://archive.org)

**Obra principal**: Mariana, J. de. *Historia General de España*. Toledo, 1601. — *Historiae de rebus Hispaniae libri XXX*. Maguncia, 1617.

---

**TFG Juan de Mariana** — Mayo 2026  
[Repositorio en GitHub](https://github.com/RRCarlos/TFG_JUAN_DE_MARIANA)
