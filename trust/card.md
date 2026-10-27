# AI TrustBOM system card

> **draft (unapproved)**

## Identity

- **System:** vendor-service
- **Repository:** `vendor-service`
- **Commit:** `402c56a44fd15e952edacb143bb01e63a884a81a`
- **Graph fingerprint:** `efc2dca15727`
- **Full fingerprint (SHA-256):** `efc2dca157274f8273e09d48771a47604baf0000c3a2f1ea434f551707bdf1e9`
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
| openai | gpt-4o | eu-west-1 | unknown | manual | `trust/manual.yml:9` |

## Declared subprocessors

| Provider | Party | Purpose | Location | DPA path | Cite |
|---|---|---|---|---|---|
| anthropic | Anthropic | Synthetic model inference | Ireland | trust/dpas/anthropic.txt | `trust/dpas/anthropic.txt`<br>`trust/subprocessors.yml:2` |

## Data handling

Trust declares, for each AI provider used by this system, how long prompts and customer data are retained, whether that data is used to train provider models, and how deletion is requested. AI TrustBOM does not read, fetch or verify provider terms. "unknown" means Trust has not declared the value; it is not a statement that data is retained, used for training, or safe.

| Provider | Prompt retention | Training use | Deletion path | Source | Cite |
|---|---|---|---|---|---|
| anthropic | 30 days | not used for training | trust/deletion-anthropic.md | manual | `trust/deletion-anthropic.md:1`<br>`trust/dpas/anthropic.txt:1`<br>`trust/manual.yml:25` |
| openai | unknown | unknown | unknown | undeclared | none |

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
| human_send_required | true | manual | `trust/manual.yml:18` |
| kill_switch | true | manual | `trust/manual.yml:21` |
| prompt_bodies_stored | false | manual | `trust/manual.yml:15` |

## Evaluation gates

| Name | Path | Source | Cite |
|---|---|---|---|
| unknown | unknown | unknown | none |

## Findings

| ID | Severity | Message | Cite |
|---|---|---|---|
| subprocessor-undeclared | medium | Provider 'openai' has no declared subprocessor. | `trust/manual.yml:9` |

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

Commit `402c56a44fd15e952edacb143bb01e63a884a81a` using AI TrustBOM CLI `1.0.0`.

## Gate assessment

- **Status:** failed
- **Summary:** The gate is blocked by 2 conditions.

### Semantic changes

- Added model openai / gpt-4o.
- Added medium finding subprocessor-undeclared.

### Required actions

#### The approved graph does not match this change

Trust approved fingerprint 8e478971e534, but this branch produces efc2dca15727.

Choose the appropriate resolution:

- Revert or correct unintended AI-system changes.
- Add a reasoned manual declaration when repository evidence is incomplete.
- If the changes are intended, have Trust review the semantic changes and complete graph before approving the current fingerprint.

Example:

```yaml
approved_graph_sha: efc2dca157274f8273e09d48771a47604baf0000c3a2f1ea434f551707bdf1e9
```

#### Finding subprocessor-undeclared is not waived

The subprocessor-undeclared finding is medium. This workflow blocks medium or higher, and no active waiver covers it.

Evidence:

- `trust/manual.yml:9`

Choose the appropriate resolution:

- Fix the underlying finding and rerun the scan.
- If Trust accepts the risk temporarily, add or renew a time-bounded waiver with a reason and reviewer.

Example:

```yaml
waivers:
  - finding_id: 'subprocessor-undeclared'
    reason: <why the risk is accepted temporarily>
    until: <yyyy-MM-dd>
    by: <Trust reviewer>
```

### Next step

Resolve every blocking condition below, then rerun AI TrustBOM.

