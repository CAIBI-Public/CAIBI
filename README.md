# CAIBI Public Catalogue

Public catalogue, source references, schemas and community contribution material for CAIBI.

CAIBI separates evidence into three voices:

- **SOURCE**: what the original project, creator, manufacturer or documentation says.
- **CAIBI**: CAIBI's current synthesis and assessment.
- **BUILDERS**: approved evidence from people who attempted or completed the build.

This repository is for intentionally public catalogue and community material. It is not an application source repository.

## Current state

The public **project** dataset uses contract **v2.0**, adding reviewed cost guidance and build-vs-buy classification for assessed projects. Discovery-stage records do not receive assessment or money fields before assessment.

The separate **builder-evidence** dataset remains on contract **v1.0** and remains empty until its moderation, rights and media-safety publication gates are satisfied.

Machine-readable schemas are published under `schema/`. The previous project v1 schema remains available for consumers that need the historical contract definition.

## Structure

```text
schema/
  project-v1.schema.json
  project-v2.schema.json
  builder-evidence-v1.schema.json

data/
  projects.json
  builder-evidence.json

docs/
  DATA-CONTRACT.md
  CONTRIBUTING.md
```

## Contributions

Corrections and evidence are welcome. See `docs/CONTRIBUTING.md` for the distinction between source corrections, CAIBI assessment challenges and builder evidence.

Website: https://caibi.app
