---
id: EP-005
tipo: epica
titulo: Gestión administrativa
estado: Borrador
historias: ["[[HU-019-decidir-cita-especializada]]", "[[HU-020-consultar-bandeja-administrativa]]", "[[HU-024-decidir-reprogramacion]]"]
dependencias: ["[[EP-004-reserva-y-ciclo-de-cita]]"]
---
# EP-005 — Gestión administrativa
## Objetivo
Permitir a ADMIN decidir solicitudes y operar la bandeja.
## Valor esperado
Control explícito de las citas especializadas y reprogramaciones.
## Actores
- ADMIN
## Alcance
- Bandeja, filtros, aprobación/rechazo y motivos.
## Fuera de alcance
- Aprobación de cita general.
## Reglas de negocio
- Rechazo con motivo; liberación/retención coherente de slots.
## Dependencias
- [[EP-004-reserva-y-ciclo-de-cita]]
## Historias de usuario
- [[HU-019-decidir-cita-especializada]]
- [[HU-020-consultar-bandeja-administrativa]]
- [[HU-024-decidir-reprogramacion]]
## Criterio de completitud de la épica
- [ ] Toda decisión administrativa actualiza estados y reservas correctamente.
## Riesgos e incógnitas
- Ninguno adicional a la estrategia de reserva aprobada.
