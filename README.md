<div align="center">

# Landen Stecker

**AI &amp; Agent Security Engineer** &nbsp;&middot;&nbsp; Navy Veteran &nbsp;&middot;&nbsp; CISSP

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/CISSP-ISC2-8A2BE2?style=flat-square" alt="CISSP" />
<img src="https://img.shields.io/badge/OWASP-LLM_Top_10-000000?style=flat-square&logo=owasp&logoColor=white" alt="OWASP LLM Top 10" />
<img src="https://img.shields.io/badge/MITRE-ATLAS-C8102E?style=flat-square" alt="MITRE ATLAS" />
<img src="https://img.shields.io/badge/NIST-AI_RMF-005EA2?style=flat-square" alt="NIST AI RMF" />
</p>

*From securing the system to securing the decision it makes.*

</div>

---

I build at the intersection of security and AI. The focus is the containment layer for autonomous agents: the deterministic boundary that decides what an agent is allowed to do before it does it.

I started this work in the last year of my undergraduate degree in Cybersecurity Technology, building trading systems out of my own research before I held any professional certification. Running them taught me that an autonomous system holding keys, executing unattended, and ingesting outside data is an attack surface before it is a strategy, so I built it security-minded from the first commit. Encrypted credentials, secrets resolved at runtime instead of stored, graceful degradation under failure, and a refusal to feed my models any data I had not checked for tampering or poisoning.

That instinct was a student's, though, not yet a professional's. I knew the difference between building carefully and being able to stand behind a claim that a system handling real money was secure, and I did not yet have the second. Closing that gap is what came next. Security+ in October 2025, my B.S. conferred that December, and both the ISC2 CC and CISSP exams passed in early March 2026, a week apart, just before I began a full-time M.S. in Artificial Intelligence at Santa Clara.

## What I'm building

The design is three planes. A deterministic floor decides on structural facts before a call executes. A bounded adjudicator above it can only subtract from what the floor allows. Isolation contains whatever neither can settle.

**The floor. [capability-gate](https://github.com/Steck43/capability-gate).** A deny-by-default capability gate for an AI agent's tool calls. Every tool call that reaches the gate is checked against an allowlist before it runs, and a call outside what the skill was granted does not execute. Deterministic code makes the decision, not the model being guarded against. It fails closed, fails loud on a bad policy, and logs every decision before the action runs. Configured in enforce on my own Hermes profile, after a documented observe, would-deny, adjudicate chain. Least privilege at an agent's point of action.

**The adjudicator.** Built and measured, not consumed in live adjudication. Bounded and subtract-only: concur, flag, tighten, escalate, never widen. A prompt-injected judge therefore degrades to denial of service rather than privilege escalation. A paid model sitting in an authorization path is also a denial-of-wallet surface, so it refuses before issuing once its budget is spent, and exhaustion returns the floor's verdict rather than opening or blocking.

**Isolation.** Firecracker microVM under the jailer, a six-crate Rust tree, sub-second jailed boot. Built on its own tree and not consumed by the gate.

## What I broke first

**[newwave-owasp-security-lab](https://github.com/Steck43/newwave-owasp-security-lab).** A hands-on OWASP LLM Top 10 security lab. An unsafe versus hardened finance assistant with archived live-model evidence, seven of the ten risks demonstrated, mapped to MITRE ATLAS and NIST AI RMF. Honest about which risks are demonstrated and which are in progress. LLM10 Unbounded Consumption is one of the seven, and it is the same risk the budget control above is built against: demonstrated in one repository, defended in another.

## Other work

**[crypto-signal-confluence](https://github.com/Steck43/crypto-signal-confluence).** A research instrument that tests whether fusing volume, sentiment, and technical signals produces predictive edge under honest validation and realistic trading costs. It is not a profitable bot and does not claim to be. Edge on real data is unproven, and saying so plainly is the point. The repository carries purged cross-validation, a sentiment ablation, a transaction-cost study, and a clear account of what is validated, what is exploratory, and what is not yet tested.

**[cpt-reimbursement-engine](https://github.com/Steck43/cpt-reimbursement-engine).** A dependency-free TypeScript engine that predicts where Medicare reimbursement fails, not just whether a code exists. Forty-nine tests validated against CMS actuals. Every output is computed at runtime rather than hardcoded, tagged with its provenance, and routed to review instead of a confident wrong answer when the signal is weak.

## Background

- Navy veteran, nearly seven years.
- B.S. Cybersecurity Technology, University of Maryland Global Campus, 2025. Computer science minor. Capstone work in blockchain and machine learning, and an APT32 threat risk analysis using MITRE ATT&amp;CK.
- CompTIA Security+. ISC2 Certified in Cybersecurity. ISC2 CISSP.
- M.S. Artificial Intelligence, Santa Clara University. Full-time, in progress.

My focus is AI and agent security.
