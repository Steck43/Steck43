<div align="center">

<img src="./assets/fig1-box-between.svg" width="720" alt="Figure 1. Box between floor and judge. Audit attests enforce. Identity is not a fifth plane." />

# Landen Stecker

**Agentic AI engineer and architect with security built in**

Navy Veteran &nbsp;&middot;&nbsp; CISSP

Security Architect for AI Coworkers

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
<img src="https://img.shields.io/badge/CISSP-ISC2-8A2BE2?style=flat-square" alt="CISSP" />
<img src="https://img.shields.io/badge/OWASP-LLM_Top_10-000000?style=flat-square&logo=owasp&logoColor=white" alt="OWASP LLM Top 10" />
<img src="https://img.shields.io/badge/MITRE-ATLAS-C8102E?style=flat-square" alt="MITRE ATLAS" />
<img src="https://img.shields.io/badge/NIST-AI_RMF-005EA2?style=flat-square" alt="NIST AI RMF" />
</p>

*From securing the system to securing the decision it makes.*

</div>

---

I built four escalation layers for AI agents. A decision can resolve at any level. It escalates due to ambiguity or contradiction the previous layer could not settle. I operate the gate on my own work and keep a hash-chained, append-only record that supersedes and never deletes.

Deterministic gating is applied risk management. The risk decision is made ahead of time by a person, written as policy, enforced in code the model cannot argue with, and recorded.

## What I am building

The design is four planes. Identity is the argument they take, not a fifth plane. The floor decides on structural facts before a call executes. The judge doubts, and it can subtract from what the floor allows. The box contains, and it sits between the two, so a contradiction runs somewhere disposable before a judge call is paid. The audit attests. The record is hash-chained and append-only. It supersedes and does not delete.

<p align="center">
  <img src="./assets/four-planes.svg" width="560" alt="Four planes: floor, box, judge, audit." />
</p>

<p align="center">
  <a href="https://github.com/Steck43/capability-gate"><img src="https://img.shields.io/badge/floor-capability--gate-1f6feb?style=flat-square" alt="capability-gate" /></a>
  <a href="https://github.com/Steck43/aegis-atoms"><img src="https://img.shields.io/badge/atoms-aegis--atoms-238636?style=flat-square" alt="aegis-atoms" /></a>
  <a href="https://github.com/Steck43/isolation-layer"><img src="https://img.shields.io/badge/box-isolation--layer-8b949e?style=flat-square" alt="isolation-layer" /></a>
  <a href="https://github.com/Steck43/owasp-dual-top10-lab"><img src="https://img.shields.io/badge/lab-owasp--dual-000000?style=flat-square" alt="owasp-dual-top10-lab" /></a>
  <a href="https://github.com/Steck43/newwave-owasp-security-lab"><img src="https://img.shields.io/badge/earlier-newwave-6e7781?style=flat-square" alt="earlier-newwave" /></a>
  <a href="https://doi.org/10.5281/zenodo.22018052"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.22018052-informational?style=flat-square" alt="Zenodo DOI" /></a>
</p>

| Plane | Repository | State |
|---|---|---|
| Floor | [capability-gate](https://github.com/Steck43/capability-gate) | built and tested |
| Atom plane | [aegis-atoms](https://github.com/Steck43/aegis-atoms) | built and tested |
| Box | [isolation-layer](https://github.com/Steck43/isolation-layer) | built and tested |
| Judge | same mount as atoms | built and tested |
| Evidence | [dual-lab](https://github.com/Steck43/owasp-dual-top10-lab) &middot; [newwave](https://github.com/Steck43/newwave-owasp-security-lab) | built and tested |

**The floor. [capability-gate](https://github.com/Steck43/capability-gate).** A deny-by-default capability gate for an AI agent's tool calls. A call outside the grant does not execute. Deterministic code makes the decision. It fails closed, and the host runtime still fails open if a hook throws. The decision log is hash-chained. A deleted, truncated or rewritten log makes the gate deny, and the same OS user can still rewrite the log, its witness and its anchor together. Signed checkpoint verification is built and tested. No hook passes a checkpoint yet, and there is no public signer. Concept record: [10.5281/zenodo.22018052](https://doi.org/10.5281/zenodo.22018052). OWASP Agentic: ASI02 denies an unlisted tool, ASI05 denies shell and code tools unless granted, ASI01 limits impact without detecting a hijack, and ASI10 is the kill switch. Counts and test ids: see the repo.

**The atom plane. [aegis-atoms](https://github.com/Steck43/aegis-atoms).** Polarity-free facts, with a bounded subtract-only judge. The judge can concur, flag, tighten or escalate. It cannot widen. Live load is untested live, and judge apply is off by default. The triad plugin is not mounted. OWASP Agentic tags in the tree include ASI02, ASI03, ASI04, ASI05, ASI06, ASI01 with ASI09, and ASI10. Suite result: see the repo.

**The box. [isolation-layer](https://github.com/Steck43/isolation-layer).** One Firecracker microVM per task under the jailer. Built and tested on its own tree. `always_invoked` is design intent, so the full path is untested live. Docker is runtime, packaging and test infrastructure, never the isolation boundary. gVisor is a named fallback, not a shipped runtime. ASI05 is the class this contains. See the repo for the boot record.

**The labs.** [owasp-dual-top10-lab](https://github.com/Steck43/owasp-dual-top10-lab) holds one scenario per Agentic code, ASI01 through ASI10. Status of each row: see the repo. [newwave-owasp-security-lab](https://github.com/Steck43/newwave-owasp-security-lab) is the earlier course lab. It cites the Agentic list and does not ship a mapping.

## How I think

The floor decides, the judge doubts, the box contains, the audit attests. Fail closed, and put the limit in the same sentence as the claim. A default allow is a named decision, not an inherited accident. Enforcement sits at the point of action. A human stays the gate on irreversible actions. Authority is earned in stages and verified before it expands.

The bounded judge comes from my ML work: uncertainty-aware voting, ensemble orchestration, and confidence-based abstention. In [crypto-signal-confluence](https://github.com/Steck43/crypto-signal-confluence) `src/machine_learning/ml_ensemble.py`, each model's vote is weighted by its confidence and the signal is hold when neither side clears `decision_threshold = 0.6`. In [aegis-atoms](https://github.com/Steck43/aegis-atoms) `bounded_judge.py` a low-confidence opinion retries, then escalates to a human and returns the floor verdict. The final decision stayed with me on the signals. No return is claimed.

## How I work

Independent adversarial review before merge. Known gaps stay as strict expected failures. A fix claim needs a strip test that goes red when the fix is removed. CI pins its own guard files by hash and, on a pull request, loads the guard from the base branch. That pin is built and tested. It is not a required check on the default branch.

An audit trail toward SOC 2 is the record: hash-chained, append-only, and checkable by someone who does not trust the operator. The same-user rewrite limit above is part of that sentence.

## Background

Nearly seven years in Navy security operations. As a plank owner I stood up the security program for a new NATO installation, rewrote the base's SOPs, PPRs (pre-planned responses) and playbooks at every escalation level, qualified 50+ watchstanders, and passed the certification inspection it was commissioned on. I led installation security operations on watch, responsible for about 50 people. I supervised 10 to 15 on watch daily, ran accountability for 40 to 50 in base operations, briefed the commanding officer and command triad every morning on security posture, and led recurring physical risk and vulnerability assessments. Titles I use: Security Operations Manager, Department Lead, Billet Watch Commander.

M.S. Artificial Intelligence in progress at Santa Clara University. B.S. Cybersecurity Technology. CISSP, Security+.

Founding security engineer at an early-stage agent-security startup. Shadow mode at three enterprise clients for about four weeks before enforcement. Designed for a single client fleet of over 1,000 agents, with per-client isolated delivery.

<details>
<summary>How this work started</summary>

I started this work in the last year of my undergraduate degree in Cybersecurity Technology, building trading systems out of my own research before I held any professional certification. Running them taught me that a system holding keys, executing unattended, and ingesting outside data is an attack surface before it is a strategy, so I built it security-minded from the start. Encrypted credentials, secrets resolved at runtime instead of stored, graceful degradation under failure, and a refusal to feed my models any data I had not checked for tampering or poisoning.

That instinct was a student's, though, not yet a professional's. I knew the difference between building carefully and being able to stand behind a claim that a system handling real money was secure, and I did not yet have the second. Closing that gap is what came next. Security+ in October 2025, my B.S. conferred that December, and both the ISC2 CC and CISSP exams passed in early March 2026, a week apart, just before I began a full-time M.S. in Artificial Intelligence at Santa Clara.

</details>

## Earlier work

**[cpt-reimbursement-engine](https://github.com/Steck43/cpt-reimbursement-engine).** A dependency-free TypeScript engine that predicts where Medicare reimbursement fails, not just whether a code exists.

**[crypto-signal-confluence](https://github.com/Steck43/crypto-signal-confluence).** A research instrument that tests whether fusing volume, sentiment, and technical signals holds up under purged cross-validation and realistic costs. Edge on real data is unproven.

## Links

[capability-gate](https://github.com/Steck43/capability-gate) · [aegis-atoms](https://github.com/Steck43/aegis-atoms) · [isolation-layer](https://github.com/Steck43/isolation-layer) · [owasp-dual-top10-lab](https://github.com/Steck43/owasp-dual-top10-lab) · [newwave-owasp-security-lab](https://github.com/Steck43/newwave-owasp-security-lab)

Landen Stecker, agentic AI engineer and architect with security built in.
