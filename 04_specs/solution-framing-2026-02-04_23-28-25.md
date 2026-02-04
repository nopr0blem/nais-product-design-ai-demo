# Solution Framing (UX-led, IA-assisted)

## Scope
Topics covered: TOP 3 from Insight Analysis

- patient_summary_visibility (Libellia, Studio, FR, IT)
- pediatric_data_prominence (Libellia, FR)
- cognitive_load (Libellia, FR)

---

## Topic 1: patient_summary_visibility

### Problem recap
Users struggle to quickly locate and interpret the patient summary, impacting their ability to gain an immediate overview at critical workflow moments.

### Solution directions

#### 1. "Summary Card Elevation"
- **Description:** Increase visual prominence of the existing patient summary card at dossier opening and consultation start (e.g., larger card, bolder header, slight color accent).
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary card component can be visually adjusted without backend/API changes.
- **Risks / open questions:** May require minor design system updates; risk of visual clutter if not carefully balanced.
- **What should be validated:** Quick comprehension in 5-second tests; user preference for new visual treatment.

#### 2. "Sticky Summary Header"
- **Description:** Make the patient summary persistently visible as a sticky header during key workflow steps (e.g., scrolling through dossier or consultation).
- **Impacted moment:** Throughout dossier/consultation navigation
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Frontend supports sticky positioning; summary content is concise enough for persistent display.
- **Risks / open questions:** Screen real estate on smaller devices; possible distraction.
- **What should be validated:** Usability on various screen sizes; does stickiness aid or distract?

#### 3. "Quick Summary Toggle"
- **Description:** Add a one-click toggle (e.g., icon or button) to expand/collapse the patient summary for rapid access without leaving the current context.
- **Impacted moment:** Any point during dossier/consultation
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Toggle can be implemented using existing UI patterns.
- **Risks / open questions:** Discoverability of the toggle; risk of users missing summary if collapsed by default.
- **What should be validated:** Toggle discoverability; impact on workflow speed.

---

## Topic 2: pediatric_data_prominence

### Problem recap
Pediatricians in France cannot easily identify or access key pediatric data (growth, development, vaccination), leading to inefficiency and missed signals.

### Solution directions

#### 1. "Pediatric Highlights Row"
- **Description:** Add a dedicated row or section at the top of the patient summary displaying pediatric-specific signals (growth percentile, development milestones, vaccination status) using icons or compact charts.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia (FR)
- **Assumptions:** Data is already available in the frontend; can be surfaced using existing visualization components.
- **Risks / open questions:** Overcrowding summary card; clarity of iconography.
- **What should be validated:** Pediatrician ability to spot key data in 5 seconds; icon comprehension.

#### 2. "Contextual Pediatric Badges"
- **Description:** Overlay small, color-coded badges or indicators on the patient summary and relevant sections (e.g., dossier tabs) to flag pediatric-relevant data or alerts.
- **Impacted moment:** Throughout dossier/consultation navigation
- **Products impacted:** Libellia (FR)
- **Assumptions:** Badge component exists or can be adapted; logic for badge display is frontend-only.
- **Risks / open questions:** Risk of badge overload; visual noise.
- **What should be validated:** Badge effectiveness in drawing attention; does not increase cognitive load.

#### 3. "Pediatric Quick Access Tab"
- **Description:** Add a fixed, always-visible tab or button for direct access to a pediatric data synthesis view (reusing existing synthesis components).
- **Impacted moment:** Any point during dossier/consultation
- **Products impacted:** Libellia (FR)
- **Assumptions:** Synthesis view exists and can be filtered for pediatric data.
- **Risks / open questions:** Navigation consistency; risk of fragmenting workflow.
- **What should be validated:** Speed of access; user preference for tab vs. inline display.

---

## Topic 3: cognitive_load

### Problem recap
Users experience high cognitive load due to dense screens and non-prioritized information, especially during pediatric consultations.

### Solution directions

#### 1. "Progressive Disclosure for Pediatric Data"
- **Description:** Collapse less-critical pediatric data by default, with clear expand/collapse affordances, so only the most relevant signals are shown upfront.
- **Impacted moment:** Consultation start, dossier review
- **Products impacted:** Libellia (FR)
- **Assumptions:** Existing UI supports collapsible sections; prioritization of signals is agreed.
- **Risks / open questions:** Users may miss hidden data; need clear cues for expandability.
- **What should be validated:** User ability to find hidden data; does this reduce perceived overload?

#### 2. "Visual Grouping and Spacing"
- **Description:** Apply increased spacing and visual grouping (e.g., cards, separators) to pediatric data sections to reduce visual clutter and guide attention.
- **Impacted moment:** Dossier and consultation views
- **Products impacted:** Libellia (FR)
- **Assumptions:** Can be achieved with frontend style updates; no backend changes.
- **Risks / open questions:** May increase vertical scroll; risk of hiding information below the fold.
- **What should be validated:** User perception of clarity; impact on navigation speed.

#### 3. "Signal Priority Icons"
- **Description:** Use a limited set of priority icons (e.g., star, exclamation) to visually mark the most critical pediatric data points within existing views.
- **Impacted moment:** Dossier and consultation views
- **Products impacted:** Libellia (FR)
- **Assumptions:** Icon set exists; priority rules are defined.
- **Risks / open questions:** Icon overload; ambiguity in what icons mean.
- **What should be validated:** Icon comprehension; does this help users focus?

---

## Cross-topic considerations

- **Shared patterns:** Visual prioritization (icons, badges, highlights) and progressive disclosure are recurring themes.
- **Platform implications:** Patient summary visibility improvements should be handled at NAIS platform level for consistency; pediatric-specific changes remain Libellia-specific.
- **Sequencing / dependency notes:** Summary visibility changes should precede pediatric-specific enhancements to avoid conflicting layouts; cognitive load reductions can be layered on top of