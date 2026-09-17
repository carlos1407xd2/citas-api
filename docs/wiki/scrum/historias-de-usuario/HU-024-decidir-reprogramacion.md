---
id: HU-024
tipo: historia-de-usuario
titulo: Decidir reprogramación
estado: Borrador
epica: "[[EP-005-gestion-administrativa]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 6 — Ciclo del usuario"
dependencias: ["[[HU-023-solicitar-reprogramacion]]"]
relacionadas: ["[[HU-022-cancelar-cita]]", "[[HU-027-consultar-auditoria-estados]]"]
---
# HU-024 — Decidir reprogramación
## Historia de usuario
**COMO** ADMIN **QUIERO** aprobar o rechazar una reprogramación pendiente **PARA** resolver el cambio sin corromper la cita original.
## Alcance
- Aprobar: libera antigua/asigna nueva/actualiza cita. Rechazar: libera nueva/mantiene original.
## Fuera de alcance
- Cambio de profesional.
## Reglas de negocio
- Decisión ADMIN; rechazo con motivo cuando corresponda; RN-10 y RN-11.
## Dependencias y relaciones
- Épica: [[EP-005-gestion-administrativa]]; depende de [[HU-023-solicitar-reprogramacion]]; relacionadas: [[HU-022-cancelar-cita]], [[HU-027-consultar-auditoria-estados]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** transferencia atómica de reserva, estados e historial.
## Tareas de desarrollo
- [ ] **T-01 — Implementar transiciones PENDING.** Dificultad: Alto. Motivos y autorización.
- [ ] **T-02 — Transferir/liberar slots atómicamente.** Dificultad: Alto. Consistencia original/nueva.
- [ ] **T-03 — Integrar bandeja y pruebas de ambas decisiones.** Dificultad: Alto. UI/API/historial.
## Criterios de aceptación
### CA-01 — Aprobación
**Dado** reprogramación `PENDING`, **cuando** ADMIN aprueba, **entonces** libera slots antiguos, asigna nuevos y actualiza la cita.
### CA-02 — Rechazo
**Dado** reprogramación `PENDING`, **cuando** ADMIN rechaza con motivo aplicable, **entonces** libera nueva reserva y conserva cita/franja original.
### CA-03 — Decisión única
**Dado** solicitud ya decidida o actor no ADMIN, **cuando** intenta decidir, **entonces** se rechaza sin alterar reservas.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Transferencia/liberación, historial y prueba de consistencia evidenciados.
- [ ] Bandeja/UI/API y trazabilidad actualizadas.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.
