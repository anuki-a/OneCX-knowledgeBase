---
trigger: manual
---

# Knowledge Base Generation Rules

## Purpose
Generate concise product knowledge bases for AI-assisted software development.

## General Principles
* **Business Over UI:** Prefer business understanding over screen descriptions.
* **Workflows Over Navigation:** Prefer workflows over UI navigation.
* **Aggregated Knowledge:** Prefer aggregated knowledge over module documents.
* **Fact-Based Only:** Capture facts only from provided sources.
* **Handle Uncertainty:** If uncertain, create an open question instead of making assumptions.

## Documentation Rules
* **Conciseness:** Keep information concise.
* **De-duplication:** Merge duplicate information and similar workflows.
* **Grouping:** Group workflow variations together.
* **No Implementation Details:** Avoid implementation details unless they affect business behavior.
* **No UI Hand-holding:** Avoid UI click-by-click instructions, screenshots, and screen descriptions.

## Source Traceability
* **Mandatory References:** Every section must contain source references.
* **Original Naming:** Use original filenames.
* **Multi-Source Support:** Multiple sources may be listed.
* **No Inventing:** Never create information without a source.

## Workflow Rules
* **Unified Workflows:** One workflow may contain multiple variations.
* **Alternative Paths:** Alternative paths belong inside the same workflow.
* **Exception Handling:** Exception flows belong inside the same workflow.
* **Approvals:** Approval variations belong inside the same workflow.

## Business Rule Rules
Capture the following elements:
* Validations
* State transitions
* Approval conditions
* Restrictions
* Calculations
* Required conditions

## Question Rules
Create open questions when:
* Information is missing.
* Documents conflict.
* Behavior is unclear.
* Business decisions are not documented.

## Output Rules
* **Strict Scope:** Produce only explicitly requested files. Never create additional, module, feature, or screen documents.
* **Target Audience:** The resulting knowledge base must be understandable by:
  * Developers
  * Architects
  * Business analysts
  * AI coding assistants

