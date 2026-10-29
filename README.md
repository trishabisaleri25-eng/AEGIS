# AEGIS

AEGIS is a Python project for reviewing AI systems for governance and security risks. It brings together risk classification, model documentation, and human review steps.

The project covers requirements and guidance related to the EU AI Act, GDPR Article 35, and ISO/IEC 42001. It is a practical tool for teams working with AI systems.

## Features

- 🔴 Classify AI systems by risk level and record the reasons
- 📋 Create model cards in Markdown or JSON
- 🗺️ Map AI systems to GDPR Article 35 DPIA requirements
- 🔐 Review security risks such as adversarial attacks and data integrity issues
- 👁️ Record human review steps for high-risk decisions
- 💡 Create reports about transparency and governance gaps
- 🖥️ Use the Streamlit dashboard

Some features are still in progress. See the status table below.

## Why AEGIS?

Many organisations are adopting AI faster than their security and governance processes can keep up. Teams may face:

- No clear way to classify AI risk across different teams
- AI systems used without security threat modelling or adversarial risk reviews
- Human oversight that is documented but not used in day-to-day decisions
- Model documentation that is not ready for regulatory reviews or audits
- DPIA processes that do not fully consider AI systems

AEGIS helps teams connect AI deployment with accountability by including security, human oversight, and explainability from the start.

## Quick start

Install the package:

```bash
pip install aegis-framework
```

Example usage:

```python
from aegis import RiskClassifier, ModelCardGenerator, HITLController

classifier = RiskClassifier()
result = classifier.classify(
    system_name="Customer Credit Scoring Model",
    domain="financial_services",
    automated_decision=True,
)
print(result.risk_tier)
print(result.obligations)

card = ModelCardGenerator()
card.generate(model_name="credit-scorer-v2", output_format="markdown")

hitl = HITLController()
hitl.define_checkpoint(
    decision_type="credit_denial",
    required_reviewer="human",
    escalation_threshold=0.85,
)
```

## Feature status

| Feature | Status |
|---|---|
| EU AI Act risk classification | Available |
| Model card generation (Markdown and JSON) | Available |
| GDPR Article 35 DPIA mapping | Available |
| Streamlit dashboard | Available |
| AI security risk assessment | In progress |
| Human review controls | In progress |
| Explainability reports | In progress |
| AI system inventory | In progress |
| Cloud integration guides | Planned |

## Installation from source

Requirements: Python 3.9 or later.

```bash
git clone https://github.com/trishabisaleri25-eng/AEGIS.git
cd AEGIS
pip install -r requirements.txt
```

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

Areas for improvement include security risk reviews, human oversight, explainability, regulatory mappings, and cloud integration examples.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Note

AEGIS is not legal advice. It is a tool to support AI governance and security work.
