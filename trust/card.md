# AI TrustBOM system card

> **draft (unapproved)**

## Identity

- **System:** vendor-service
- **Repository:** `vendor-service`
- **Commit:** `d7b48ccb4b26924b128ffc915c831a18f5f731e4`
- **Graph fingerprint:** `8e478971e534`
- **Full fingerprint (SHA-256):** `8e478971e5342d1e1c442287c245561de7add4db2380a27422acd75a775bd5e6`
- **CLI version:** `1.0.0`
- **Description:** Disposable AI TrustBOM manual-test vendor service
- **Customer-facing name:** Vendor Service

## Draft classification

- **Role:** `unknown`
- **GPAI provider:** `false`
- **High risk:** `unknown`
- **Article 50:** `unknown`

## Models

| Provider | Model | Region | Endpoint | Source | Cite |
|---|---|---|---|---|---|
| anthropic | claude-sonnet-4-5 | eu-central-1 | unknown | manual | `trust/manual.yml:5` |

## Declared subprocessors

| Provider | Party | Purpose | Location | DPA path | Cite |
|---|---|---|---|---|---|
| anthropic | Anthropic | Synthetic model inference | Ireland | trust/dpas/anthropic.txt | `trust/dpas/anthropic.txt`<br>`trust/subprocessors.yml:2` |

## Data handling

Trust declares, for each AI provider used by this system, how long prompts and customer data are retained, whether that data is used to train provider models, and how deletion is requested. AI TrustBOM does not read, fetch or verify provider terms. "unknown" means Trust has not declared the value; it is not a statement that data is retained, used for training, or safe.

| Provider | Prompt retention | Training use | Deletion path | Source | Cite |
|---|---|---|---|---|---|
| anthropic | 30 days | not used for training | trust/deletion-anthropic.md | manual | `trust/deletion-anthropic.md:1`<br>`trust/dpas/anthropic.txt:1`<br>`trust/manual.yml:21` |

## Tools

| Name | Effect | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## MCP servers

| Name | Connection | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Declared data

| Class | Sent to model | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Declared controls

| Control | Value | Source | Cite |
|---|---|---|---|
| human_send_required | true | manual | `trust/manual.yml:14` |
| kill_switch | true | manual | `trust/manual.yml:17` |
| prompt_bodies_stored | false | manual | `trust/manual.yml:11` |

## Evaluation gates

| Name | Path | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Findings

| ID | Severity | Message | Cite |
|---|---|---|---|
| none | info | No open scan findings. | none |

## Coverage statement

This card describes only what AI TrustBOM detected in tracked repository files and what Trust declared manually. It does not establish that other AI use is absent: files, ecosystems and runtime behaviour outside the method below may contain AI use that was not detected.

**Detector packs used:**

- assist-dotnet 1.0.0
- assist-go 1.0.0
- assist-java 1.0.0
- assist-js 1.7.0
- assist-python 1.4.0
- data-processing 1.0.0
- raw-http 1.0.0

**Ecosystems found with detector support:**

- None found

**Ecosystems found without detector support (AI use unknown):**

- None found

**Not in scope (excluded by Trust):**

- None declared

**Method limits:**

- Models, regions and endpoints are matched only in allowlisted configuration files by detector-pack patterns.
- Ecosystems are recognised from manifest and lockfile names only.
- Source code is not parsed; there is no AST or call-graph analysis.
- Runtime behaviour, network traffic and deployed infrastructure are not inspected.
- Only files tracked in Git at the scanned commit are read.

Ecosystems are recognised from tracked manifest and lockfile names only; an ecosystem without a recognised manifest or lockfile is not listed.

## Generated from

Commit `d7b48ccb4b26924b128ffc915c831a18f5f731e4` using AI TrustBOM CLI `1.0.0`.

## Gate assessment

- **Status:** bootstrap required
- **Summary:** The gate is blocked because this repository has no reviewed graph approval.

### Semantic changes

No semantic graph changes are available.

### Required actions

#### No approval file exists

AI TrustBOM could not find trust/approvals.yml. The first graph must be reviewed by Trust before it can become the baseline.

Choose the appropriate resolution:

- Review the generated system card and repository evidence.
- Create trust/approvals.yml from the template below and complete every human-owned value.
- Request the configured Trust or CODEOWNER review; check the full graph before approving its fingerprint.

Example:

```yaml
approved_graph_sha: 8e478971e5342d1e1c442287c245561de7add4db2380a27422acd75a775bd5e6
approved_by: <Trust reviewer>
approved_at: <ISO-8601 timestamp>
high_risk: unset
article_50: unset
```

### Next step

Have Trust review graph fingerprint 8e478971e534 and commit trust/approvals.yml. Copy the full fingerprint from the approval template above.

