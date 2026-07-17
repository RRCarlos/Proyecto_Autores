# Bitácora de Investigación: Edición de 1601

## Estado

| Campo | Valor |
|-------|-------|
| **Inicio** | 2026-07-17 |
| **Estado** | EN CURSO |
| **Fase actual** | Fase 2 — Validación (tras Oleada 2) |

---

## Fase 0 — Inicialización

**Fecha**: 2026-07-17
**Estado**: Completada ✅

- Plan de investigación creado (`PLAN_INVESTIGACION_1601.md`)
- Esta bitácora creada
- Commit `d728edc` push a main

---

## Fase 1 — Oleada 1: Repositorios principales

**Fecha**: 2026-07-17
**Estado**: Completada ✅

### Repositorios consultados

| # | Repositorio | URL | Resultado |
|---|-------------|-----|-----------|
| 1 | BNE (Biblioteca Digital Hispánica) | bdh.bne.es | ❌ NO ENCONTRADA (búsqueda directa falló) |
| 2 | Biblioteca Virtual Miguel de Cervantes | cervantesvirtual.com | ❌ NO ENCONTRADA (ediciones: 1780, 1678, 1794, 1818) |
| 3 | Internet Archive | archive.org | ❌ NO ENCONTRADA (ediciones: 1780, 1794, 1818, 1678) |
| 4 | HathiTrust | hathitrust.org | ❌ NO ENCONTRADA |
| 5 | Gallica (BnF) | gallica.bnf.fr | ❌ NO ENCONTRADA |
| 6 | WorldCat / catálogos | worldcat.org | ❌ NO ENCONTRADA (encontrada 1817-1822, OCLC 8097245) |

**Conclusión**: La edición de 1601 no está en ninguno de los 6 repositorios principales.

---

## Fase 2 — Oleada 2: Búsqueda dirigida + hallazgos críticos

**Fecha**: 2026-07-17
**Estado**: Completada ✅

### CANDIDATOS ENCONTRADOS ⭐

#### Candidato 1: Universidad de Chile (libros.uchile.cl) — ONLINE READING

| Campo | Valor |
|-------|-------|
| **Repositorio** | Universidad de Chile — Libros de Oro |
| **URL Tomo I** | https://libros.uchile.cl/109 |
| **URL Tomo II** | https://libros.uchile.cl/110 |
| **DOI Tomo I** | 10.34720/ng00-yq91 |
| **DOI Tomo II** | 10.34720/8582-y679 |
| **Formato** | FlippingBook (lectura online) |
| **Derechos** | Public Domain |
| **Contenido** | Tomo I: Prólogo + Libros I-XV / Tomo II: Libros XVI-XXX |
| **¿Buen OCR?** | DESCONOCIDO — formato FlippingBook, no se puede descargar PDF directamente |

**Nota**: La Universidad de Chile tiene AMBOS tomos de la edición de 1601. El formato FlippingBook es lectura online; no se encontró descarga directa de PDF.

#### Candidato 2: BNE (Biblioteca Nacional de España) — DIGITALIZADA, VISOR CAÍDO

| Campo | Valor |
|-------|-------|
| **Repositorio** | BNE — Biblioteca Digital Hispánica |
| **Catálogo** | datos.bne.es/obra/XX2073435.html |
| **Signatura** | BNE 3/31952 |
| **USTC** | 5006449 |
| **URL visor (antigua)** | http://bdh-rd.bne.es/viewer.vm?id=0000193802 |
| **Estado visor** | ❌ HTTP 403 — caído o formato de URL cambiado |
| **¿Digitalizada?** | SÍ — confirmado por múltiples fuentes |

**Nota**: La BNE tiene la edición digitalizada pero el visor del BDH devuelve 403. La URL puede haber cambiado de formato.

#### Candidato 3: Biblioteca Cartagena (USal) — TRANSCRIPCIONES + ESCANEADOS

| Campo | Valor |
|-------|-------|
| **Repositorio** | Biblioteca Cartagena — Universidad de Salamanca |
| **URL** | bibliotecacartagena.usal.es |
| **Contenido** | Transcripciones del tomo II + escaneados originales de las páginas |
| **Fuente** | Copia de la BNE (signatura 3/31952) |
| **Páginas disponibles** | Portada, pp. 252-476, colofón (parcial) |

**Nota**: Tiene transcripciones diplomáticas + imágenes facsimilares del tomo II. No es completo (solo pp. 252-476), pero confirma la existencia y legibilidad del original.

### Fuentes académicas consultadas

| Fuente | Referencia clave |
|--------|-----------------|
| Sánchez Torres (2024) | Studia philologica valentina 26, pp. 45-60. DOI: 10.7203/sphv.26.28040 |
| UC3M (s.f.) | Estudio de Libros I-IV. Convención: (I 2) = edición 1601 |
| Brais Ferrás García (2024) | Talia Dixit — confirma diferencias entre ediciones |
| Instituto Juan de Mariana | Resumen histórico de la obra |
| Open Library | Entrada OL43725470M |
| Deutsche Digitale Bibliothek | Ediciones 1592 (latín) y 1605 (Maguncia), NO 1601 |

### Ediciones conocidas de la Historia General (cadena de correcciones)

| # | Año | Lugar | Editor | Notas |
|---|-----|-------|--------|-------|
| 1 | 1601 | Toledo | Pedro Rodríguez | **EDICIÓN OBJETIVO** — Primera edición española |
| 2 | 1605 | Maguncia (Mainz) | Schönwetter | Segunda edición (latín completo, 30 libros) |
| 3 | 1608 | Madrid | Luis Sánchez | Tercera edición — Mariana corregida |
| 4 | 1617 | Madrid | Viuda de Alonso Martín | Cuarta — "corregida y muy aumentada" — +500 correcciones vs 1608 |
| 5 | 1623 | Madrid/Toledo | Luis Sánchez / Diego Rodríguez | Quinta — más completa, incluye falsos cronicones |

**Implicación**: La edición de 1617 NO es sustancialmente igual a la de 1601. El propio Mariana declaró que la de 1617 tenía "exceden de quinientas" correcciones y adiciones respecto a la de 1608 (que a su vez era corregida desde 1601).

---

## Fase 3 — Punto de decisión

**Fecha**: --
**Estado**: PENDIENTE

### Decisión pendiente

¿Qué candidato elegimos para la verificación? Opciones:
1. **U. de Chile** — ambas ediciones disponibles online, formato FlippingBook
2. **BNE** — digitalizada pero visor caído (posible resolver con URL alternativa)
3. **Ambos** — verificar ambos y quedarnos con el mejor

---

## Fase 4A — Verificación de candidato

**Fecha**: --
**Estado**: No aplicada / Pendiente

---

## Fase 4B — Oleada 2 (extras)

**Fecha**: 2026-07-17
**Estado**: Completada ✅

### Repositorios adicionales consultados

| # | Repositorio | Resultado |
|---|-------------|-----------|
| 1 | Open Library | Entrada encontrada (OL43725470M) — sin descarga directa |
| 2 | Deutsche Digitale Bibliothek | Ediciones 1592 y 1605 — NO 1601 |
| 3 | Instituto Juan de Mariana | Resumen histórico — sin digitalización |
| 4 | UC3M | Estudio académico — referencias a la edición |
| 5 | USal (Biblioteca Cartagena) | ✅ Transcripciones + escaneados parciales |

---

## Fase 5 — Oleada 3: Contacto directo

**Fecha**: --
**Estado**: Pendiente

---

## Fase 6 — Síntesis y selección

**Fecha**: --
**Estado**: Pendiente

---

## Fase 7 — Reporte final

**Fecha**: --
**Estado**: Pendiente

---

## Errores y problemas encontrados

| # | Fase | Problema | Acción tomada | Resultado |
|---|------|----------|---------------|-----------|
| 1 | Fase 1 | BNE búsqueda directa falló (site:bdh.bne.es no encontró la edición) | Cambiar a búsqueda en datos.bne.es (catálogo) | Encontrada en Oleada 2 |
| 2 | Fase 2 | BNE visor BDH devuelve HTTP 403 | Documentar URL antigua; buscar URL alternativa | Pendiente investigación |
| 3 | Fase 2 | U. de Chile: no hay descarga PDF directa (solo FlippingBook) | Investigar si hay API o exportación | Pendiente investigación |
| 4 | Fase 2 | Biblioteca Cartagena: solo tomo II parcial (pp. 252-476) | Usar como referencia complementaria | OK — no es fuente primaria |
| 5 | Fase 1 | Búsqueda inicial no encontró la edición de 1601 | Reintentar con búsquedas más específicas | Resuelto en Oleada 2 |
