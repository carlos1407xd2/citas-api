# Convenciones de la LLM Wiki

- Cada claim debe enlazar una fuente o marcarse como inferencia.
- Clasificación durable: `HECHO`, `DECISIÓN`, `PREFERENCIA`, `PREGUNTA ABIERTA`.
- `QUERY` parte de `wiki/index.md`, consulta páginas relevantes y verifica contra código/especificaciones.
- `LEARN` solo persiste conocimiento durable después de una interacción sustancial y verificación.
- `LINT` busca contradicciones, claims obsoletos, duplicados, páginas huérfanas, enlaces rotos, decisiones no aprobadas y contenido sensible.
- `log.md` registra fecha, operación, fuentes/páginas afectadas y resultado; es append-only.
