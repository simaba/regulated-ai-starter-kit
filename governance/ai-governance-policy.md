# AI Governance Policy

**Organization:** [Organization Name]
**Version:** 1.0
**Effective Date:** [Date]
**Owner:** [AI Governance Lead / CAIO]

---

## 1. Purpose

This policy establishes [Organization Name]'s commitment to the responsible
development, deployment, and operation of artificial intelligence (AI) systems.
It defines the governance structures, principles, and processes that ensure AI
systems are trustworthy, safe, and aligned with applicable regulatory requirements.

---

## 2. Scope

This policy applies to all AI systems developed, procured, or deployed by
[Organization Name], including:
- Machine learning models in production
- Large language model (LLM) applications
- Automated decision-making systems
- AI-powered tools used by employees or customers

---

## 3. Core Principles

| Principle | Description |
|---|---|
| **Accountability** | Clear ownership of AI systems through the full lifecycle |
| **Transparency** | Explainable AI decisions with appropriate documentation |
| **Fairness** | Bias evaluation and mitigation across affected populations |
| **Safety** | Robust testing and monitoring before and after deployment |
| **Privacy** | Data minimization and protection in AI system design |
| **Human Oversight** | Appropriate human review for high-stakes AI decisions |

---

## 4. NIST AI RMF Alignment

This policy implements the NIST AI Risk Management Framework (AI RMF 1.0):

- **GOVERN:** This policy, roles (see `roles-and-responsibilities.md`), and model inventory
- **MAP:** Risk taxonomy and per-system risk assessments (`risk/`)
- **MEASURE:** Release readiness gates and evaluation metrics (`release/`)
- **MANAGE:** Incident response procedures and monitoring (`incident/`)

---

## 5. Regulatory Compliance

[Organization Name] AI systems must comply with applicable regulations including:

- [ ] NIST AI RMF (voluntary but adopted as internal standard)
- [ ] EU AI Act (if applicable — systems affecting EU residents)
- [ ] ISO/IEC 42001 (if certification is pursued)
- [ ] HIPAA (if applicable — healthcare AI systems)
- [ ] GLBA / SR 11-7 (if applicable — financial services AI models)
- [ ] State AI regulations (identify applicable state laws)

---

## 6. AI System Classification

All AI systems must be classified before deployment:

| Risk Level | Criteria | Governance Required |
|---|---|---|
| **High Risk** | Automated decisions affecting individuals' rights, health, or finances | Full review cycle, legal sign-off, ongoing monitoring |
| **Medium Risk** | AI-assisted decisions with human in the loop | Technical review, bias evaluation, documentation |
| **Low Risk** | Internal tools, analytics, no direct individual impact | Standard development process, documented |

---

## 7. Prohibited Uses

[Organization Name] prohibits AI systems that:
- Make autonomous decisions in life-or-death situations without human oversight
- Generate or process protected class information in discriminatory ways
- Operate without explainability mechanisms in regulated decision contexts
- Process personal data in ways inconsistent with privacy policies and applicable law

---

## 8. Review and Updates

This policy is reviewed annually or when significant regulatory changes occur.
Questions: contact [AI Governance Lead] or open a GitHub Discussion.
