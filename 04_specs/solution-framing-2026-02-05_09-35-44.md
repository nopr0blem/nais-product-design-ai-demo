# Solution Framing (UX-led, IA-assisted)

## Scope
Topics covered: TOP 3 from Insight Analysis

1. patient_summary_visibility (Libellia, Studio, FR/IT)
2. pediatric_data_prominence (Libellia, FR)
3. cognitive_load (Libellia, FR)

---

## Topic 1: patient_summary_visibility

### Problem recap
Users struggle to immediately see a clear, clinically relevant summary of the pediatric patient, impacting their ability to quickly assess status at the start of a consultation.

### Solution directions

#### 1. "Summary Card Emphasis"
- **Description:** Visually elevate the existing patient summary card at dossier/consultation entry (e.g., increased size, color accent, placement at top).
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary card component is available and can be visually adjusted without backend/API changes.
- **Risks / open questions:** Risk of visual clutter if not carefully designed; may not address content gaps in summary.
- **What should be validated:** Quick comprehension test (5-second rule); visual hierarchy in prototype.

#### 2. "Progressive Disclosure for Details"
- **Description:** Show only the most critical summary signals by default (e.g., age, growth percentile, key alerts), with a clear "expand for more" affordance.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary data can be filtered/hidden via frontend logic.
- **Risks / open questions:** May hide information some users expect; needs careful selection of default signals.
- **What should be validated:** User acceptance of default vs. expanded view; test with pediatricians.

#### 3. "Sticky Summary Bar"
- **Description:** Make the summary persistently visible as a sticky header during consultation navigation.
- **Impacted moment:** Throughout consultation workflow
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Frontend supports sticky/fixed elements; summary content is not too large.
- **Risks / open questions:** May reduce available screen space; performance on lower-end devices.
- **What should be validated:** Usability in real workflows; impact on screen real estate.

---

## Topic 2: pediatric_data_prominence

### Problem recap
Pediatric-specific data (growth, development, vaccination) is not prominent enough in the current UI, making it harder for pediatricians to focus on key signals during consultations.

### Solution directions

#### 1. "Pediatric Signal Highlighting"
- **Description:** Use color, iconography, or badges to visually distinguish pediatric data fields (e.g., growth charts, vaccination status) within the summary and consultation views.
- **Impacted moment:** Dossier opening, consultation start, during consultation
- **Products impacted:** Libellia (FR)
- **Assumptions:** Existing UI elements can be styled/enhanced without new data sources.
- **Risks / open questions:** Overuse of highlights may reduce effectiveness; needs balance.
- **What should be validated:** Visual scan test; pediatrician feedback on prominence.

#### 2. "Section Reordering for Pediatrics"
- **Description:** Move pediatric-relevant sections (growth, development, vaccination) to the top of the summary/consultation screens for pediatric patients.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia (FR)
- **Assumptions:** Section order is configurable at the frontend for pediatric profiles.
- **Risks / open questions:** May disrupt workflows for GPs; needs to be pediatric-specific.
- **What should be validated:** Pediatrician acceptance; no negative impact on GP workflows.

#### 3. "Quick-Access Pediatric Tabs"
- **Description:** Add pediatric-specific quick-access tabs or shortcuts in the summary/consultation view (e.g., "Growth," "Vaccination").
- **Impacted moment:** Consultation start, during consultation
- **Products impacted:** Libellia (FR)
- **Assumptions:** Tabbed navigation exists or can be reused; no backend changes required.
- **Risks / open questions:** Tab overload; discoverability for new users.
- **What should be validated:** Usability of tab navigation; speed of access to pediatric data.

---

## Topic 3: cognitive_load

### Problem recap
The current interface presents too much information or too many options at once, increasing cognitive load for pediatricians during time-pressured consultations.

### Solution directions

#### 1. "Default Collapsed Sections"
- **Description:** Collapse less critical sections by default, showing only the most relevant pediatric information on initial view.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia (FR)
- **Assumptions:** Section collapse/expand is supported in the frontend.
- **Risks / open questions:** Users may miss information; needs clear affordance for expansion.
- **What should be validated:** User ability to find hidden info; satisfaction with reduced clutter.

#### 2. "Contextual Tooltips/Helpers"
- **Description:** Add subtle tooltips or helper texts that appear contextually, guiding users to key actions or explaining pediatric data fields only when needed.
- **Impacted moment:** During consultation, when hovering or focusing on fields
- **Products impacted:** Libellia (FR)
- **Assumptions:** Tooltip/helper pattern exists in component library.
- **Risks / open questions:** Tooltip overload; accessibility for keyboard users.
- **What should be validated:** User comprehension; impact on workflow speed.

#### 3. "Visual Grouping of Pediatric Data"
- **Description:** Group related pediatric data visually (e.g., within a bordered box or shaded area), reducing visual fragmentation and aiding quick scanning.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia (FR)
- **Assumptions:** UI allows for visual grouping without backend changes.
- **Risks / open questions:** May require minor layout adjustments; risk of over-grouping.
- **What should be validated:** User ability to scan and locate pediatric data quickly.

---

## Cross-topic considerations

- **Shared patterns:** Visual hierarchy, progressive disclosure, and section reordering are relevant across all three topics.
- **Platform implications:** "Summary Card Emphasis" and "Sticky Summary Bar" could be standardized at the NAIS platform level for reuse.
- **Sequencing / dependency notes:** 
  - Section reordering and visual grouping should precede more complex navigation changes.
  - Any changes to summary visibility should be validated for both pediatric and adult/GP