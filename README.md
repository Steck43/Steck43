<div align="center">

# Landen Stecker

**Security architect for AI agents**

CISSP &nbsp;&middot;&nbsp; M.S. Artificial Intelligence, Santa Clara University
&nbsp;&middot;&nbsp; Navy veteran

[![OpenSSF bestpractices.dev][bp-badge]][bp] [![DOI][doi-badge]][doi]

</div>

> **The helpfulness is the hazard.** A capable agent without context or bounds does not
> refuse. It fills the gap with a guess and acts, with real permissions.

So the control cannot live inside the model. I build the control that sits in front of
every action an AI agent takes, and answers three questions: who allowed this action, how
do we stop it now, and how do we prove what happened.

![Where the gate sits between people, the agent, aegis-atoms and isolation-layer][fig]

## Three repos, one system

**[capability-gate][cg]** decides each tool call before it runs. Deny by default, a kill
switch, and every decision on a hash-chained log before the agent hears it.
[One command][demo] shows it working. 34 mutation checks each remove one control, and
its test must fail.

**[aegis-atoms][atoms]** holds small policy rules and a judge that may tighten a verdict,
never loosen it. Built and tested; not measured live.

**[isolation-layer][il]** runs a risky task in its own Firecracker microVM under the
jailer. Live jailed runs are in its [receipts][il-receipts]. Wiring the gate's isolate
route to the real box is the next step.

**Research.** [owasp-dual-top10-lab][dual] maps the OWASP Top 10 for LLM and agentic apps
to MITRE ATLAS techniques, CVEs and AI incidents. [newwave-owasp-security-lab][nw] is
the earlier course lab.

## How I work

- Every control ships with a test that fails when the control is removed.
- Observe before enforce: watch real traffic, then write the policy.
- The limit sits next to the claim.
- Independent review before anything merges.

## Background

Nearly seven years of Navy security operations across Bahrain, Poland and Norfolk.
Built the security program for a NATO installation from construction to commissioning.
Led a fifty-person security department at Naval Station Norfolk as Security Operations
Manager (billet: Watch Commander).

M.S. Artificial Intelligence at Santa Clara University, in progress. B.S. Cybersecurity
Technology. CISSP, ISC2 CC, CompTIA Security+ and A+.

<details>
<summary>Earlier work</summary>

**[cpt-reimbursement-engine][cpt].** A dependency-free TypeScript engine that predicts
where Medicare reimbursement fails, not just whether a code exists.

**[crypto-signal-confluence][csc].** A research instrument that tests whether fusing
volume, sentiment and technical signals holds up under purged cross-validation and
realistic costs. Edge on real data is unproven.

</details>

[fig]: assets/gate-in-system.png
[bp-badge]: https://www.bestpractices.dev/projects/16124/badge
[bp]: https://www.bestpractices.dev/projects/16124
[doi-badge]: https://zenodo.org/badge/DOI/10.5281/zenodo.22018052.svg
[doi]: https://doi.org/10.5281/zenodo.22018052
[cg]: https://github.com/Steck43/capability-gate
[demo]: https://github.com/Steck43/capability-gate#see-it-work
[atoms]: https://github.com/Steck43/aegis-atoms
[il]: https://github.com/Steck43/isolation-layer
[il-receipts]: https://github.com/Steck43/isolation-layer/tree/main/receipts
[dual]: https://github.com/Steck43/owasp-dual-top10-lab
[nw]: https://github.com/Steck43/newwave-owasp-security-lab
[cpt]: https://github.com/Steck43/cpt-reimbursement-engine
[csc]: https://github.com/Steck43/crypto-signal-confluence
