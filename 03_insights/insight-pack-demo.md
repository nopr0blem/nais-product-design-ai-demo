# Insight Pack: NAIS Platform User Signals (Libellia FR, Studio IT)

## 1. Key Insights

### 1.1. Difficulty Assessing Patient Status at a Glance
- Pediatricians in France report that the patient summary does not allow them to quickly determine a child's health status upon opening the file. [sig_2026_02_03_001]
- General practitioners in France seek prominent display of critical alerts amid information overload. [sig_2026_02_03_002]
- Italian pediatricians indicate that clinically prioritized information is not immediately visible during first visits. [sig_2026_02_03_003]

**Implication:** Both Libellia (FR) and Studio (IT) users struggle to rapidly identify key clinical information, especially at critical moments (file opening, first visit).

---

### 1.2. Insufficient Highlighting of Pediatric Data
- French pediatricians state that growth curves and percentiles are present but not sufficiently visible in the patient summary. [sig_2026_02_03_005]

**Implication:** Essential pediatric metrics are not adequately surfaced, impacting clinical efficiency for pediatric use cases.

---

### 1.3. Lack of Contextualization in Patient View
- French general practitioners note that the patient view remains identical regardless of patient age or context. [sig_2026_02_03_006]

**Implication:** The platform does not adapt its display to patient demographics or clinical context, reducing relevance and efficiency.

---

### 1.4. Information Overload and Prioritization Challenges
- General practitioners in France and Italy express that while navigation is clear, key information is not sufficiently highlighted, slowing down workflow. [sig_2026_02_03_002, sig_2026_02_03_004]
- Italian pediatricians report that vaccination information is not immediately distinguishable from other data. [sig_2026_02_03_007]

**Implication:** Users experience cognitive overload and require better visual prioritization of alerts, vaccinations, and key clinical data.

---

## 2. Recommendations

- Redesign patient summary views to surface critical clinical status and alerts at a glance, tailored to context (e.g., age, visit type). [sig_2026_02_03_001, sig_2026_02_03_003, sig_2026_02_03_006]
- Enhance visibility of pediatric-specific data (growth curves, percentiles, vaccinations) in relevant patient summaries. [sig_2026_02_03_005, sig_2026_02_03_007]
- Implement visual hierarchy and prioritization mechanisms to reduce cognitive load and highlight urgent information. [sig_2026_02_03_002, sig_2026_02_03_004]

---

## 3. Evidence Table

| Signal ID             | Product   | Persona                | Theme                  | Severity | Key Point                                                                 |
|-----------------------|-----------|------------------------|------------------------|----------|--------------------------------------------------------------------------|
| sig_2026_02_03_001    | libellia  | pédiatre (FR)          | synthese_patient       | High     | Cannot quickly assess child’s health status in summary                    |
| sig_2026_02_03_002    | libellia  | médecin généraliste (FR)| charge_cognitive       | Medium   | Too much info; wants important alerts highlighted                         |
| sig_2026_02_03_003    | studio    | pediatra (IT)          | priorisation_clinique  | High     | Priority clinical info not visible at first visit                         |
| sig_2026_02_03_004    | studio    | medico generale (IT)   | navigation             | Low      | Navigation clear, but key info should be more prominent                   |
| sig_2026_02_03_005    | libellia  | pédiatre (FR)          | donnees_pediatriques   | High     | Growth curves/percentiles not visible enough in summary                   |
| sig_2026_02_03_006    | libellia  | médecin généraliste (FR)| vue_patient            | Medium   | Patient view not adapted by age/context                                   |
| sig_2026_02_03_007    | studio   