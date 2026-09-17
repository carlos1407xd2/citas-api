---
id: HU-009
tipo: historia-de-usuario
titulo: Gestionar especialidades
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-003-iniciar-sesion]]"]
relacionadas: ["[[HU-011-asignar-especialidades-profesional]]", "[[HU-016-consultar-disponibilidad]]"]
---
# HU-009 — Gestionar especialidades
## Historia de usuario
**COMO** ADMIN **QUIERO** gestionar especialidades y su duración **PARA** definir una oferta reservable con tiempos consistentes.
## Alcance
- CRUD lógico de especialidad activa y duración 30/60 minutos, incluida Medicina General.
## Fuera de alcance
- Permitir al profesional sobrescribir duración.
## Reglas de negocio
- Duración 30 = 1 slot, 60 = 2 slots consecutivos; especialidad referenciada no se borra físicamente.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-003-iniciar-sesion]]; relacionadas: [[HU-011-asignar-especialidades-profesional]], [[HU-016-consultar-disponibilidad]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** regla de duración impacta disponibilidad y reserva.
## Tareas de desarrollo
- [ ] **T-01 — Modelar catálogo y duración restringida.** Dificultad: Alto. Migración/constraint 30 o 60.
- [ ] **T-02 — Implementar gestión ADMIN.** Dificultad: Medio. Activación/desactivación y UI/API.
- [ ] **T-03 — Probar dependencia con slots.** Dificultad: Alto. Casos 30/60 y referenciados.
## Criterios de aceptación
### CA-01 — Duración válida
**Dado** ADMIN, **cuando** registra o actualiza especialidad, **entonces** solo puede establecer duración 30 o 60 minutos.
### CA-02 — Uso reservable
**Dado** especialidad activa, **cuando** es asignada y consultada para reserva, **entonces** su duración requerida es la configurada.
### CA-03 — Desactivación segura
**Dado** especialidad referenciada, **cuando** ADMIN la retira de oferta, **entonces** se desactiva sin borrado físico.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Constraint/migración, relación con slots y pruebas evidenciados.
- [ ] Contrato/UI/documentación Scrum actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

