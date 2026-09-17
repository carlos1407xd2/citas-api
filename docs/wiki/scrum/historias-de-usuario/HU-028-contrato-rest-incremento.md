---
id: HU-028
tipo: historia-de-usuario
titulo: Documentar contrato REST por incremento
estado: Borrador
epica: "[[EP-007-integracion-y-calidad-del-incremento]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 4 — Cita general"
dependencias: ["[[HU-003-iniciar-sesion]]"]
relacionadas: ["[[HU-016-consultar-disponibilidad]]", "[[HU-017-reservar-cita-general]]", "[[HU-018-solicitar-cita-especializada]]", "[[HU-019-decidir-cita-especializada]]", "[[HU-024-decidir-reprogramacion]]"]
---
# HU-028 — Documentar contrato REST por incremento
## Historia de usuario
**COMO** equipo de producto **QUIERO** documentar y verificar el contrato REST de cada capacidad cross-repo aprobada **PARA** integrar frontend y backend sin un BFF ni supuestos incompatibles.
## Alcance
- Recursos, operaciones, autorización, entradas/salidas, errores y CORS de cada HU aprobada que cruce UI/API.
## Fuera de alcance
- Implementar Express/BFF, CI/CD obligatorio o fijar framework frontend antes de elección.
## Reglas de negocio
- REST JSON directo a Spring Boot; servidor conserva validación, ownership, estados y reservas; URL API configurable por environment.
## Dependencias y relaciones
- Épica: [[EP-007-integracion-y-calidad-del-incremento]]; depende de [[HU-003-iniciar-sesion]]; relacionadas: [[HU-016-consultar-disponibilidad]], [[HU-017-reservar-cita-general]], [[HU-018-solicitar-cita-especializada]], [[HU-019-decidir-cita-especializada]], [[HU-024-decidir-reprogramacion]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** coordinación de seguridad, errores, contratos y dos repositorios.
## Tareas de desarrollo
- [ ] **T-01 — Diseñar contrato para HU aprobada.** Dificultad: Alto. Operaciones, roles, payloads, errores y no secretos.
- [ ] **T-02 — Implementar consumidores/proveedores acordados.** Dificultad: Alto. Backend REST y frontend directo según framework elegido.
- [ ] **T-03 — Verificar integración.** Dificultad: Alto. Pruebas backend/frontend/cross-repo aplicables sin generar artefactos no aislados.
## Criterios de aceptación
### CA-01 — Contrato explícito
**Dado** una HU cross-repo aprobada, **cuando** se inicia su implementación, **entonces** existe contrato documentado con autorización, request, response y errores relevantes.
### CA-02 — Consumo directo
**Dado** frontend configurado, **cuando** ejecuta el flujo de la HU, **entonces** consume `citas-api` REST directamente y URL es configurable por environment.
### CA-03 — Autoridad backend
**Dado** solicitud manipulada desde cliente, **cuando** alcanza API, **entonces** validación, ownership, estados y reservas se aplican en backend.
## Definition of Done
- [ ] CA-01 a CA-03 validados para cada HU cross-repo incluida en el incremento.
- [ ] Evidencia de pruebas backend, frontend y contrato cuando apliquen; CORS explícito verificable.
- [ ] Sin Express/BFF, secretos ni lógica autoritativa de negocio en frontend.
- [ ] Wikilinks y evidencia de la HU funcional relacionada actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.
