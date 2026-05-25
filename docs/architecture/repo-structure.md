# Repo Structure

Estructura real actual del repositorio.

```text
/
|- AGENTS.md
|- CLAUDE.md
|- CONTEXT-MAP.md
|- ERS - Grupo 2 - UMBRAL (5).md
|- docs/
|  |- agents/
|  |- architecture/
|  `- product/
|- src/
|  |- mission-design/
|  |- session-operations/
|  |- scoring-audit/
|  `- identity-access/
`- .agents/
   `- skills/
```

## Convenciones

- `src/` describe bounded contexts y lenguaje de dominio, no código de producción todavía.
- `.agents/skills/` contiene skills reutilizables del entorno.
- `docs/agents/` contiene instrucciones cortas para agentes.
- `docs/product/` contiene la versión normalizada del enunciado y sus aclaratorias.
- `docs/architecture/adr/` se reserva para decisiones difíciles de revertir cuando aparezcan.

## No asumir todavía

- No asumir `src/backend`, `src/web` o `src/mobile` hasta que existan.
- No asumir `tests/`, `.github/workflows/` o `docker-compose.yml` como estructura implementada.
- No asumir una forma final del monorepo más allá del mapa de contextos vigente.
