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
- Elegir el formato por fidelidad, legibilidad, accesibilidad, expresividad, compatibilidad y costo de mantenimiento; no asumir superioridad universal de una herramienta.
- Para grafos editables en Markdown, probar primero las capacidades **actuales** de Mermaid y del motor de distribución disponible (incluidos retornos y conexiones cruzadas) antes de concluir que hace falta SVG.
- Utilizar SVG cuando se requiera control de composición que no pueda obtenerse con claridad y esfuerzo razonable en Mermaid; mantener fuente editable y alternativa textual accesible.
- No confiar en que todos los visores de GitHub/Markdown utilicen la misma versión, motor o configuración de Mermaid. Validar en el destino real.
- No introducir conceptos, causalidades, jerarquías o secuencias no sostenidos en la fuente.
- Evitar codificar significado exclusivamente en color o posición.
- Mantener alternativa textual suficiente para lectores y agentes que no puedan renderizar el diagrama.
- Actualizar visual y texto juntos cuando cambie la semántica.
- Revisar legibilidad en GitHub o el visualizador destino cuando sea viable.

## Heurística: texto legible dentro de diagramas Mermaid

Cuando los nombres de nodos o relaciones dificulten leer el diagrama en su visor real, **optimizar primero las etiquetas sin alterar su significado**:

1. **Dividir etiquetas de nodos en unidades semánticas breves.** En diagramas Mermaid que admitan etiquetas con HTML, usar saltos explícitos como `<br/>` dentro de etiquetas entre comillas; por ejemplo, `A["Intención<br/>pedagógica"]`. Preferir cortes entre palabras o sintagmas, no dentro de términos.
2. **Mantener los nombres completos cuando sean necesarios.** Un salto de línea reorganiza texto; no autoriza abreviar conceptos hasta volverlos ambiguos ni cambiar su vocabulario canónico.
3. **Reducir la longitud visual, no necesariamente la cantidad de texto.** Equilibrar el ancho y la altura de los nodos; evitar tanto cajas desmesuradamente anchas como columnas de palabras sueltas. Dos líneas son una opción práctica frecuente, no una restricción.
4. **Redactar las etiquetas de las conexiones como frases cortas y explícitas.** Mantener verbos o modalidades que aclaren el vínculo; por ejemplo, `-->|"puede informar"|`. Si una etiqueta sigue siendo demasiado larga, trasladar su detalle a la explicación textual sin cambiar la interpretación.
5. **Evaluar el conjunto renderizado**, no cada etiqueta aislada: comprobar si las flechas, nombres y saltos se distinguen a tamaño de lectura habitual, si el grafo exige desplazamiento horizontal y si controles o márgenes tapan información.
6. **Comprobar compatibilidad antes de aplicar HTML en masa.** La interpretación de `<br/>`, comillas, Markdown strings y configuración de seguridad puede variar según versión o visor de Mermaid. Probar en el destino (por ejemplo, GitHub); si no funciona, usar otra sintaxis soportada o simplificar el diseño.

**No equiparar tamaño de caja con importancia semántica.** El ajuste de línea es una decisión de presentación; preservar una lectura textual accesible fuera del diagrama.

Esta heurística es una pauta editorial opcional. No exige insertar `<br/>` en todos los nodos ni establece un máximo universal de palabras o caracteres.

## Heurística: relaciones posibles sin cadena obligatoria

Cuando una visualización reúna **conceptos distintos** que pueden relacionarse sin depender necesariamente unos de otros:

1. Identificar cada concepto con el vocabulario de la fuente; no sustituir distinciones por una única etapa del proceso.
2. Examinar cada flecha por separado: su **dirección, verbo y modalidad** deben estar respaldados por el texto. Preferir etiquetas como «puede informar», «puede orientar» o «puede producir» cuando la relación sea contingente; no emplear «produce», «requiere» o «garantiza» sin fundamento.
3. Incluir rutas alternativas relevantes si omitirlas induciría una dependencia falsa (por ejemplo, representar también una conexión directa cuando la ruta intermedia no es necesaria). No intentar dibujar todas las posibilidades.
4. Usar diferencias de trazo solo como **ayudas visuales explicadas**, no como semántica universal. Una línea discontinua no significa por sí sola «opcional»: la etiqueta y el texto deben aclararlo; una línea continua tampoco convierte una relación posible en obligatoria.
5. Acompañar el gráfico con una **lectura textual equivalente** y límites explícitos: ausencia de secuencia obligatoria, ausencia de garantía de resultados y excepciones pertinentes.
6. Comprobar el resultado en el visor de destino; si el layout oculta etiquetas, cruza enlaces o parece imponer un orden que el contenido niega, revisar representación, disposición o formato.

**Criterio de revisión:** alguien que lea solo las etiquetas y luego la explicación debe poder distinguir qué relaciones son posibles, qué conceptos no se identifican entre sí y qué conclusiones **no** autoriza el diagrama.

Esta heurística complementa las reglas de composición y calidad; **no exige usar Mermaid, flechas discontinuas ni diagramas para todos los conceptos**.

Caso de aplicación editorial: [TDidacta — fuente, realización y aprendizaje](https://github.com/the-alive-lab/tdidacta/blob/main/foundations/concept-candidates.md). El caso ilustra la heurística; no prueba aprendizaje, ni transforma los conceptos candidatos de TDidacta en definiciones adoptadas.

## Aprendizaje de aplicación: Mermaid y SVG

La capacidad de **declarar relaciones** y la capacidad del motor de **distribuirlas de forma legible** son problemas distintos. Ciclos y retornos pueden expresarse en Mermaid sin rutas manuales; el resultado depende del layout y del entorno de renderizado. Un diagrama complejo no justifica automáticamente cambiar de formato. Cuando la distribución automática no conserve la claridad o se necesite composición precisa, considerar SVG. Comparar también fidelidad semántica: dos diagramas atractivos pueden omitir relaciones diferentes.

Caso de contraste: [TDidacta — comparación Lifecycle Mermaid/SVG](https://github.com/the-alive-lab/tdidacta/blob/main/lifecycle/visual-comparison-mermaid-svg.md), un experimento editorial sin validación de usuarios ni adopción semántica.

## Casos no normativos

Estas reglas **no** prescriben un tipo único de diagrama, un número fijo de visualizaciones por archivo, ni una estructura de carpetas para otras organizaciones. La documentación canónica local prima ante conflicto.
