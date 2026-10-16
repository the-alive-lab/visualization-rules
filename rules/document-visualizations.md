# Visualizaciones en documentos — reglas v0.1

**Estado:** propuesta reutilizable; no adopción automática por otros proyectos.

## Cuándo visualizar

Evaluar un visual breve cuando el documento explique relaciones, operaciones, ciclos, recursividad, jerarquías, comparaciones o distinciones estructurales. Omitirlo cuando no añada comprensión verificable.

## Selección por pregunta

| Pregunta de lectura | Forma sugerida |
| --- | --- |
| ¿Cómo se mueve o cambia? | Flujo, ciclo o estados |
| ¿Cómo se relacionan elementos? | Grafo relacional |
| ¿Qué operación hace qué? | Esquema operacional o tabla comparativa |
| ¿Qué conceptos se distinguen? | Mapa conceptual o matriz |
| ¿Qué responsabilidad corresponde a cada parte? | Matriz de responsabilidades |

No presentar un grafo como secuencia obligatoria, ni un flujo como ontología de elementos.

## Composición

Cuando resulte útil, estructurar así: (1) propósito, (2) visual, (3) cómo leerlo, (4) explicación textual, (5) límites y no-afirmaciones.

Una visual principal suele ser suficiente; una segunda requiere justificación. **No hay límite numérico obligatorio**: la complejidad puede exigir más, o ninguna.

## Reglas de calidad

- Declarar la pregunta que resuelve la visualización.
- Usar etiquetas consistentes con el vocabulario definido en el documento.
- Acompañar el diagrama con interpretación textual y límites.
- Marcar propuestas, alternativas, supuestos, relaciones opcionales o incertidumbre.
- Preferir formatos versionables y accesibles (Mermaid, Markdown, texto).
- No introducir conceptos, causalidades, jerarquías o secuencias no sostenidos en la fuente.
- Evitar codificar significado exclusivamente en color o posición.
- Mantener alternativa textual suficiente para lectores y agentes que no puedan renderizar el diagrama.
- Actualizar visual y texto juntos cuando cambie la semántica.
- Revisar legibilidad en GitHub o el visualizador destino cuando sea viable.

## Casos no normativos

Estas reglas **no** prescriben un tipo único de diagrama, un número fijo de visualizaciones por archivo, ni una estructura de carpetas para otras organizaciones. La documentación canónica local prima ante conflicto.
