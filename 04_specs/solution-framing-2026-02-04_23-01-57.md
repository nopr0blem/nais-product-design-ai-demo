# Solution Framing (UX-led, IA-assisted)

## Scope
Topics covered: TOP 3 from Insight Analysis
1. Patient summary visibility
2. Pediatric data visibility
3. Vaccination visibility

---

## Topic 1: Patient summary visibility

### Problem recap
Users struggle to immediately see a relevant, clear summary of the patient’s status, especially for pediatric cases, leading to slower orientation and increased cognitive load at the start of a consultation.

### Solution directions

**Option 1: Pediatric-Focused Summary Block**
- **Description:** Add a dedicated, visually distinct summary block at the top of the patient dossier/consultation view, surfacing age, growth percentiles, key conditions, and next critical actions.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary widget can be adapted; no new backend fields required.
- **Risks / open questions:** May require minor UI layout changes; risk of overcrowding if not carefully prioritized.
- **What should be validated:** Quick comprehension in 5 seconds (UX test); technical feasibility of summary block reuse.

**Option 2: Progressive Disclosure in Summary**
- **Description:** Default summary shows only top 2–3 pediatric signals (e.g., age, weight trend, vaccination status), with a “Show more” to expand for details.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Existing summary component supports collapsible sections.
- **Risks / open questions:** Users may miss less prominent data; needs careful selection of default signals.
- **What should be validated:** User preference for default vs. expanded view; impact on speed of orientation.

**Option 3: Highlighted Pediatric Alerts**
- **Description:** Use visual cues (badges, color highlights) to flag urgent pediatric issues (e.g., missed vaccinations, abnormal growth) directly in the summary.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Both (Libellia, Studio)
- **Assumptions:** Alert logic can be implemented with current data; no new backend logic needed.
- **Risks / open questions:** Risk of alert fatigue; requires clear criteria for what triggers an alert.
- **What should be validated:** Clarity and usefulness of alerts (prototype test); technical feasibility.

---

## Topic 2: Pediatric data visibility

### Problem recap
Pediatricians in Libellia cannot easily access or interpret key pediatric data (growth, development, milestones) due to poor prioritization and lack of synthesis.

### Solution directions

**Option 1: Growth & Development Mini-Panel**
- **Description:** Insert a compact, always-visible panel in the patient view showing latest growth metrics, percentile curves, and milestone checklists.
- **Impacted moment:** Dossier opening, during consultation
- **Products impacted:** Libellia
- **Assumptions:** Growth data already available in frontend; can reuse chart widget.
- **Risks / open questions:** Space constraints; may need to hide less relevant adult data.
- **What should be validated:** Usability of mini-panel; impact on consultation flow.

**Option 2: Pediatric Tab in Patient Record**
- **Description:** Add a dedicated “Pediatrics” tab aggregating all child-specific data (growth, milestones, vaccinations) for quick access.
- **Impacted moment:** Dossier navigation, consultation
- **Products impacted:** Libellia
- **Assumptions:** Tabbed navigation pattern exists; data aggregation possible without backend changes.
- **Risks / open questions:** Risk of users missing data if not in default view; tab overload.
- **What should be validated:** Discoverability and usage of the tab; preference for tab vs. inline display.

**Option 3: Contextual Pediatric Data Popover**
- **Description:** Enable hover/click on child’s age or name to show a popover with key pediatric data (growth, milestones, next vaccine).
- **Impacted moment:** Dossier opening, consultation
- **Products impacted:** Libellia
- **Assumptions:** Popover component available; data accessible in frontend.
- **Risks / open questions:** May not be discoverable for all users; accessibility concerns.
- **What should be validated:** Ease of access; user understanding of interaction.

---

## Topic 3: Vaccination visibility

### Problem recap
Vaccination status is not immediately visible or actionable in the pediatric workflow, causing missed or delayed interventions.

### Solution directions

**Option 1: Vaccination Status Widget in Summary**
- **Description:** Integrate a vaccination status indicator (e.g., up-to-date, overdue, upcoming) directly into the patient summary area.
- **Impacted moment:** Dossier opening, consultation start
- **Products impacted:** Libellia
- **Assumptions:** Vaccination data available in frontend; summary area can be extended.
- **Risks / open questions:** May crowd summary if not designed compactly.
- **What should be validated:** Visibility and clarity of status; technical feasibility.

**Option 2: Next Vaccine Callout**
- **Description:** Add a prominent callout (e.g., colored pill or banner) showing the next due vaccine and date in the consultation view.
- **Impacted moment:** Consultation start, during consultation
- **Products impacted:** Libellia
- **Assumptions:** Next vaccine logic can be computed client-side.
- **Risks / open questions:** Accuracy of due date calculation; risk of distraction if too prominent.
- **What should be validated:** Comprehension and actionability; accuracy of displayed information.

**Option 3: Vaccination Timeline Quick Access**
- **Description:** Provide a one-click access (icon/button) to a timeline or list of past and upcoming vaccinations from the main patient view.
- **Impacted moment:** Dossier opening, consultation
- **Products impacted:** Libellia
- **Assumptions:** Timeline/list component exists; data available.
- **Risks / open questions:** May add navigation step; risk of underuse if not visible enough.
- **What should be validated:** Usage frequency; user preference for timeline vs. list.

---

## Cross-topic considerations

- **Shared patterns:** Use of summary blocks, visual cues, and progressive disclosure can be standardized across both products where possible.
- **Platform implications:** Most solutions leverage existing NAIS components (summary, tabs, popovers); avoid backend/API changes.
- **Sequencing / dependency notes:** Patient summary improvements should precede or coincide with pediatric data and vaccination visibility enhancements to avoid redundant UI changes.

---

## What the human team must decide

- Which summary enhancements (block,