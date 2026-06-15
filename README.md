# TFG Juan de Mariana — Análisis Historiográfico de las Fuentes de la *Historia General de España* (Libros I–IV, 1601)

> **Trabajo de Fin de Grado** | Curso de Inteligencia Artificial  
> Análisis de las fuentes historiográficas utilizadas por Juan de Mariana (1536–1624) en los cuatro primeros libros de su *Historia General de España*.

---

## Resumen

Este repositorio contiene el proceso completo de investigación del TFG, que responde a la pregunta:

> **¿Para qué usa Juan de Mariana a cada autor que cita en su *Historia General de España*?**

El estudio va más allá de un mero recuento de fuentes: analiza la **función historiográfica** de cada autor dentro del discurso histórico de Mariana. No se trata solo de saber *si* existían las obras, sino de entender *cómo* y *para qué* las utiliza.

### Resultados principales

| Indicador | Dato |
|-----------|------|
| **Autores únicos** identificados en L. I–IV | 68 |
| **Citas** extraídas y clasificadas | **180** |
| **Localizadas** en la edición de 1617 mediante OCR automatizado | **113 (62.8%)** |
| **Obras explícitas** (autor + obra nombrados en el mismo pasaje) | **18** |
| **Autores con edición pre-1592 verificada** | **58 (85.3%)** |
| **Falsificaciones detectadas** | 1 (Falso Beroso / Annio de Viterbo) |
| **Obras perdidas** | 2 (Filisto, Quinto Fabio Píctor) |

---

## Pregunta de investigación

La investigación parte de una pregunta inicial:

> *¿Realmente tuvo Juan de Mariana acceso a las obras que cita?*

Esta pregunta se descompone en cuatro niveles de evidencia:

1. **¿Existieron** los autores que cita?
2. **¿Tenían ediciones impresas** antes de 1592?
3. **¿Se conservan ejemplares** en las bibliotecas jesuitas de Toledo?
4. **¿Tienen esos ejemplares marcas de propiedad jesuita?**

Tras la reorientación metodológica, el eje central pasó a ser:

> **¿Qué función cumple cada autor citado dentro del relato histórico de Mariana?**

Esto permite analizar las citas como parte de la **construcción historiográfica**: autoridad clásica, apoyo cronológico, tradición bíblica, legitimación de episodios, etc.

---

## Estructura del repositorio

```
TFG_JUAN_DE_MARIANA/
├── README.md                    ← Este documento
├── .gitignore
├── requirements.txt             ← Dependencias Python (openpyxl)
│
├── docs/                        ← Documentación académica
│   ├── MEMORIA.md               ← Memoria completa del proyecto
│   └── PLAN_REORIENTACION_METODOLOGICA.md  ← Nueva metodología (2026-05-18)
│
├── data/                        ← Tablas de investigación (CSV + XLSX + MD)
│   ├── tabla_base.*             ← 180 citas extraídas de notas Word
│   ├── validacion_1617.*        ← Localización automatizada contra OCR
│   ├── validacion_por_lotes.*   ← Validación completa con fragmentos OCR
│   └── obras_explicitas.*       ← 18 obras donde Mariana nombra autor + obra
│
├── scripts/                     ← Procesamiento y validación
│   ├── build_citation_use_table.py      ← Extrae citas del docx Word
│   ├── validate_table_against_1617.py   ← Valida contra OCR 1617
│   ├── apply_explicit_works_phase1.py   ← Fase 1: obras explícitas Libro I
│   ├── apply_explicit_works_phase2_complete.py ← Fase 2: obras explícitas I–IV
│   ├── export_validation_table_md.py    ← Exporta validación a Markdown
│   └── summary_phase2.py               ← Resumen de obras explícitas
│
└── sources/                     ← Fuentes digitalizadas
    ├── mariana_1617_tomo_primero_ocr.txt         ← OCR completo (96K líneas)
    └── mariana_1617_tomo_primero_page_numbers.json
```

---

## Metodología

### Fases completadas

| Fase | Descripción | Estado |
|------|-------------|--------|
| **1–2** | Extracción de autores desde notas Word de la edición 1601 | ✅ |
| **3–4** | Verificación en 6 catálogos internacionales (VIAF, USTC, GW, BNE, CCPB, BCLM) | ✅ |
| **5** | Verificación de ediciones pre-1592 (85.3% verificadas) | ✅ |
| **6** | Localización en Biblioteca de Castilla-La Mancha (fondos jesuitas de Toledo) | ✅ |
| **7** | OCR de la edición 1617 + validación automatizada (Internet Archive) | ✅ |
| **8** | Identificación de obras explícitas (autor + obra en mismo pasaje) | ✅ |
| **9** | Reorientación metodológica (nuevo eje: función historiográfica) | ✅ |
| **10** | Transcripción verificada de fragmentos | 🔲 |
| **11** | Análisis historiográfico por función de cita | 🔲 |

### Herramientas

- **OCR**: Edición 1617 de Google Books / Internet Archive (`bub_gb_qpHbv84HpA0C`)
- **Procesamiento**: Python 3.10+ con openpyxl
- **Validación**: Búsqueda automatizada de nombres de autor en OCR segmentado por libros
- **Catálogos**: VIAF, USTC, GW, BNE, CCPB, Biblioteca de Castilla-La Mancha

### Ediciones de referencia

| Edición | Año | Uso |
|---------|-----|-----|
| *Historia General de España* (castellano) | **1601** | Texto base de referencia. BNE, tomo primero |
| *Historia General de España* (latín, ampliada) | **1617** | Testigo auxiliar para búsqueda OCR |

---

## Hallazgos clave

### Autores con status especial

| Categoría | Autores | Implicación |
|-----------|---------|-------------|
| **Falsificación** | Falso Beroso (Annio de Viterbo) | Mariana utiliza una obra forjada en 1498, no fuentes antiguas genuinas |
| **Obra perdida** | Filisto, Quinto Fabio Píctor | Solo fragmentos conservados; Mariana cita a través de tradición indirecta |
| **Principalmente manuscritos** | Moro Rasis, Miguel Sincelo, Braulio, San Ildefonso | Sin edición impresa verificada antes de 1592 |
| **Autoría dudosa** | Julio Capitolino, Trebellio Polión (Historia Augusta), Andrea de' Bardi | Atribuciones cuestionadas por la crítica textual |

### Vías de transmisión

1. **Ediciones impresas** (~70%): Desde 1450, producción masiva de clásicos
2. **Compilaciones medievales** (~20%): Isidoro, Beda preservan fragmentos
3. **Manuscritos** (~10%): Obras menores o fragmentos específicos

### Incunables más antiguos localizados

| Autor | Obra | Año |
|-------|------|-----|
| San Jerónimo | Vulgata | 1456 |
| Cicerón | Opera | 1465 |
| Virgilio | Opera | 1469 |
| Tito Livio | Ab Urbe Condita | 1470 |
| Plutarco | Vidas Paralelas | 1470 |

---

## Cómo usar este repositorio

```bash
# Clonar
git clone https://github.com/RRCarlos/TFG_JUAN_DE_MARIANA.git
cd TFG_JUAN_DE_MARIANA

# Instalar dependencias
pip install -r requirements.txt

# Regenerar tabla base desde el Word original
python scripts/build_citation_use_table.py

# Validar contra OCR 1617
python scripts/validate_table_against_1617.py

# Identificar obras explícitas
python scripts/apply_explicit_works_phase2_complete.py
```

> **Nota**: El script `build_citation_use_table.py` requiere el archivo Word original (`Historia general de España.docx`) que no está incluido en el repositorio por derechos de autor. Las tablas pregeneradas en `data/` contienen el resultado completo del análisis.

---

## Estado del proyecto

| Fase | Estado |
|------|--------|
| Extracción y verificación de fuentes | ✅ Completo |
| OCR y validación automatizada | ✅ Completo |
| Identificación de obras explícitas | ✅ Completo |
| Reorientación metodológica | ✅ Completo |
| Transcripción verificada de fragmentos | 🔲 Pendiente |
| Análisis historiográfico completo | 🔲 Pendiente |
| Redacción de conclusiones | 🔲 Pendiente |

---

## Referencias

### Catálogos internacionales
- [VIAF](https://viaf.org) — Authority files internacionales
- [USTC](https://ustc.ac.uk) — Ediciones europeas pre-1600
- [GW](https://gesamtkatalogderwiegendrucke.de) — Incunables (1450–1500)

### Bibliotecas españolas
- [BNE](https://www.bne.es) — Biblioteca Nacional de España
- [CCPB](https://bvpb.mcu.es) — Catálogo Colectivo del Patrimonio Bibliográfico Español
- [Biblioteca CLM](https://patrimoniodigital.castillalamancha.es) — Fondo del Colegio de Jesuitas de Toledo

### Bibliotecas digitales
- [Gallica](https://gallica.bnf.fr) — Bibliothèque nationale de France
- [Biblioteca Virtual Miguel de Cervantes](https://www.cervantesvirtual.com)

### Referencias académicas
- Cirot, G. *Mariana historien: études sur l'historiographie espagnole*. Burdeos: Feret & Fils, 1905.

---

## Licencia

El contenido académico y los datos de investigación son de acceso abierto.  
Los scripts están disponibles bajo licencia MIT.

---

**TFG Juan de Mariana** — Mayo 2026  
[Repositorio](https://github.com/RRCarlos/TFG_JUAN_DE_MARIANA)
