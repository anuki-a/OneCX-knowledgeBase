# Knowledge Base Generation Prompt

## Analyze these sources:
- OneCX.html (inside /raw folder)
- BA training scripts (*.md) (inside /raw folder)

## Goal
Create a lightweight AI coding knowledge base for product understanding. Do NOT document every screen, page, or module. Do NOT create additional files.
create only 3 files: product-overview.md, workflows.md, business-rules-and-questions.md


## Create ONLY these files:

### 1. product-overview.md

**Purpose:** Provide a high-level understanding of the product.

**Include:**
- Product purpose
- Target users or user roles
- Main business areas
- Main feature groups from OneCX.html
- High-level system capabilities
- Relationships between business areas
- Important terminology and definitions

**special instructions:**
- add sources for each item (ex: OneCX.html, BA-Customer-Onboarding.md). - can be multiple sources for each item.

---

### 2. workflows.md

**Purpose:** Describe how the business operates.

**Include:**
- End-to-end business processes
- User journeys
- Operational flows
- Process steps extracted from BA scripts

**Format:**

#### Workflow Name

Purpose: 
Actors: 
Main Flow:
Variations:
 - Alternative paths
 - Exception paths
 - Approval variations
 - Cancelation paths
 - Configuration related paths


**Rules:**
- Keep workflows at business level.
- Avoid UI-level clicks and navigation details.
- Do not create separate workflows for similar processes.
- Combine similar workflows.

---

### 3. business-rules-and-questions.md

**Purpose:** Capture logic that affects system behavior.

**Include:**

#### Business Rules
- Validation rules
- Eligibility rules
- Approval conditions
- Status transitions
- Required fields
- Calculations
- Restrictions

#### Customization
- recognize any Customizations and categorize them by type (tenent customization, workflow customization, role customization, form customization, etc.)

#### Open Questions
- Missing information
- Contradictions between documents
- Ambiguous behavior
- Unknown business decisions
- Areas requiring SME clarification

**Format:**
Question: 
Reason: 
Source:



---

## Additional instructions:
- Use OneCX.html as the primary source for product structure.
- Use BA scripts as the primary source for workflows and rules.
- Remove duplicate information.
- Prefer concise bullet points.
- If uncertain, add a question instead of making assumptions.
- Every section must contain source references.
- Use the original file names as references.
- If information appears in multiple sources, list all sources.
- Prefer summaries over detailed explanations.
- Total knowledge base size should remain small and easy to maintain.
- The result should be understandable by both developers and AI coding assistants.


