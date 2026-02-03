# Product Context — NAIS Platform

## Platform
NAIS is a modular healthcare platform designed to support multiple countries and medical specialties.

Core principles:
- Shared platform, localized products
- Reusable workflows and components
- Progressive maturity (not feature parity at all costs)

---

## Products

### Libellia (France)
Target users:
- Pediatricians
- General Practitioners
- Solo or small practices

Current maturity:
- Patient record: stable
- Consultation workflow: partially implemented
- Pediatric-specific views: limited
- Administrative workflows: in progress (SPICE, MSS)

Known gaps:
- Weak pediatric signal prioritization
- Limited synthesis readability
- Workflow still influenced by adult/GP logic

Constraints:
- Segur V1 ongoing
- No major architectural refactor in short term

---

### Studio (Italy)
Target users:
- General practitioners
- Pediatricians (secondary)

Current maturity:
- Administrative workflows more mature
- Consultation workflow more flexible
- Pediatric specialization less advanced

Constraints:
- Country-specific integrations (FSE)
- Different coding systems (ICD9)

---

## Important rule for analysis
When generating insights or solutions:
- Do not assume missing features already exist
- Prefer incremental improvements over full redesign
- Reuse existing workflows and components when possible
