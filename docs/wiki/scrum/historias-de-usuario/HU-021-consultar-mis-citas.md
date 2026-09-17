---
id: HU-021
tipo: historia-de-usuario
titulo: Consultar mis citas
estado: Borrador
epica: "[[EP-004-reserva-y-ciclo-de-cita]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 6 — Ciclo del usuario"
dependencias: ["[[HU-017-reservar-cita-general]]", "[[HU-018-solicitar-cita-especializada]]"]
relacionadas: ["[[HU-022-cancelar-cita]]", "[[HU-023-solicitar-reprogramacion]]"]
---
# HU-021 — Consultar mis citas
## Historia de usuario
**COMO** USER **QUIERO** consultar y filtrar mis citas **PARA** conocer su estado y gestionar las que correspondan.
## Alcance
- Filtros por estado/fecha y sede, profesional, especialidad, fecha/hora, duración, estado/motivo.
## Fuera de alcance
- Ver citas de otros usuarios.
## Reglas de negocio
- Ownership obligatorio; motivo de rechazo cuando exista.
## Dependencias y relaciones
- Épica: [[EP-004-reserva-y-ciclo-de-cita]]; depende de [[HU-017-reservar-cita-general]], [[HU-018-solicitar-cita-especializada]]; relacionadas: [[HU-022-cancelar-cita]], [[HU-023-solicitar-reprogramacion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** proyección segura de estados y filtros.
## Tareas de desarrollo
- [ ] **T-01 — Exponer listado/detalle con ownership.** Dificultad: Medio. API y proyección.
- [ ] **T-02 — Implementar lista/filtros UI.** Dificultad: Medio. Empty/error/loading.
- [ ] **T-03 — Probar aislamiento y motivo.** Dificultad: Medio. Datos propios/ajenos.
## Criterios de aceptación
### CA-01 — Información mínima
**Dado** USER con citas, **cuando** consulta las suyas, **entonces** ve sede, profesional, especialidad, fecha/hora, duración y estado.
### CA-02 — Filtros y rechazo
**Dado** citas de varios estados/fechas, **cuando** filtra, **entonces** obtiene coincidencias y visualiza motivo en `REJECTED`.
### CA-03 — Privacidad
**Dado** otra cuenta, **cuando** USER consulta, **entonces** no accede a citas ajenas.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Ownership, proyección sin datos excesivos y pruebas evidenciados.
- [ ] UI/API/documentación actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

