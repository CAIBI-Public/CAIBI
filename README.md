# CAIBI Public Catalogue

Public catalogue, source references, schemas and community contribution material for CAIBI.

CAIBI separates evidence into three voices:

- **SOURCE**: what the original project, creator, manufacturer or documentation says.
- **CAIBI**: CAIBI's current synthesis and assessment.
- **BUILDERS**: approved evidence from people who attempted or completed the build.

This repository is for intentionally public catalogue and community material. It is not an application source repository.

## Current state

The v1 public data contract is now defined. Machine-readable schemas are published under `schema/`.

The first generated catalogue dataset will be published only from the validated allowlisted export. Builder evidence will remain empty until its moderation, rights and media-safety publication gates are connected.

## Structure

```text
schema/
  project-v1.schema.json
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
