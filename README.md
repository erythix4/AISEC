#  AI Security Resources

### Learn. Understand. Decide.

> A curated collection of **free, open resources** to help engineers, decision-makers, and researchers understand the security challenges of AI systems in production  and make informed choices about how to address them.

---

##  Why This Repository?

AI is being deployed at scale in critical systems from industrial environments to public services  often without a clear understanding of the security risks involved. Most existing resources are either vendor-locked, overly academic or scattered across dozens of sources.

This repository aims to change that by providing a **structured, vendor-neutral, and opinionated learning path** through the landscape of AI security. Whether you're a developer shipping ML models, a CISO evaluating risk, or a student entering the field, you'll find practical knowledge here.

**No hype. No sales pitch. Just signal.**

---

##  Table of Contents

- [Foundations](#-foundations)
- [Threat Landscape](#-threat-landscape)
- [LLM Security](#-llm-security)
- [MLOps & Supply Chain Security](#-mlops--supply-chain-security)
- [AI Observability & Monitoring](#-ai-observability--monitoring)
- [Governance, Regulation & Compliance](#-governance-regulation--compliance)
- [Hands-On Labs & Challenges](#-hands-on-labs--challenges)
- [Talks, Courses & Conferences](#-talks-courses--conferences)
- [Community & Contribution](#-community--contribution)

- [Erythix ressources ](#-erythix--ressources)

---

##  Foundations

Core concepts you should master before diving deeper.

| Resource | Type | Description |
|----------|------|-------------|
| [OWASP ML Top 10](https://owasp.org/www-project-machine-learning-security-top-10/) | Framework | Top 10 security risks in machine learning systems |
| [OWASP Top 10 for LLM Applications](https://genai.owasp.org/) | Framework | Dedicated risk taxonomy for LLM-powered applications |
| [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence/executive-order-safe-secure-and-trustworthy-artificial-intelligence) | Standard | US federal framework for AI risk governance |
| [MITRE ATLAS](https://atlas.mitre.org/) | Knowledge Base | Adversarial threat landscape for AI systems (ATT&CK for AI) |
| [EU AI Act — Full Text](https://artificialintelligenceact.eu/) | Regulation | The European regulation on artificial intelligence |
| [ENISA AI Threat Landscape](https://www.enisa.europa.eu/) | Report | European perspective on AI cybersecurity threats |

---

##  Threat Landscape

Understanding how AI systems are attacked in practice.

### Adversarial Machine Learning

- [Adversarial Robustness Toolbox (ART)](https://github.com/Trusted-AI/adversarial-robustness-toolbox)  IBM's open-source library for ML security (evasion, poisoning, extraction, inference attacks)
- [CleverHans](https://github.com/cleverhans-lab/cleverhans)  Benchmarking ML model vulnerability to adversarial examples
- [TextAttack](https://github.com/QData/TextAttack)  Framework for adversarial attacks on NLP models
- [Counterfit](https://github.com/Azure/counterfit)  Microsoft's tool for assessing ML model security

### Data Poisoning & Model Integrity

- [Nightshade](https://nightshade.cs.uchicago.edu/)  Research on data poisoning attacks against generative models
- [Sleeper Agents (Anthropic Research)](https://www.anthropic.com/research/sleeper-agents-training-deceptive-llms-that-persist-through-safety-training)  Study on deceptive behaviors persisting through safety training

### Model Extraction & Inference

- [ML Privacy Meter](https://github.com/privacytrustlab/ml_privacy_meter)  Quantifying privacy risks of ML models
- [Stolen Model Research (USENIX)](https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/tramer)  Foundational work on model stealing attacks

---

##  LLM Security

Specific risks and defenses for Large Language Models in production.

| Resource | Focus |
|----------|-------|
| [OWASP LLM Top 10](https://genai.owasp.org/) | Prompt injection, insecure output handling, training data poisoning, etc. |
| [Prompt Injection Primer (Simon Willison)](https://simonwillison.net/series/prompt-injection/) | Deep exploration of prompt injection as an unsolved problem |
| [LLM Guard](https://github.com/protectai/llm-guard) | Open-source toolkit for LLM input/output validation |
| [Rebuff](https://github.com/protectai/rebuff) | Self-hardening prompt injection detector |
| [Garak](https://github.com/NVIDIA/garak) | NVIDIA's LLM vulnerability scanner |
| [PyRIT](https://github.com/Azure/PyRIT) | Microsoft's red teaming toolkit for generative AI |
| [Vigil](https://github.com/deadbits/vigil-llm) | LLM prompt injection detection |
| [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) | NVIDIA's framework for controllable AI applications |

---

##  MLOps & Supply Chain Security

Securing the ML pipeline from training to deployment.

- [SLSA Framework](https://slsa.dev/)  Supply chain integrity standard, applicable to ML pipelines
- [ModelScan](https://github.com/protectai/modelscan) Scan ML models for serialization attacks (pickle exploits, etc.)
- [Fickling](https://github.com/trailofbits/fickling)  Trail of Bits' Python pickle decompiler and analyzer
- [Sigstore](https://www.sigstore.dev/)  Signing and verification for software artifacts (models included)
- [HuggingFace SafeTensors](https://github.com/huggingface/safetensors)  Safe serialization format eliminating arbitrary code execution
- [ML-BOM (AI/ML Bill of Materials)](https://cyclonedx.org/capabilities/mlbom/)  CycloneDX specification for ML component tracking

### Key Reading

- [Securing the ML Supply Chain (Trail of Bits)](https://blog.trailofbits.com/)  Practical risks in model distribution
- [Compromised PyTorch Dependency (2022)](https://pytorch.org/blog/compromised-nightly-dependency/)  Real-world supply chain attack case study

---

##  AI Observability & Monitoring

You can't secure what you can't see. Monitoring AI workloads is a security function.

| Resource | Description |
|----------|-------------|
| [OpenTelemetry](https://opentelemetry.io/) | Vendor-neutral observability framework — increasingly supporting ML workloads |
| [VictoriaMetrics](https://victoriametrics.com/) | High-performance open-source TSDB for metrics at scale |
| [Prometheus + GPU Exporters](https://github.com/NVIDIA/dcgm-exporter) | NVIDIA DCGM exporter for GPU monitoring |
| [Arize Phoenix](https://github.com/Arize-AI/phoenix) | Open-source LLM observability and evaluation |
| [Langfuse](https://github.com/langfuse/langfuse) | Open-source LLM engineering platform (tracing, evals, monitoring) |
| [OpenLIT](https://github.com/openlit/openlit) | OpenTelemetry-native observability for GenAI & LLMs |
| [Evidently AI](https://github.com/evidentlyai/evidently) | ML model monitoring — data drift, performance degradation, bias detection |

### Why This Matters for Security

Model drift, anomalous inference patterns, unexpected latency spikes, and unusual token distributions can all be **early indicators of adversarial activity**. Observability is your first line of defense.

---

##  Governance, Regulation & Compliance

Navigating the evolving regulatory landscape.

### European Framework

- [EU AI Act — Official Text](https://artificialintelligenceact.eu/)  Risk-based classification and compliance requirements
- [ENISA AI Cybersecurity Guidelines](https://www.enisa.europa.eu/)  European cybersecurity agency guidance for AI
- [France — CNIL AI Guidance](https://www.cnil.fr/en/artificial-intelligence)  GDPR-specific guidance for AI systems
- [BSI (Germany) — AI Security Recommendations](https://www.bsi.bund.de/)  German federal office for information security

### International Standards

- [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html)  AI Management System standard
- [ISO/IEC 23894:2023](https://www.iso.org/standard/77304.html)  AI Risk Management guidance
- [NIST AI 100-2](https://www.nist.gov/artificial-intelligence)  Adversarial ML taxonomy and terminology

### Responsible AI

- [Anthropic Research Publications](https://www.anthropic.com/research)  Safety research from Claude's creators
- [Google Responsible AI Practices](https://ai.google/responsibility/responsible-ai-practices/)  Google's framework for responsible development
- [Partnership on AI](https://partnershiponai.org/)  Multi-stakeholder AI governance research

---

##  Hands-On Labs & Challenges

Learn by doing. Attack models, break pipelines, defend systems.

| Resource | Type | Difficulty |
|----------|------|------------|
| [Damn Vulnerable LLM Agent](https://github.com/WithSecureLabs/damn-vulnerable-llm-agent) | CTF |  Intermediate |
| [Gandalf (Lakera)](https://gandalf.lakera.ai/) | Challenge |  Beginner →  Advanced |
| [HackAPrompt](https://www.aicrowd.com/challenges/hackaprompt-2023) | Competition |  Intermediate |
| [AI Goat](https://github.com/dhammon/ai-goat) | Vulnerable Lab |  Intermediate |
| [MLSecOps Podcast Labs](https://mlsecops.com/) | Tutorial |  Beginner |
| [TensorFlow Privacy](https://github.com/tensorflow/privacy) | Library |  Advanced |
| [Adversarial ML Threat Matrix](https://github.com/mitre/advmlthreatmatrix) | Framework |  Intermediate |

---

##  Talks, Courses & Conferences

### Free Courses

- [NVIDIA — AI Security Fundamentals](https://www.nvidia.com/en-us/training/)  Self-paced, covers adversarial robustness
- [Google — Secure AI Framework (SAIF)](https://safety.google/cybersecurity-advancements/saif/)  Conceptual framework for secure AI
- [Hugging Face — ML for Security Course](https://huggingface.co/learn)  Community-driven learning paths
- [SANS — AI Security Resources](https://www.sans.org/)  Whitepapers and webcasts (free tier)

### Notable Talks

- **FOSDEM**  Security & HPC devrooms regularly feature AI security content
- **BlackHat / DEF CON AI Village** — Cutting-edge offensive AI security research
- **KubeCon**  MLOps and platform security sessions
- **OSMC**  Open-source monitoring including AI workload observability

### Podcasts

- [MLSecOps Podcast](https://mlsecops.com/podcast)  Dedicated to ML security operations
- [Risky Business](https://risky.biz/)  Infosec podcast, regularly covers AI risks
- [The TWIML AI Podcast](https://twimlai.com/)  ML research with security episodes

---

##  Learning Paths

###  I'm a Developer shipping ML models

1. Start with **OWASP ML Top 10** and **OWASP LLM Top 10**
2. Explore **ModelScan** and **SafeTensors** for supply chain basics
3. Practice with **Gandalf** and **Damn Vulnerable LLM Agent**
4. Implement **LLM Guard** or **NeMo Guardrails** in a test project

###  I'm a Security Engineer expanding to AI

1. Study **MITRE ATLAS** alongside your ATT&CK knowledge
2. Run **Garak** or **PyRIT** against a test LLM deployment
3. Explore **ART** for adversarial attack/defense simulation
4. Set up **AI observability** (Arize Phoenix + VictoriaMetrics) for anomaly detection

###  I'm a CISO / Decision-Maker evaluating AI risk

1. Read the **EU AI Act** risk classification and **NIST AI RMF**
2. Review **ISO/IEC 42001** for AI management system structure
3. Understand the **threat landscape** through MITRE ATLAS and ENISA reports
4. Define your organization's AI security policy using the governance resources

---

##  Community & Contribution

This is a living repository. Contributions are welcome.

### How to Contribute

1. **Fork** this repository
2. **Add resources** following the existing format — include name, link, and a brief description
3. Submit a **Pull Request** with a clear explanation of what you're adding and why

### Contribution Guidelines

- Resources must be **free and publicly accessible** (free tiers of commercial tools are acceptable)
- Prioritize **open-source, vendor-neutral** resources when possible
- Include a brief description — don't just drop links
- No affiliate links, sponsored content, or marketing material
- Respect **European digital sovereignty** — highlight EU-based alternatives when they exist

### Quality Criteria

- ✅ Actively maintained (updated within the last 12 months)
- ✅ Technically accurate and peer-reviewed when applicable
- ✅ Practical and actionable
- ❌ Abandoned projects or deprecated tools
- ❌ Paywalled content with no free tier
- ❌ Vendor-specific marketing disguised as education

---

##  License

This repository is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

You are free to share and adapt this material, as long as you give appropriate credit and distribute your contributions under the same license.

---

##  Philosophy

> *"The goal is not to create dependency, but to transfer competency."*

AI security is not a product you buy but it's a discipline you build. This repository exists because informed engineers and decision-makers are the best defense against the risks that come with deploying AI in the real world.



---

<p align="center">
  <em>Maintained with care from Europe 🇪🇺</em><br>
  <strong>Learn. Understand. Decide.</strong>
</p>
