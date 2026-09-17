---
id: HU-007
tipo: historia-de-usuario
titulo: Gestionar EPS
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Medio
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-003-iniciar-sesion]]"]
relacionadas: ["[[HU-008-gestionar-planes-eps]]", "[[HU-006-gestionar-perfil-y-afiliacion]]"]
---
# HU-007 — Gestionar EPS
## Historia de usuario
**COMO** ADMIN **QUIERO** crear, consultar, actualizar y desactivar EPS **PARA** administrar opciones de afiliación sin perder referencias históricas.
## Alcance
- CRUD de EPS con activación/desactivación.
## Fuera de alcance
- Borrado físico de una EPS referenciada.
## Reglas de negocio
- Catálogo configurable; referencias transaccionales se conservan.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-003-iniciar-sesion]]; relacionadas: [[HU-008-gestionar-planes-eps]], [[HU-006-gestionar-perfil-y-afiliacion]].
## Esfuerzo
**Nivel:** Medio. **Justificación:** CRUD protegido, estado lógico y FK.
## Tareas de desarrollo
- [ ] **T-01 — Modelar EPS 3FN y estado.** Dificultad: Medio. Migración/constraints.
- [ ] **T-02 — Exponer gestión exclusiva ADMIN.** Dificultad: Medio. API, UI y validación.
- [ ] **T-03 — Probar desactivación referenciada.** Dificultad: Medio. Integridad y autorización.
## Criterios de aceptación
### CA-01 — Gestión ADMIN
**Dado** ADMIN autenticado, **cuando** crea o actualiza una EPS válida, **entonces** queda disponible con datos consistentes.
### CA-02 — Desactivación segura
**Dado** EPS referenciada, **cuando** ADMIN intenta retirarla, **entonces** puede desactivarla y no se borra físicamente.
### CA-03 — Protección de rol
**Dado** USER o PROFESSIONAL, **cuando** intenta gestionar EPS, **entonces** la operación es rechazada.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Migración/FK y estado lógico evidenciados.
- [ ] Contrato REST, UI y pruebas aplicables registrados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

