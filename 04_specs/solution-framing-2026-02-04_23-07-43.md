# Solution Framing (UX-led, IA-assisted)

## Scope
Topics covered: TOP 3 from Insight Analysis  
1. patient_summary_visibility  
2. pediatric_data_visibility  
3. cognitive_load

---

## Topic 1: patient_summary_visibility

### Problem recap
Users struggle to immediately access and understand the patient summary at key workflow moments, impacting both Libellia (FR) and Studio (IT).

### Solution directions

**Option 1: Persistent Summary Banner**
- **Description:** Add a persistent, collapsible summary banner at the top of the patient dossier and consultation screens, displaying key patient signals (age, allergies, chronic conditions, last visit).
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary widget can be reused/adapted; no backend changes required.
- **Risks / open questions:** Banner may reduce available screen space; needs to avoid information overload.
- **What should be validated:** Quick-glance comprehension (5-second test), impact on screen real estate.

**Option 2: Enhanced Summary Card Placement**
- **Description:** Reposition the existing summary card to the most prominent area of the patient view, using visual hierarchy (color, size) to distinguish it from secondary data.
- **Impacted moment:** Dossier opening
- **Products impacted:** Both
- **Assumptions:** Current summary card component is available and modifiable.
- **Risks / open questions:** May conflict with local layout conventions; risk of crowding if not carefully prioritized.
- **What should be validated:** Eye-tracking or click heatmaps, user preference testing.

**Option 3: Contextual Summary Popover**
- **Description:** Introduce a summary popover accessible via a fixed icon/button, showing the patient’s key data on demand without navigating away.
- **Impacted moment:** Throughout dossier and consultation
- **Products impacted:** Both
- **Assumptions:** Popover component exists in shared library.
- **Risks / open questions:** Discoverability; risk of users missing the feature if not visually prominent.
- **What should be validated:** Usability testing for discoverability and speed.

---

## Topic 2: pediatric_data_visibility

### Problem recap
Pediatricians in Libellia (FR) cannot easily access or synthesize pediatric-specific data (growth, development, vaccinations), leading to missed signals and increased cognitive effort.

### Solution directions

**Option 1: Pediatric Data Highlight Section**
- **Description:** Add a dedicated, visually distinct section at the top of the patient summary for pediatric signals (growth curves, development milestones, vaccination status).
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia
- **Assumptions:** Existing widgets for growth/vaccination can be reused; no new data sources required.
- **Risks / open questions:** May require minor UI adjustments; risk of overwhelming the summary if not carefully scoped.
- **What should be validated:** Pediatrician feedback on relevance and clarity.

**Option 2: Tabbed Pediatric View**
- **Description:** Introduce a pediatric-specific tab in the patient dossier, grouping all relevant pediatric data for quick access.
- **Impacted moment:** Dossier navigation
- **Products impacted:** Libellia
- **Assumptions:** Tabbed navigation pattern exists; data already available in system.
- **Risks / open questions:** Potential for users to miss pediatric data if not default; extra click required.
- **What should be validated:** Usage analytics, preference testing.

**Option 3: Inline Pediatric Alerts**
- **Description:** Display inline alerts or badges for missing/outdated pediatric data (e.g., overdue vaccinations) directly in the summary or consultation view.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia
- **Assumptions:** Alert/badge components exist; logic for overdue data can be handled on frontend.
- **Risks / open questions:** Alert fatigue; clarity of alert criteria.
- **What should be validated:** Pediatrician understanding and perceived usefulness.

---

## Topic 3: cognitive_load

### Problem recap
Libellia users (FR) experience high cognitive load due to dense screens and non-prioritized information, especially during time-pressured consultations.

### Solution directions

**Option 1: Progressive Disclosure for Secondary Data**
- **Description:** Collapse or hide less critical data by default, allowing users to expand sections only when needed.
- **Impacted moment:** Consultation, dossier review
- **Products impacted:** Libellia
- **Assumptions:** Expand/collapse UI pattern exists; no backend changes needed.
- **Risks / open questions:** Risk of hiding needed information; must ensure defaults match clinical priorities.
- **What should be validated:** Task completion time, error rate, user satisfaction.

**Option 2: Visual Signal Emphasis**
- **Description:** Use color, icons, and font weight to visually emphasize the most clinically relevant data (e.g., abnormal growth, missing vaccinations).
- **Impacted moment:** Consultation, summary review
- **Products impacted:** Libellia
- **Assumptions:** Visual styling can be safely adjusted within design system.
- **Risks / open questions:** Overuse of emphasis may reduce effectiveness; accessibility (contrast, color blindness).
- **What should be validated:** Visual hierarchy comprehension, accessibility review.

**Option 3: Default Pediatric View for Pediatricians**
- **Description:** Automatically present the pediatric summary view as the default for pediatrician users, reducing navigation and filtering steps.
- **Impacted moment:** Dossier opening
- **Products impacted:** Libellia
- **Assumptions:** User role detection is reliable; pediatric summary view exists.
- **Risks / open questions:** Edge cases for mixed practices; user override needs.
- **What should be validated:** Pediatrician workflow fit, error/override frequency.

---

## Cross-topic considerations

- **Shared patterns:** Visual hierarchy, progressive disclosure, and summary emphasis are relevant across all topics.
- **Platform implications:** Patient summary improvements should be platform-level (NAIS), but pediatric-specific enhancements are Libellia-only.
- **Sequencing / dependency notes:** Patient summary visibility improvements should precede pediatric data visibility changes to avoid rework; cognitive load solutions can be layered on top.

---

## What the human team must decide

- Which summary enhancement direction best balances visibility and screen space (banner, card, popover)?
- Should pediatric data be highlighted in the main summary or separated in a dedicated view/tab?
- What is the acceptable trade-off between hiding secondary data and risk of missing information?
- How much visual emphasis is appropriate without causing alert fatigue or accessibility issues?
- Should pediatricians always land on a