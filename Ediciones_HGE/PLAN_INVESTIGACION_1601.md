# Plan de Investigación: Edición de 1601 con OCR accesible

## Objetivo

Encontrar una edición digitalizada de la *Historia general de España* de Juan de Mariana, edición de **1601** (Toledo, Pedro Rodríguez), con OCR de calidad suficiente para usar como referencia textual. Priorizamos opciones **Open Access** (descarga libre o visualización sin restricciones).

## Escenarios posibles

1. **Escenario A**: Encontramos la edición de 1601 con buen OCR y descargable/visible en Open Access → la usamos como referencia.
2. **Escenario B**: Encontramos la edición con buen OCR pero requiere pago/registro → documentamos el link, pero seguimos buscando OA en las oleadas restantes. Si no hay OA, finalizamos la investigación y el usuario decidirá si accede a la opción de pago.
3. **Escenario C**: No encontramos la edición de 1601 con OCR accesible → documentamos todo, dejamos registro de la investigación, y se buscará otra solución (transcripción manual, contacto con bibliotecas, etc.).

## Documentos generados

| Documento | Ruta en el repo | Propósito |
|-----------|----------------|-----------|
| `PLAN_INVESTIGACION_1601.md` | `Ediciones_HGE/` | Este plan |
| `INVESTIGACION_1601_LOG.md` | `Ediciones_HGE/` | Bitácora viva — se actualiza tras cada fase |
| `REPORTE_FINAL_1601.md` | `Ediciones_HGE/` | Reporte final: resumen, hallazgos, errores, recomendación |

## Fases

### FASE 0 — Inicialización
- Crear `PLAN_INVESTIGACION_1601.md` (este documento)
- Crear `INVESTIGACION_1601_LOG.md` con estructura base
- ✅ **Seguridad**: Commit + push a GitHub

### FASE 1 — Oleada 1: Repositorios principales (paralelo)
- Lanzar delegaciones en paralelo buscando en:
  - BNE (Biblioteca Digital Hispánica)
  - Biblioteca Virtual Miguel de Cervantes
  - Internet Archive
  - HathiTrust
  - Gallica (BnF)
  - WorldCat / catálogos bibliográficos
- Cada delegación registra en el LOG: repositorio consultado, URL, estado de digitalización, formato
- ✅ **Seguridad**: Commit + push del LOG actualizado

### FASE 2 — Oleada 1: Validación de hallazgos
- Evaluar calidad OCR de cada copia encontrada en Fase 1
- Leer muestras de texto (Libros I-IV) y comparar con el texto conocido de 1601
- Clasificar cada copia: A (usable), B (aceptable con correcciones), C (inutilizable)
- Determinar accesibilidad: Open Access / registro / pago / solo en sala
- Actualizar LOG con evaluaciones
- ✅ **Seguridad**: Commit + push del LOG actualizado

### FASE 3 — Punto de decisión
- Si hay candidato Open Access clase A o B → ir a Fase 4A (verificar y documentar)
- Si hay candidato pero requiere pago → ir a Fase 4A (documentar link, seguir buscando OA)
- Si no hay ningún candidato → ir a Fase 4B (Oleada 2)
- Documentar decisión en LOG
- ✅ **Seguridad**: Commit + push

### FASE 4A — Verificación de candidato (si existe)
- **NO SE REALIZA NINGUNA COMPRA.** Solo se documenta el link y se verifica:
  - Que efectivamente es la edición de 1601 (portada, colofón, impresor Pedro Rodríguez)
  - Que el OCR es de calidad aceptable
  - Que es Open Access o no
- Guardar evidencia (capturas, fragmentos de texto) en el LOG
- **Continuar con las oleadas restantes** para buscar opciones Open Access
- ✅ **Seguridad**: Commit + push

### FASE 4B — Oleada 2: Repositorios menos obvios (paralelo)
- Lanzar delegaciones paralelas buscando en:
  - Repositorios universitarios (USal, UCM, UAM, UV, UC3M, etc.)
  - Archivos eclesiásticos y catedralicios
  - Catálogos especializados (USTC, incunables)
  - Repositorios americanos con fondos hispánicos (UTexas, NYU, Harvard, etc.)
  - Librerías anticuarias en línea (Iberlibro, AbeBooks) — solo para localizar ejemplares, NO para comprar
- Cada delegación registra hallazgos en el LOG
- ✅ **Seguridad**: Commit + push del LOG

### FASE 5 — Oleada 3: Contacto directo (secuencial)
- Solo si Oleadas 1 y 2 no dieron resultado OA
- Contactar:
  - Servicio de reprografía de la BNE (solicitar escaneado de páginas específicas)
  - Bibliotecas universitarias con ejemplares conocidos
  - Especialistas en Mariana (Sánchez Torres, etc.) para preguntar por digitalizaciones
- Registrar respuestas en LOG
- ✅ **Seguridad**: Commit + push

### FASE 6 — Síntesis y selección
- Consolidar TODOS los hallazgos de Oleadas 1-3
- Ranking final de opciones Open Access por: calidad OCR + accesibilidad
- Si no hay OA: documentar la mejor opción de pago como referencia futura
- Documentar errores y problemas encontrados en cada fase
- Actualizar LOG con síntesis
- ✅ **Seguridad**: Commit + push

### FASE 7 — Reporte final
- Generar `REPORTE_FINAL_1601.md` con:
  - Resumen ejecutivo
  - Hallazgos detallados por repositorio
  - Evaluación de calidad OCR (si aplica)
  - Errores y problemas surgidos durante la investigación
  - Recomendación final
  - Próximos pasos
- ✅ **Seguridad**: Commit + push final

## Flujo de ejecución

```
Fase 0 (init) → Fase 1 (Oleada 1) → Fase 2 (validación) → Fase 3 (decisión)
                                                                    │
                                                    ┌───────────────┴───────────────┐
                                                    ▼                               ▼
                                              Fase 4A (verificar)           Fase 4B (Oleada 2)
                                                    │                               │
                                                    │                      Fase 5 (Oleada 3)
                                                    │                               │
                                                    └───────────────┬───────────────┘
                                                                    ▼
                                                           Fase 6 (síntesis)
                                                                    │
                                                                    ▼
                                                           Fase 7 (reporte)
```

## Notas

- **Prioridad Open Access**: aunque se encuentre un candidato de pago, se continúan las oleadas buscando opciones libres.
- **Sin permisos de compra**: el usuario decidirá sobre opciones de pago cuando vuelva.
- **Trabajo autónomo**: el investigador trabaja sin supervisión. Los problemas se documentan en el LOG y se busca alternativa.
- **Criterio de parada**: si tras todas las oleadas no hay candidato Open Access, se finaliza la investigación con documentación completa.
