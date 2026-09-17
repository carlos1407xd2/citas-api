---
id: HU-020
tipo: historia-de-usuario
titulo: Consultar bandeja administrativa
estado: Borrador
epica: "[[EP-005-gestion-administrativa]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 5 — Cita especializada"
dependencias: ["[[HU-018-solicitar-cita-especializada]]"]
relacionadas: ["[[HU-019-decidir-cita-especializada]]", "[[HU-024-decidir-reprogramacion]]"]
---
# HU-020 — Consultar bandeja administrativa
## Historia de usuario
**COMO** ADMIN **QUIERO** consultar solicitudes de cita y reprogramación pendientes con filtros **PARA** tomar decisiones operativas.
## Alcance
- `REQUESTED`, `PENDING` y filtros por sede, profesional, especialidad y fecha.
## Fuera de alcance
- Decisión, cubierta por HU relacionadas.
## Reglas de negocio
- Solo ADMIN; no incluir otros estados como pendientes.
## Dependencias y relaciones
- Épica: [[EP-005-gestion-administrativa]]; depende de [[HU-018-solicitar-cita-especializada]]; relacionadas: [[HU-019-decidir-cita-especializada]], [[HU-024-decidir-reprogramacion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** consulta segura con filtros interrelacionados.
## Tareas de desarrollo
- [ ] **T-01 — Definir consulta filtrable.** Dificultad: Medio. Índices y contrato.
- [ ] **T-02 — Crear bandeja ADMIN.** Dificultad: Medio. Estados loading/empty/error.
- [ ] **T-03 — Probar aislamiento y filtros.** Dificultad: Medio. Autorización/resultados.
## Criterios de aceptación
### CA-01 — Pendientes visibles
**Dado** ADMIN, **cuando** abre bandeja, **entonces** ve citas `REQUESTED` y reprogramaciones `PENDING`.
### CA-02 — Filtros
**Dado** datos pendientes, **cuando** filtra por sede, profesional, especialidad o fecha, **entonces** ve únicamente coincidencias.
### CA-03 — Rol
**Dado** USER o PROFESSIONAL, **cuando** intenta consultar la bandeja, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Filtros, índices/consulta, autorización y estados UI evidenciados.
- [ ] Contrato y trazabilidad actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

