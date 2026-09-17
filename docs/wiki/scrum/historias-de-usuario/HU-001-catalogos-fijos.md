---
id: HU-001
tipo: historia-de-usuario
titulo: Consultar catálogos fijos
estado: Borrador
epica: "[[EP-001-identidad-y-perfil]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 1 — Acceso seguro"
dependencias: []
relacionadas: ["[[HU-002-registrar-usuario]]", "[[HU-007-gestionar-eps]]"]
---
# HU-001 — Consultar catálogos fijos
## Historia de usuario
**COMO** usuario de la aplicación  
**QUIERO** consultar los catálogos fijos disponibles  
**PARA** usar valores válidos y consistentes en los flujos del sistema.
## Alcance
- Roles, estados de cita y reprogramación, regímenes y sedes precargados y de solo lectura.
## Fuera de alcance
- Administración de catálogos configurables.
## Reglas de negocio
- Catálogos fijos definidos por RF-05; sedes son HIC e ICV.
## Dependencias y relaciones
- Épica: [[EP-001-identidad-y-perfil]]; relacionadas: [[HU-002-registrar-usuario]], [[HU-007-gestionar-eps]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** requiere seed, modelo 3FN y acceso coherente.
## Tareas de desarrollo
- [ ] **T-01 — Modelar catálogos y claves.** Dificultad: Medio. Justificar 3FN, únicos y relaciones.
- [ ] **T-02 — Exponer consumo de solo lectura.** Dificultad: Medio. Documentar contrato REST y vista del frontend elegido.
- [ ] **T-03 — Probar valores iniciales.** Dificultad: Bajo. Verificar seed y no mutabilidad.
## Criterios de aceptación
### CA-01 — Valores requeridos
**Dado** el sistema inicializado, **cuando** se consultan catálogos fijos, **entonces** existen roles, estados, regímenes y las dos sedes del PRD.
### CA-02 — Solo lectura
**Dado** un consumidor autorizado o público según contrato, **cuando** intenta alterar un catálogo fijo, **entonces** la operación no está disponible.
## Definition of Done
- [ ] CA-01 y CA-02 validados con evidencia.
- [ ] Seed/migración Flyway y justificación 3FN verificables.
- [ ] Contrato REST y trazabilidad Scrum actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

