# CAIBI Public Data Contract v1

Status: **stable for first public export**.

This repository contains intentionally public catalogue and community material. The contract is deliberately narrower than the application model. A field existing elsewhere does not make it public here.

## Evidence voices

CAIBI keeps three evidence voices separate.

### SOURCE

What the original project, creator, manufacturer or documentation says.

### CAIBI

CAIBI's current synthesis and assessment.

### BUILDERS

Approved reports from people who attempted or completed the build.

A public record should make the voice of a statement explicit rather than requiring readers to infer it.

## Public project data

The v1 project dataset may contain:

- stable project slug and name;
- category, summary and public tags;
- original public source reference;
- pipeline stage;
- concise CAIBI assessment fields for assessed projects;
- evidence status and last-checked information;
- reviewed public supporting resources;
- approved public media references where publication rights are established.

Discovery records may be published before full assessment, but they must not expose a CAIBI assessment block until they are actually assessed.

See `../schema/project-v1.schema.json` for the machine-readable definition.

## Public builder evidence

Builder evidence is a separate dataset. It is never copied directly from raw submissions.

Before a builder report may be public:

1. it must pass moderation;
2. any display name or region must have been supplied for publication;
3. private contact details must be removed;
4. media rights must be confirmed;
5. media safety scanning must pass;
6. no moderation, fingerprint, queue or risk metadata may be exported.

Until those publication gates are connected, the public builder-evidence dataset remains empty.

See `../schema/builder-evidence-v1.schema.json` for the machine-readable definition.

## What is not public data

This repository must not contain:

- application source code or deployment configuration;
- environment variables, credentials or infrastructure details;
- moderation rules, thresholds, fingerprints or queue internals;
- private working notes;
- submitter email addresses or private contact information;
- private analytics or account data;
- raw uploaded media before rights and safety checks;
- private backend identifiers where a public stable identifier is sufficient.

## Export envelope

Generated datasets use this envelope:

```json
{
  "contractVersion": "1.0",
  "generatedAt": "2026-08-29T00:00:00.000Z",
  "records": []
}
```

`generatedAt` records when the public artefact was generated. It is separate from source freshness or assessment `checkedOn` dates.

Unknown values remain unknown. They are not filled merely to make records look complete.

## Assessment summary

An assessed public project may expose:

- verdict;
- concise reason;
- cost and time where known;
- difficulty and AI leverage on the public CAIBI scales;
- evidence status;
- AI CAN HELP;
- AI CAN'T DO;
- the main physical catch;
- checked date where available.

The public reason explains the judgement. It does not expose private implementation or derivation logic.

## Corrections and contributions

A correction or contribution should identify:

- the affected project slug or public record;
- the field or claim being challenged or improved;
- a public source or firsthand builder basis where relevant;
- whether the contribution concerns SOURCE, CAIBI or BUILDERS evidence.

A contribution never automatically changes a CAIBI verdict. Material contradictions trigger editorial review.

See `CONTRIBUTING.md` for the contribution route.

## Versioning

A v1-compatible change may add optional fields, add records or correct values without changing the meaning of existing fields.

A new major contract version is required to remove or rename existing fields, change their meaning or type, merge the three evidence voices, or expose a previously private class of data.
