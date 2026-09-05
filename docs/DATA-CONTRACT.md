# CAIBI Public Data Contract

Project dataset: **v2.0**  
Builder-evidence dataset: **v1.0**

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

## Public project data v2

The project dataset may contain:

- stable project slug and name;
- category, summary and public tags;
- original public source reference;
- pipeline stage;
- concise CAIBI assessment fields for assessed projects;
- reviewed project cost guidance;
- reviewed build-vs-buy classification and comparison sources where a comparison is defensible;
- evidence status and last-checked information;
- reviewed public supporting resources;
- approved public media references where publication rights are established.

Discovery records may be published before full assessment, but they must not expose a CAIBI assessment, cost guidance or build-vs-buy block until they are actually assessed.

See `../schema/project-v2.schema.json` for the current machine-readable definition. `project-v1.schema.json` remains published as the historical v1 contract.

## Cost guidance

Every assessed project in v2 carries a `costGuidance` block. CAIBI distinguishes:

- **Source cost**: a creator/source total or a source-backed partial total;
- **CAIBI estimate**: an estimate assembled by CAIBI from current representative parts or services;
- **Planning cost**: a broader range where configuration, scale or local fabrication materially changes the result.

The block also carries confidence, checked date, explanation, inclusions and exclusions. A CAIBI estimate must not be presented as a creator-published fact.

## Build versus buy

Every assessed project in v2 carries a `buildVsBuy` classification. The status is one of:

- `priced`;
- `incomplete`;
- `no-close-equivalent`;
- `not-like-for-like`.

A cash difference is published only when CAIBI has a defensible bought reference and priced comparison. Where the comparison is incomplete or misleading, the public record says so instead of inventing a saving.

Cash differences are not expected-cost claims. Time, owned tools, shipping, failure risk and builder-specific changes remain separate unless genuine evidence supports them.

## Public builder evidence

Builder evidence remains a separate v1 dataset. It is never copied directly from raw submissions.

Before a builder report may be public:

1. it must pass moderation;
2. any display name or region must have been supplied for publication;
3. private contact details must be removed;
4. media rights must be confirmed;
5. media safety scanning must pass;
6. no moderation, fingerprint, queue or risk metadata may be exported.

Until those publication gates are satisfied for genuine submissions, the public builder-evidence dataset remains empty.

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

## Export envelopes

Current project dataset:

```json
{
  "contractVersion": "2.0",
  "generatedAt": "2026-09-05T00:00:00.000Z",
  "records": []
}
```

Builder evidence remains:

```json
{
  "contractVersion": "1.0",
  "generatedAt": "2026-09-05T00:00:00.000Z",
  "records": []
}
```

`generatedAt` records when the public artefact was generated. It is separate from source freshness, cost `checkedOn` dates and comparison `checkedOn` dates.

Unknown values remain unknown. They are not filled merely to make records look complete.

## Assessment summary

An assessed public project may expose:

- verdict;
- concise reason;
- legacy source cost text;
- structured cost guidance with provenance label and assumptions;
- build-vs-buy classification and, where defensible, bought reference and cash difference;
- time;
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

Project v2 is a deliberate major-version change because it adds a new reviewed public class of assessment data: structured cost basis and build-vs-buy comparison.

Within v2, compatible changes may add optional fields, add records or correct values without changing the meaning of existing fields. A new major project-contract version is required to remove or rename existing fields, change their meaning or type, merge the three evidence voices, or expose another previously private class of data.
