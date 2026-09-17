---
id: EP-003
tipo: epica
titulo: Disponibilidad profesional
estado: Borrador
historias: ["[[HU-013-crear-bloques-disponibilidad]]", "[[HU-014-modificar-bloques-futuros]]", "[[HU-015-consultar-calendario-profesional]]"]
dependencias: ["[[EP-002-catalogos-y-profesionales]]"]
---
# EP-003 — Disponibilidad profesional
## Objetivo
Permitir que un profesional habilitado publique agenda utilizable.
## Valor esperado
Fuente confiable de slots para reservar citas.
## Actores
- PROFESSIONAL
## Alcance
- Bloques por fecha/sede, edición futura y calendario propio.
## Fuera de alcance
- Aprobación de citas.
## Reglas de negocio
- Sin pasado ni solapamientos; sede asignada; slots de 30 min.
## Dependencias
- [[EP-002-catalogos-y-profesionales]]
## Historias de usuario
- [[HU-013-crear-bloques-disponibilidad]]
- [[HU-014-modificar-bloques-futuros]]
- [[HU-015-consultar-calendario-profesional]]
## Criterio de completitud de la épica
- [ ] Los bloques futuros válidos son consultables y preservan citas comprometidas.
## Riesgos e incógnitas
- Precisar la representación normalizada de slots/bloques y la protección de concurrencia.
