---
id: HU-015
tipo: historia-de-usuario
titulo: Consultar calendario profesional
estado: Borrador
epica: "[[EP-003-disponibilidad-profesional]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 3 — Agenda publicable"
dependencias: ["[[HU-013-crear-bloques-disponibilidad]]"]
relacionadas: ["[[HU-025-consultar-agenda-profesional]]"]
---
# HU-015 — Consultar calendario profesional
## Historia de usuario
**COMO** PROFESSIONAL **QUIERO** consultar mi calendario de bloques **PARA** revisar la disponibilidad que publiqué.
## Alcance
- Consulta de bloques propios por fecha/sede según contrato.
## Fuera de alcance
- Agenda de citas aprobadas, tratada en [[HU-025-consultar-agenda-profesional]].
## Reglas de negocio
- Solo calendario propio.
## Dependencias y relaciones
- Épica: [[EP-003-disponibilidad-profesional]]; depende de [[HU-013-crear-bloques-disponibilidad]]; relacionada: [[HU-025-consultar-agenda-profesional]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** consulta filtrable con ownership y UI calendario.
## Tareas de desarrollo
- [ ] **T-01 — Exponer consulta propia filtrable.** Dificultad: Medio. API y ownership.
- [ ] **T-02 — Renderizar calendario.** Dificultad: Medio. Estados vacío/error/loading.
- [ ] **T-03 — Probar aislamiento de profesional.** Dificultad: Medio. Autorización.
## Criterios de aceptación
### CA-01 — Consulta propia
**Dado** PROFESSIONAL autenticado, **cuando** consulta su calendario, **entonces** visualiza sus bloques por fecha y sede.
### CA-02 — Aislamiento
**Dado** otro profesional tiene bloques, **cuando** el actor consulta, **entonces** no puede ver ni modificar esos bloques.
## Definition of Done
- [ ] CA-01 y CA-02 validados.
- [ ] Ownership, filtros y estados de UI evidenciados.
- [ ] Contrato y trazabilidad Scrum actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

