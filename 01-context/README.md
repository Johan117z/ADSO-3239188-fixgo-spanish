# 01 — Project Context

> **What is this?** The "why" of the system. Anyone new must be able to read this
> folder and understand what problem the project solves, what it includes, and what it does NOT include.

## Why this section exists

Before designing anything, the team needs to agree on:
- What problem are we solving?
- For whom?
- What is in scope and what is out of scope?
- What does each term we use mean?

Without this, each team member works with different assumptions and the project fragments.

---

## What is here and how to fill it in

### `overview.md` ⭐
Executive description of the system in maximum 1 page.
**Fill in:** system name, problem it solves, main users, key technologies,
current status (under construction / in production / legacy).

**Suggested format:**
```markdown
## What is [FixGO]?
[FixGo es una plataforma móvil en tiempo real diseñada para conectar instantáneamente a los conductores varados con talleres mecánicos y de asistencia en carretera cercanos. Agiliza las reparaciones vehiculares de emergencia al ofrecer una coincidencia precisa de geolocalización y un manejo seguro de solicitudes digitales.]

## Problem it solves
[Los conductores que experimentan  fallas  mecánicas inesperadas se enfrentan a graves retrasos, carecen de formas fiables de encontrar talleres abiertos cercanos y tienen dificultades para obtener rápidamente asistencia en carretera confiable. Los mecánicos también pierden clientes locales debido a la mala visibilidad digital y al envío manual ineficiente.]

## Main users
- [Conductores]: [Solicite asistencia en carretera inmediata, realice un seguimiento de la ubicación del mecánico en tiempo real y administre perfiles de servicio.]
- [Mecánica]: [Reciba solicitudes de servicios de emergencia, acepte trabajos basados en la proximidad y administre ofertas de diagnóstico en el sitio.]

## Technology stack
- Backend: [Java/maven]
- Database: [Base de datos en tiempo real Firebase / SQL]
- Infrastructure: [Implementación basada en la nube con estándares de seguridad AES-256]
```

### `scope.md` ⭐
System boundaries: what it does and what it does NOT do.
**Fill in:** explicit list of what is INSIDE and OUTSIDE the MVP scope and future versions.
This prevents scope creep (the system that grows without control).

**Format:**
```markdown
## In scope (MVP)
- [Registro de perfiles de conductores y mecánicos con Firebase authentication. ]
- [Rastreo de geolocalización en tiempo real con un objetivo de precisión de 15 metros.]
- [Emparejamiento automatizado de solicitudes de servicio con un SLA de respuesta de 3 segundos.]
- [Protección de datos del cliente utilizando estándares de cifrado AES-256.]

## Out of scope (MVP)
- [Procesamiento de pagos dentro de la aplicación y transacciones financieras.]
- [Venta directa de repuestos automotrices o mercancía física.]
- [Contratar o emplear directamente  mecánicos por parte de FixGo.]
- [Provisión de grúas físicas por parte de la plataforma.]

## Candidates for future versions
- [Pasarelas de pago integradas con tarjetas de crédito, billeteras digitales.]
- [Chat dentro de la aplicación y llamadas VoIP entre conductores y mecánicos.]
- [Un sistema de calificación y reseñas de usuarios para mecánicos y talleres.]
- [Reservas de mantenimiento programado y diagnósticos preventivos.]
```

### `glossary.md` ⭐
Dictionary of the project domain.
**Fill in:** all technical and business terms used in the project, with their exact definition.
If two people define "client" differently, the system will have bugs.

**Format:**
```markdown
| Término             | Definición                                                                                    | Sinónimos             | Notas                                                              |
|---------------------|-----------------------------------------------------------------------------------------------|-----------------------|--------------------------------------------------------------------|
| Conductor           | Individuo que sufre una avería y solicita asistencia inmediata.                               | Cliente, Usuario      | Inicia el proceso de emparejamiento.                               |
| Mecánico            | Profesional automotriz que ofrece diagnósticos y servicios de reparación en el sitio.         | Taller, Proveedor     | Debe pasar la verificación del sistema.                            |
| Emparejamiento      | El proceso algorítmico de emparejar la solicitud de un conductor con el mecánico más cercano. | Vinculación, Despacho | Debe cumplir con el SLA de 3 segundos.                             |
| Reparación en sitio | Asistencia mecánica proporcionada directamente en la ubicación de la avería del vehículo.     | Asistencia Vial       | El servicio principal facilitado por FixGo.                        |
| SLA                 | Acuerdo de Nivel de Servicio que define el punto de referencia de rendimiento del sistema.    | Respuesta Objetivo    | Establecido en un máximo de 3 segundos para consultas del sistema. |
```

### `_template-project-profile.md`
Project technical sheet for internal records.
**Fill in:** when the project is formalized (official name, tech lead, dates, stakeholders).

### `_template-scope-declaration.md`
Formal scope declaration template for presentations or deliverables.

---

## Correlations with other sections

| If you change this... | Also review... |
|-----------------------|----------------|
| The problem described in `overview.md` | Product vision in `03-product/vision.md` |
| The scope in `scope.md` | Requirements in `04-requirements/`, PRD in `03-product/` |
| A term in `glossary.md` | Every document where that term appears |

---

## Recommended fill order

1. `overview.md` — 30 minutes with the full team
2. `scope.md` — 1 hour of discussion (the most valuable thing you can do at the start)
3. `glossary.md` — grows throughout the project, start with 10 key terms

---

## Questions this section must answer

- What does this system exist for?
- Who are the users?
- What does the system NOT do?
- What does [term X] mean in this project?
