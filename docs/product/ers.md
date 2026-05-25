# ERS Normalizado

Documento operativo derivado de [../../ERS - Grupo 2 - UMBRAL (5).md](../../ERS%20-%20Grupo%202%20-%20UMBRAL%20(5).md) para consumo de agentes.

## Propósito

UMBRAL es una plataforma para operar experiencias narrativas inmersivas en tiempo real con dos tipos de juego:

- `Treasure Hunt`
- `Trivia`

Existen dos superficies principales:

- web para `Administrator` y `Operator`
- móvil para `Participant`

## Decisiones estables del enunciado

- Arquitectura limpia o hexagonal.
- Separación CQRS.
- Persistencia relacional.
- Comunicación en tiempo real.
- Mensajería asíncrona.
- Roles `Administrator`, `Operator` y `Participant`.
- La experiencia del participante ocurre en móvil.
- El diseño reusable de la misión está separado de la operación en vivo.

## Bounded contexts esperados

- `Mission Design`
- `Session Operations`
- `Scoring and Audit`
- `Identity and Access`

## Reglas de negocio transversales

- Una misión debe estar activa para usarse en sesiones.
- Una sesión no inicia sin equipos registrados.
- No se aceptan evidencias en sesión pausada, finalizada o cancelada.
- Las etapas progresan de forma lineal por equipo.
- El ranking se ordena por puntaje y desempata por tiempo de resolución.
- Las penalizaciones deben registrar motivo y momento.
- Al finalizar la sesión se revelan pistas y soluciones.

## Ambigüedades abiertas del ERS

### Trivia

El enunciado mezcla dos formulaciones:

- validación automática con intervención manual solo en casos ambiguos
- validación manual por operador tras registrar respuesta pendiente

Hasta que esto se cierre, los agentes deben tratarlo como contradicción del enunciado y no como una verdad resuelta.

## Uso esperado

Este archivo resume el ERS para trabajo diario. El documento raíz sigue siendo la referencia académica completa.
