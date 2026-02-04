# Solution Framing (UX-led, IA-assisted)

## Scope
Topics covered: TOP 3 from Insight Analysis  
1. Patient summary visibility  
2. Pediatric data prominence  
3. Cognitive load

---

## Topic 1: Patient Summary Visibility

### Problem recap
Users struggle to immediately access and interpret the patient summary, impacting their ability to quickly understand patient status at the start of a consultation.

### Solution directions

#### 1. Synthesis Panel Emphasis
- **Description:** Visually elevate the patient summary/synthesis panel (e.g., larger font, color accent, fixed position at top of patient record).
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary component can be visually modified without backend/API changes.
- **Risks / open questions:** May reduce space for other elements; risk of visual clutter if not carefully balanced.
- **What should be validated:** Quick comprehension in 5-second tests; visual hierarchy effectiveness.

#### 2. Progressive Disclosure for Details
- **Description:** Default to a concise summary view, with a clear “expand for details” affordance for less critical data.
- **Impacted moment:** Dossier opening, throughout consultation
- **Products impacted:** Both
- **Assumptions:** Existing summary widget supports collapsible/expandable sections.
- **Risks / open questions:** Users may miss hidden details; needs careful default content selection.
- **What should be validated:** Usability of expand/collapse; user trust in default view.

#### 3. Contextual Highlighting of Key Signals
- **Description:** Use subtle highlights (e.g., badges, icons) for critical signals (alerts, recent changes) within the summary.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both
- **Assumptions:** Can reuse existing badge/icon components; no new data fields required.
- **Risks / open questions:** Highlighting too many items may dilute impact.
- **What should be validated:** Clarity of highlighted signals; avoidance of alert fatigue.

---

## Topic 2: Pediatric Data Prominence

### Problem recap
Pediatricians in Libellia cannot easily identify growth, development, and vaccination data, which are clinically critical for children.

### Solution directions

#### 1. Pediatric Signal Row
- **Description:** Add a dedicated, visually distinct row or section for pediatric signals (growth, development, vaccination) at the top of the patient summary.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia (France) only
- **Assumptions:** Data already available in summary; can be rearranged in UI.
- **Risks / open questions:** May require minor UI adaptation; risk of crowding if not well designed.
- **What should be validated:** Pediatrician ability to spot key signals instantly.

#### 2. Pediatric-Specific Icons/Badges
- **Description:** Use pediatric-specific icons or color-coded badges to visually differentiate child-specific data within the summary.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia only
- **Assumptions:** Existing icon/badge library is sufficient.
- **Risks / open questions:** Icon meaning must be clear; risk of inconsistency if not standardized.
- **What should be validated:** Recognition and interpretation of pediatric markers.

#### 3. Default Pediatric View for Child Patients
- **Description:** Automatically present a pediatric-focused summary layout when the patient is under a certain age, without requiring user configuration.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia only
- **Assumptions:** Patient age is reliably available; summary layout can be conditionally rendered.
- **Risks / open questions:** Edge cases (e.g., adolescents); technical feasibility of conditional layouts.
- **What should be validated:** Correct triggering of pediatric view; user acceptance.

---

## Topic 3: Cognitive Load

### Problem recap
The current patient record and consultation views in Libellia present too much information at once, increasing cognitive load and slowing down pediatricians.

### Solution directions

#### 1. Information Grouping & Collapsing
- **Description:** Group related information (e.g., administrative, clinical, pediatric) and collapse non-critical sections by default.
- **Impacted moment:** Dossier opening, consultation workflow
- **Products impacted:** Libellia only
- **Assumptions:** UI supports collapsible sections; grouping can be done without backend changes.
- **Risks / open questions:** Users may overlook collapsed sections; grouping logic must match clinical priorities.
- **What should be validated:** Speed of finding key info; user comfort with collapsed sections.

#### 2. Visual Hierarchy Enhancement
- **Description:** Adjust font sizes, weights, and spacing to make the most important data stand out, reducing the need to scan dense screens.
- **Impacted moment:** Dossier opening, consultation workflow
- **Products impacted:** Libellia only
- **Assumptions:** Can be achieved via frontend style updates.
- **Risks / open questions:** Overemphasis may cause other data to be missed.
- **What should be validated:** 5-second comprehension tests; user feedback on readability.

#### 3. Quick Access Shortcuts
- **Description:** Add shortcut buttons or links to jump directly to the most-used pediatric sections (e.g., growth charts, vaccination).
- **Impacted moment:** Consultation workflow
- **Products impacted:** Libellia only
- **Assumptions:** Existing navigation can support anchor links or shortcuts.
- **Risks / open questions:** May add minor visual complexity; shortcut placement must be intuitive.
- **What should be validated:** Frequency of shortcut use; impact on workflow speed.

---

## Cross-topic considerations

- **Shared patterns:** Visual hierarchy, badges, and progressive disclosure are relevant across all topics.
- **Platform implications:** Patient summary visibility improvements can be NAIS-level; pediatric prominence and cognitive load solutions are Libellia-specific due to FR pediatric focus.
- **Sequencing / dependency notes:** Patient summary visibility changes should precede pediatric-specific enhancements to avoid rework; visual hierarchy updates can be applied in parallel.

---

## What the human team must decide

- Which summary enhancement(s) to prioritize for both Libellia and Studio, given shared platform constraints.
- Preferred approach for pediatric data prominence (dedicated row, icons, or default view), balancing clarity and UI simplicity.
- Acceptable level of information collapsing/grouping to reduce cognitive load without hiding critical data.
- Validation plan: which solutions to prototype/test first, and with which user segments.
- Any technical feasibility checks needed for conditional layouts