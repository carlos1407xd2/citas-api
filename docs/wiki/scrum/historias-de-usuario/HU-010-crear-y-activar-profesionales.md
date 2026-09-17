---
id: HU-010
tipo: historia-de-usuario
titulo: Crear y activar profesionales
estado: Borrador
epica: "[[EP-002-catalogos-y-profesionales]]"
esfuerzo: Alto
sprint_sugerido: "Incremento 2 — Oferta configurable"
dependencias: ["[[HU-001-catalogos-fijos]]", "[[HU-003-iniciar-sesion]]"]
relacionadas: ["[[HU-011-asignar-especialidades-profesional]]", "[[HU-012-asignar-sedes-profesional]]"]
---
# HU-010 — Crear y activar profesionales
## Historia de usuario
**COMO** ADMIN **QUIERO** crear y activar/desactivar cuentas PROFESSIONAL con su código y matrícula ficticia **PARA** administrar quién puede publicar agenda.
## Alcance
- Usuario PROFESSIONAL, código profesional, matrícula sintética y estado.
## Fuera de alcance
- Autoregistro profesional.
## Reglas de negocio
- Solo ADMIN crea profesionales; datos sintéticos; inactivo no debe ofertarse.
## Dependencias y relaciones
- Épica: [[EP-002-catalogos-y-profesionales]]; depende de [[HU-001-catalogos-fijos]], [[HU-003-iniciar-sesion]]; relacionadas: [[HU-011-asignar-especialidades-profesional]], [[HU-012-asignar-sedes-profesional]].
## Esfuerzo
**Nivel:** Alto. **Justificación:** identidad por rol, datos especializados y activación transversal.
## Tareas de desarrollo
- [ ] **T-01 — Modelar extensión profesional.** Dificultad: Alto. 3FN, únicos de código/matrícula.
- [ ] **T-02 — Implementar gestión exclusiva ADMIN.** Dificultad: Alto. API/UI, hash inicial según política definida.
- [ ] **T-03 — Probar habilitación de acceso/oferta.** Dificultad: Alto. Rol y estado.
## Criterios de aceptación
### CA-01 — Alta profesional
**Dado** ADMIN autenticado y datos ficticios únicos, **cuando** crea un profesional, **entonces** queda con rol PROFESSIONAL, código y matrícula.
### CA-02 — Activación
**Dado** profesional existente, **cuando** ADMIN lo activa o desactiva, **entonces** su estado se actualiza y se respeta en capacidades posteriores.
### CA-03 — Protección
**Dado** actor no ADMIN, **cuando** intenta crear o activar un profesional, **entonces** se rechaza.
## Definition of Done
- [ ] CA-01 a CA-03 validados.
- [ ] Migración/únicos, roles, estado y pruebas de autorización evidenciados.
- [ ] Contrato/UI y trazabilidad actualizados.
## Evidencia de validación
| Elemento | Resultado | Evidencia | Observación |
|---|---|---|---|
| CA-01 | Pendiente | — | — |
| CA-02 | Pendiente | — | — |
| CA-03 | Pendiente | — | — |
| DoD | Pendiente | — | — |
## Historial de validación
- 2026-09-17 — Creada en `Borrador`.

