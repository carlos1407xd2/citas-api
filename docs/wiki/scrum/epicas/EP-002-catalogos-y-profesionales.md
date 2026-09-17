---
id: EP-002
tipo: epica
titulo: Catálogos y profesionales
estado: Borrador
historias: ["[[HU-007-gestionar-eps]]", "[[HU-008-gestionar-planes-eps]]", "[[HU-009-gestionar-especialidades]]", "[[HU-010-crear-y-activar-profesionales]]", "[[HU-011-asignar-especialidades-profesional]]", "[[HU-012-asignar-sedes-profesional]]"]
dependencias: ["[[EP-001-identidad-y-perfil]]"]
---
# EP-002 — Catálogos y profesionales
## Objetivo
Permitir a ADMIN configurar la oferta y habilitar profesionales sintéticos.
## Valor esperado
Datos normalizados y configurables que hacen reservable la oferta asistencial.
## Actores
- ADMIN
## Alcance
- EPS, planes, especialidades, profesionales y sus relaciones N:M.
## Fuera de alcance
- Borrado físico de catálogos referenciados.
## Reglas de negocio
- Especialidad tiene duración 30/60 min; profesional puede tener primaria y una o ambas sedes.
## Dependencias
- [[EP-001-identidad-y-perfil]]
## Historias de usuario
- [[HU-007-gestionar-eps]]
- [[HU-008-gestionar-planes-eps]]
- [[HU-009-gestionar-especialidades]]
- [[HU-010-crear-y-activar-profesionales]]
- [[HU-011-asignar-especialidades-profesional]]
- [[HU-012-asignar-sedes-profesional]]
## Criterio de completitud de la épica
- [ ] Oferta activa, consistente y no duplicada disponible para las épicas dependientes.
## Riesgos e incógnitas
- Definir constraints e índices de relaciones N:M en el modelo 3FN.
