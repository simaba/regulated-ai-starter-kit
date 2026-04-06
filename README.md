# Regulated AI Starter Kit

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge&logo=github)](https://github.com/simaba/regulated-ai-starter-kit/generate)
[![NIST AI RMF](https://img.shields.io/badge/NIST%20AI%20RMF-Aligned-0055A4?style=flat-square)](https://www.nist.gov/system/files/documents/2023/01/26/AI%20RMF%201.0.pdf)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Maintained](https://img.shields.io/badge/Maintained-yes-green.svg?style=flat-square)](https://github.com/simaba/regulated-ai-starter-kit)

A **GitHub template repository** giving AI teams a running start on governance,
compliance, and deployment readiness for regulated industries.

Click **"Use this template"** above to create your own copy pre-wired with:

- NIST AI RMF-aligned governance documentation
- A YAML-driven release readiness gate system
- A structured risk taxonomy (mapped to NIST RMF + EU AI Act)
- CI/CD validation pipelines
- Incident response playbook stubs
- Model card templates

---

## Who Is This For?

Teams deploying AI in:
- **Healthcare** — clinical decision support, diagnostic AI, patient risk scoring
- **Financial Services** — credit scoring, fraud detection, algorithmic trading
- **Insurance** — underwriting AI, claims automation, risk assessment
- **Government** — benefits eligibility, document processing, public-facing AI

---

## Repository Structure

```
regulated-ai-starter-kit/
├── governance/
│   ├── ai-governance-policy.md        # Organizational AI governance policy template
│   ├── roles-and-responsibilities.md  # RACI for AI governance roles
│   ├── model-inventory.md             # Active model inventory tracker
│   └── nist-rmf-mapping.md            # Your implementation of NIST AI RMF functions
│
├── risk/
│   ├── risk-register.md               # AI risk register template
│   ├── risk-taxonomy.yaml             # Structured risk taxonomy (NIST + EU AI Act)
│   └── risk-assessment-template.md    # Per-system risk assessment template
│
├── release/
│   ├── release-checklist.yaml         # Release readiness gate configuration
│   ├── release-readiness-report.md    # Pre-deployment readiness report template
│   └── deployment-approval.md        # Deployment approval sign-off template
│
├── incident/
│   ├── incident-response-playbook.md  # AI incident response procedures
│   ├── incident-report-template.md    # Post-incident report template
│   └── escalation-matrix.md          # Escalation paths and contacts
│
├── model-cards/
│   └── model-card-template.md        # Standard model card template
│
├── .github/
│   └── workflows/
│       ├── validate-release-config.yml # CI: validates release-checklist.yaml
│       └── governance-checks.yml      # CI: checks governance doc completeness
│
└── setup.py                           # Setup wizard (coming soon)
```

---

## Quick Start

### 1. Create Your Repository From This Template

Click "Use this template" → "Create a new repository" and give it a name like
`acme-ai-governance` or `{team}-ai-deployment-kit`.

### 2. Customize the Governance Policy

Edit `governance/ai-governance-policy.md` — replace `[Organization Name]` placeholders
with your organization's name and adapt the policy sections to match your internal processes.

### 3. Configure Your Release Checklist

Edit `release/release-checklist.yaml` to add or remove checks relevant to your
tech stack and regulatory environment:

```yaml
# release/release-checklist.yaml
metadata:
  project: "Your Project Name"
  version: "1.0.0"
  environment: "production"
  regulated_industry: "healthcare"  # or: finance, insurance, government

pre_deployment_gates:
  model_validation:
    accuracy_threshold: 0.95
    bias_evaluation: required
    explainability_report: required
  governance:
    risk_assessment_complete: true
    legal_review_complete: true
    compliance_sign_off: true
  infrastructure:
    security_scan: passed
    load_testing: passed
    rollback_plan: documented
```

### 4. Run the CI Validation

Push to any branch to trigger automatic validation of your release configuration:

```bash
git add .
git commit -m "Configure release checklist for production deployment"
git push
```

The GitHub Actions workflow will validate your YAML configuration and report
any missing required fields.

### 5. Complete Your Risk Assessment

Copy `risk/risk-assessment-template.md` and fill it out for each AI system
you are deploying. The template walks through NIST AI RMF risk categories.

---

## NIST AI RMF Alignment

This starter kit implements the four core NIST AI RMF functions:

| Function | Implementation in This Kit |
|---|---|
| **Govern** | `governance/` directory — policy, roles, model inventory |
| **Map** | `risk/risk-taxonomy.yaml` — categorized risk landscape |
| **Measure** | `release/release-checklist.yaml` — measurable deployment gates |
| **Manage** | `incident/` directory — response procedures and escalation |

---

## Related Resources

| Repository | What It Adds |
|---|---|
| [enterprise-ai-governance-playbook](https://github.com/simaba/enterprise-ai-governance-playbook) | Full governance playbook with detailed implementation guidance |
| [ai-release-readiness-checklist](https://github.com/simaba/ai-release-readiness-checklist) | Extended release checklist framework and CLI tool |
| [ai-risk-taxonomy](https://github.com/simaba/ai-risk-taxonomy) | Detailed AI risk taxonomy with NIST RMF + EU AI Act mappings |
| [nist-ai-rmf-implementation-guide](https://github.com/simaba/nist-ai-rmf-implementation-guide) | Step-by-step guide for implementing NIST AI RMF |
| [awesome-ai-governance](https://github.com/simaba/awesome-ai-governance) | Curated list of AI governance resources |

---

## License

MIT License — see [LICENSE](LICENSE). Use freely in your organization.

---

*Maintained by [Sima Bagheri](https://github.com/simaba) · Built for AI teams in regulated industries*
