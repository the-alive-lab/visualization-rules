# Aplicación práctica

## Flujo de trabajo

1. Identificar la pregunta que una lectora o agente necesita resolver.
2. Verificar que la fuente textual justifica nodos, conexiones y dirección de flechas.
3. Elegir la representación menos compleja que permita interpretar la respuesta; para grafos Markdown, probar capacidades actuales de Mermaid y la diagramación del visor de destino antes de descartar ese formato.
4. Escribir una interpretación textual y una nota de límites.
5. Revisar accesibilidad, mantenibilidad, coherencia semántica y resultado en el visualizador real. Si Mermaid no ofrece claridad suficiente, evaluar SVG con representación textual alternativa.

## Ejemplo ilustrativo de ciclo

```mermaid
flowchart LR
  A[Necesidad identificada] --> B[Propuesta de representación]
  B --> C[Revisión humana]
  C -->|Aprobada| D[Publicación]
  C -->|Revisar| B
```

**Cómo leerlo:** ejemplo de un ciclo editorial, no protocolo prescrito para los proyectos de The Alive Lab.

**Límite:** no presupone herramientas concretas, roles fijos ni obligatoriedad de una aprobación formal para cada diagrama.

## Contraste de formatos

Al comparar Mermaid y SVG, evaluar por separado (a) fidelidad a conceptos y relaciones, (b) facilidad de lectura, (c) capacidad de distribución visual, (d) mantenimiento de cambios y (e) accesibilidad. Un mejor layout no implica mayor cobertura semántica. Las capacidades pueden variar por versión y motor: documentar el entorno de renderizado si afecta la conclusión.

Ejemplo abierto: [Lifecycle de TDidacta, Mermaid vs. SVG](https://github.com/the-alive-lab/tdidacta/blob/main/lifecycle/visual-comparison-mermaid-svg.md). Su objetivo es comparar alternativas, no imponer una tecnología.

## Ejemplo: relaciones posibles sin necesidad causal

En [el inventario de conceptos candidatos de TDidacta](https://github.com/the-alive-lab/tdidacta/blob/main/foundations/concept-candidates.md), un grafo editable distingue intención, fuente, realización, experiencia y evidencia. Etiquetas modales («puede orientar», «puede informar», «puede facilitar», «puede producir») evitan presentar los vínculos como garantías. La relación directa entre intención y realización evita sugerir que toda realización necesita una fuente documental intermedia.

El ejemplo acompaña el diagrama con «Cómo leerlo», una lectura textual equivalente y límites. La forma gráfica ayuda a ver relaciones; **su dirección espacial no establece un protocolo obligatorio**. Los trazos discontinuos refuerzan algunas posibilidades, pero no reemplazan el significado de las etiquetas ni del texto.

**Comprobación editorial:** contrastar nodos y flechas con la fuente, detectar dependencias falsamente implicadas, verificar legibilidad de etiquetas en GitHub y mantener la interpretación incluso sin renderizado. Una captura visualmente satisfactoria es revisión de legibilidad, no evidencia de eficacia pedagógica ni prueba general de accesibilidad.

## Adopción local

Recomendamos enlazar a este repositorio desde el README o AGENTS.md del proyecto consumidor, indicar versión y diferenciar **referencia** de **adopción**. No copiar fragmentos silenciosamente ni hacer que un agente los trate como política superior a la autoridad local.
