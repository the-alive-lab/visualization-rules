# Visualization Rules

Reglas compartidas para visualizar conocimiento, estructuras y operaciones en proyectos de **The Alive Lab**.

> **Estado:** propuesta inicial (v0.1). Este repositorio es una referencia reutilizable; enlazarlo desde otro proyecto **no implica** que sus reglas sean obligatorias o que ya se hayan adoptado allí.

## Propósito

Hacer que las explicaciones estructurales sean más fáciles de comprender, revisar y mantener, para personas y agentes, **sin convertir los diagramas en fuentes normativas independientes del texto**.

Las visualizaciones son útiles cuando aclaran una relación, distinción, secuencia, mecanismo, ciclo, responsabilidad o frontera. No se requieren por motivos estéticos ni en todos los documentos.

## Accesos

- [Reglas editoriales y de selección](rules/document-visualizations.md)
- [Guía de aplicación y ejemplos](guides/application.md)
- [Entrada para agentes y LLM](AGENTS.md)
- [Índice de lectura para máquinas](llms.txt)

## Principios

1. **Finalidad explícita:** cada visual responde a una pregunta de lectura concreta.
2. **Elección según el problema:** flujo, grafo, tabla, mapa conceptual o esquema, según qué deba explicarse.
3. **Texto y visual se complementan:** el visual no reemplaza definiciones, condiciones y excepciones.
4. **Interpretación y límites:** explicar qué representa y, especialmente, qué *no* representa.
5. **Editabilidad:** preferir Mermaid, Markdown y esquemas de texto cuando sean suficientes.
6. **Proporcionalidad:** evitar agregar diagramas cuyo costo de mantenimiento exceda su aporte.
7. **Sin normatividad accidental:** identificar expresamente relaciones ilustrativas, hipótesis, variantes y secuencias no obligatorias.

## Adopción por otros proyectos

Cada repositorio puede enlazar este estándar en su README o en su archivo `AGENTS.md` y especificar **qué versión o sección adopta**. El uso es optativo hasta que la autoridad del proyecto lo confirme. Ante conflictos, prevalecen los documentos canónicos específicos del proyecto.

Ejemplo de referencia:

> Convenciones visuales de referencia: [The Alive Lab / Visualization Rules](https://github.com/the-alive-lab/visualization-rules). Aplicación sujeta a las reglas propias del proyecto.

## Alcance y estado

Esta versión establece criterios editoriales generales, no un linter, compilador, ontología, estándar semántico universal ni garantía de que Mermaid renderice idénticamente en todas las plataformas. Su aplicación debe evaluarse caso por caso.

**Acceso:** GitHub puede mantener este repositorio privado; para ofrecer acceso público fuera de las cuentas autorizadas, un administrador debe cambiar su visibilidad a pública.