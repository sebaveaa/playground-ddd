# Repo Structure

Estructura real actual del repositorio.

```text
/
|- .env.example
|- docker-compose.yml
|- docker-compose.dev.yml
|- docker-compose.utils.yml
|- infra/
|  |- keycloak/
|  `- postgres/
|- docs/
|  |- agents/
|  |- architecture/
|  `- product/
|- src/
|  |- edge-proxy/
|  |- mission-design/
|  |- session-operations/
|  |- scoring-audit/
|  `- identity-access/
`- .agents/
   `- skills/
```

## Convenciones

- `src/*/CONTEXT.md` mantiene el lenguaje de dominio por bounded context.
- `src/edge-proxy/` contiene el borde tecnico minimo para exponer entrada unificada sin meter logica de dominio.
- `src/*/service/` contiene esqueletos tecnicos iniciales de microservicios `.NET`.
- `infra/` agrupa bootstrap operativo local como `Keycloak` y scripts de `PostgreSQL`.
- `docker-compose.dev.yml` levanta el entorno de desarrollo distribuido.
- `docker-compose.utils.yml` levanta contenedores utilitarios para scaffolding y tareas de plantilla.
- `.agents/skills/` contiene skills reutilizables del entorno.
- `docs/agents/` contiene instrucciones cortas para agentes.
- `docs/product/` contiene la version normalizada del enunciado y sus aclaratorias.
- `docs/architecture/adr/` contiene decisiones dificiles de revertir.

## No asumir todavia

- No asumir que `web` o `mobile` ya existen en este repo.
- No asumir que los esqueletos `.NET` ya compilan localmente sin instalar SDK o restaurar paquetes.
- No asumir pipelines de `CI/CD` o tests automatizados hasta que se agreguen explicitamente.
