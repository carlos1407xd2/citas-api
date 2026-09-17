---
tipo: indice-scrum
estado: Borrador
---

# Mapa Scrum / Spec-Driven Development — Citas FCV

## Alcance y convenciones

Este mapa deriva exclusivamente de `PRD.md`, `RESTRICCIONES_TECNICAS.md` y `database/REQUISITOS_NORMALIZACION_3FN.md`. Todas las HU están en **Borrador** y requieren revisión explícita antes de poder pasar a `Aprobada`.

Stack constatado: backend objetivo Java 21 / Spring Boot 3.5.x / Maven / MySQL 8.4 / Flyway / REST JSON; frontend TypeScript con **React o Angular aún no seleccionado**, sin Express ni BFF. El frontend consumirá directamente la API REST.

## Épicas

- [[EP-001-identidad-y-perfil]] — acceso, sesión y afiliación.
- [[EP-002-catalogos-y-profesionales]] — catálogos y capacidad profesional.
- [[EP-003-disponibilidad-profesional]] — bloques y agenda publicable.
- [[EP-004-reserva-y-ciclo-de-cita]] — disponibilidad, reserva y ciclo USER.
- [[EP-005-gestion-administrativa]] — decisiones administrativas.
- [[EP-006-atencion-y-auditoria]] — atención y trazabilidad de estados.
- [[EP-007-integracion-y-calidad-del-incremento]] — contrato REST verificable por incremento.

## Incrementos / sprints sugeridos

| Incremento | Resultado comprobable | HU en orden |
|---|---|---|
| Incremento 1 — Acceso seguro | Un USER puede registrarse, gestionar sesión, recuperar acceso y mantener perfil/afiliación. | [[HU-001-catalogos-fijos]], [[HU-002-registrar-usuario]], [[HU-003-iniciar-sesion]], [[HU-004-renovar-y-cerrar-sesion]], [[HU-005-recuperar-contrasena]], [[HU-006-gestionar-perfil-y-afiliacion]] |
| Incremento 2 — Oferta configurable | ADMIN configura catálogos y deja profesionales habilitados y asignados. | [[HU-007-gestionar-eps]], [[HU-008-gestionar-planes-eps]], [[HU-009-gestionar-especialidades]], [[HU-010-crear-y-activar-profesionales]], [[HU-011-asignar-especialidades-profesional]], [[HU-012-asignar-sedes-profesional]] |
| Incremento 3 — Agenda publicable | PROFESSIONAL publica y consulta bloques válidos en sus sedes. | [[HU-013-crear-bloques-disponibilidad]], [[HU-014-modificar-bloques-futuros]], [[HU-015-consultar-calendario-profesional]] |
| Incremento 4 — Cita general | USER encuentra un horario válido y confirma una cita general aprobada. | [[HU-016-consultar-disponibilidad]], [[HU-017-reservar-cita-general]], [[HU-028-contrato-rest-incremento]] |
| Incremento 5 — Cita especializada | USER solicita cita especializada y ADMIN decide con reserva consistente. | [[HU-018-solicitar-cita-especializada]], [[HU-019-decidir-cita-especializada]], [[HU-020-consultar-bandeja-administrativa]] |
| Incremento 6 — Ciclo del usuario | USER consulta, cancela y solicita reprogramaciones sin perder la cita original. | [[HU-021-consultar-mis-citas]], [[HU-022-cancelar-cita]], [[HU-023-solicitar-reprogramacion]], [[HU-024-decidir-reprogramacion]] |
| Incremento 7 — Atención trazable | PROFESSIONAL consulta agenda, cierra atención y el sistema conserva auditoría. | [[HU-025-consultar-agenda-profesional]], [[HU-026-cerrar-atencion]], [[HU-027-consultar-auditoria-estados]] |

## Decisiones e incógnitas pendientes

- Seleccionar React o Angular después del diseño aprobado en Stitch/AI Studio.
- Diseñar y documentar el contrato REST por HU aprobada; no se fijan endpoints ni DTOs antes de esa aprobación.
- Definir en el diseño de datos la estrategia concreta de restricción/concurrencia para RN-01, manteniendo 3FN, slots consecutivos y reservas retenidas.
- El correo de recuperación puede ser simulado de forma segura en desarrollo; SMTP no es obligatorio.
