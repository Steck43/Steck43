# Landen Stecker

Security and AI engineer. Navy veteran. CISSP. I build at the intersection of security and AI, with a focus on coordinated multi-agent systems: building them, governing them, and defending them.

I started this work in the last year of my undergraduate degree in Cybersecurity Technology, building trading systems out of my own research before I held any professional certification. Running them taught me that an autonomous system holding keys, executing unattended, and ingesting outside data is an attack surface before it is a strategy, so I built it security-minded from the first commit. Encrypted credentials, secrets resolved at runtime instead of stored, graceful degradation under failure, and a refusal to feed my models any data I had not checked for tampering or poisoning.

That instinct was a student's, though, not yet a professional's. I knew the difference between building carefully and being able to stand behind a claim that a system handling real money was secure, and I did not yet have the second. Closing that gap is what came next. Security+ in October 2025, my B.S. conferred that December, and both the ISC2 CC and CISSP exams passed in early March 2026, a week apart, just before I began a full-time M.S. in Artificial Intelligence at Santa Clara.

The progression I care about is from securing the system to securing the decision it makes.

## What I'm building

My work centers on coordinated multi-agent systems, across three legs: build, govern, defend. The build leg is live. The govern and defend legs are in development.

**Build. [crypto-signal-confluence](https://github.com/Steck43/crypto-signal-confluence).** A research instrument that tests whether fusing volume, sentiment, and technical signals produces predictive edge under honest validation and realistic trading costs. It is not a profitable bot and does not claim to be. Edge on real data is unproven, and saying so plainly is the point. The repository carries purged cross-validation, a sentiment ablation, a transaction-cost study, and a clear account of what is validated, what is exploratory, and what is not yet tested.

**Govern. Policy engine (in development).** A governance layer that sits between an autonomous system's experts and its actions. It reads calibrated confidence and uncertainty, decides what is permitted, abstains when the signal is weak, and logs every input, decision, and rationale for audit. A fixed-weight ensemble cannot explain itself. A governed one can.

**Defend. St. Michael (in development).** The defend leg, pointed outward at adversarial and hostile agents. Protecting the integrity of a system's decisions against poisoned inputs and manipulation, not just the integrity of its host.

## Background

- Navy veteran, roughly seven years.
- B.S. Cybersecurity Technology, University of Maryland Global Campus, 2025. Computer science minor. Capstone in blockchain and machine learning.
- CompTIA Security+. ISC2 Certified in Cybersecurity. ISC2 CISSP.
- M.S. Artificial Intelligence, Santa Clara University. Full-time, in progress.

My focus is AI and agent security.
