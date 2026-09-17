---
id: EP-004
tipo: epica
titulo: Reserva y ciclo de cita
estado: Borrador
historias: ["[[HU-016-consultar-disponibilidad]]", "[[HU-017-reservar-cita-general]]", "[[HU-018-solicitar-cita-especializada]]", "[[HU-021-consultar-mis-citas]]", "[[HU-022-cancelar-cita]]", "[[HU-023-solicitar-reprogramacion]]"]
dependencias: ["[[EP-001-identidad-y-perfil]]", "[[EP-002-catalogos-y-profesionales]]", "[[EP-003-disponibilidad-profesional]]"]
---
# EP-004 — Reserva y ciclo de cita
## Objetivo
Permitir que USER busque, reserve y administre sus citas sin doble reserva.
## Valor esperado
Autogestión segura de la cita general y especializada.
## Actores
- USER
## Alcance
- Consulta, reserva, detalle, cancelación y solicitud de reprogramación.
## Fuera de alcance
- Cambio de profesional durante reprogramación.
## Reglas de negocio
- RN-01, RN-02, RN-05, RN-08, RN-09 y RN-10.
## Dependencias
- [[EP-001-identidad-y-perfil]], [[EP-002-catalogos-y-profesionales]], [[EP-003-disponibilidad-profesional]]
## Historias de usuario
- [[HU-016-consultar-disponibilidad]]
- [[HU-017-reservar-cita-general]]
- [[HU-018-solicitar-cita-especializada]]
- [[HU-021-consultar-mis-citas]]
- [[HU-022-cancelar-cita]]
- [[HU-023-solicitar-reprogramacion]]
## Criterio de completitud de la épica
- [ ] El ciclo USER conserva integridad de slots, estados e historial.
## Riesgos e incógnitas
- La transacción/constraint exacta para doble reserva queda por diseñar en HU aprobadas.
