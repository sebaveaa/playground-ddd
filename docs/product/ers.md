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
- Separación CQRS implementada con `MediatR`.
- `CQRS` se aplica a nivel lógico de comandos y consultas, sin separar bases de datos de escritura y lectura.
- Persistencia relacional.
- Comunicación en tiempo real implementada con `SignalR`.
- Mensajería asíncrona.
- Roles `Administrator`, `Operator` y `Participant`.
- Identidad y acceso gestionados con `Keycloak`.
- Autenticación basada en tokens `JWT` emitidos por `Keycloak`.
- Autorización basada en roles y permisos definidos en `Keycloak` y consumidos desde los claims del token.
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

## Decisiones aclaradas del ERS

### Trivia

- La validación de respuestas de `Trivia` ocurre automáticamente por defecto.
- El `Operator` puede corregir el resultado cuando detecte que la respuesta enviada corresponde a una alternativa válida.
- No debe modelarse `Trivia` como un flujo donde toda evidencia entra primero en estado `Pending` para revisión humana obligatoria.

## Uso esperado

Este archivo resume el ERS para trabajo diario. El documento raíz sigue siendo la referencia académica completa.
