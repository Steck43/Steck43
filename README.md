<div align="center">

# Landen Stecker

**Security & AI Engineer** &nbsp;·&nbsp; Navy Veteran &nbsp;·&nbsp; CISSP

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

I build at the intersection of security and AI, on coordinated multi-agent systems: building them, governing them, defending them. My focus is the deterministic boundary that decides what an autonomous agent is allowed to do, and enforces it at the point of action.

## What I'm building

**Shipped. Four public repositories.**

<table>
  <tr>
    <td><a href="https://github.com/Steck43/capability-gate"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Steck43&repo=capability-gate" alt="capability-gate" /></a></td>
    <td><a href="https://github.com/Steck43/newwave-owasp-security-lab"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Steck43&repo=newwave-owasp-security-lab" alt="newwave-owasp-security-lab" /></a></td>
  </tr>
  <tr>
    <td><a href="https://github.com/Steck43/cpt-reimbursement-engine"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Steck43&repo=cpt-reimbursement-engine" alt="cpt-reimbursement-engine" /></a></td>
    <td><a href="https://github.com/Steck43/crypto-signal-confluence"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Steck43&repo=crypto-signal-confluence" alt="crypto-signal-confluence" /></a></td>
  </tr>
</table>

**[capability-gate](https://github.com/Steck43/capability-gate).** A deny-by-default capability gate for an agent's tool calls. Every tool call is checked against an allowlist before it runs, and a call outside what the skill was granted does not execute. Deterministic code makes the decision, not the model being guarded against. It fails closed, fails loud on a bad policy, and logs every decision before the action runs. Running live on an agent in observe mode, building its enforce policy from real behavior. Least privilege at an agent's point of action.

**[newwave-owasp-security-lab](https://github.com/Steck43/newwave-owasp-security-lab).** An OWASP LLM Top 10 security lab with live model evidence. An unsafe versus hardened finance assistant, with real attacks and their mitigations demonstrated against a live model and mapped to OWASP LLM, MITRE ATLAS, and NIST AI RMF.

**[cpt-reimbursement-engine](https://github.com/Steck43/cpt-reimbursement-engine).** A deterministic TypeScript engine that predicts whether a procedure or device will actually be reimbursed under Medicare OPPS, not just whether a code exists. Status and APC validation, five real failure modes, every output computed at runtime and tagged with its provenance, and a design that abstains rather than guess when the signal is weak.

**[crypto-signal-confluence](https://github.com/Steck43/crypto-signal-confluence).** The origin was a signal generator I ran over Telegram and hand-traded for over a year at a net profit. This is the next iteration: automating that manual edge to remove emotional bias and cover the session handoffs across Asia, Europe, and the US that no one can trade awake around the clock. A research instrument, not a profitable bot. Whether the automated edge holds under purged cross-validation and realistic costs is unproven, and saying so plainly is the point.

**In development.**

**Govern.** A governance layer that sits between an autonomous system's experts and its actions. It reads calibrated confidence and uncertainty, decides what is permitted, abstains when the signal is weak, and logs every input, decision, and rationale for audit. A fixed-weight ensemble cannot explain itself. A governed one can. The same containment idea turned outward, defending a system's decisions against poisoned inputs and manipulation rather than only its host, is the direction after it.

## Background

I came into this building trading systems out of my own research before I held any certification, and running them taught me that an autonomous system holding keys and ingesting outside data is an attack surface before it is a strategy. I built security-minded from the first commit. That instinct was a student's, though, not yet a professional's, and closing that gap is what came next.

- Navy veteran, roughly seven years.
- B.S. Cybersecurity Technology, University of Maryland Global Campus, 2025. Computer science minor. Capstone in blockchain and machine learning.
- CompTIA Security+ (2025). ISC2 Certified in Cybersecurity and CISSP (early 2026, a week apart).
- M.S. Artificial Intelligence, Santa Clara University. Full-time, in progress.

My focus is AI and agent security.
