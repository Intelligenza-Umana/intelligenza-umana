# Human-Verified Engineering (working title)
## Required review
Define the problem, constraints and threat model proportionate to risk. Explain design alternatives and trade-offs. AI output is untrusted until reviewed. The author must understand changed behavior and dependencies. Automated checks complement human judgment; passing tests is not proof of security.
## Verification
Use reproducible commands and fixtures; test normal, negative and regression cases. Where relevant test authorization boundaries, concurrency, transactions, rollback, malformed input and failure recovery. Record actual outcomes, not invented results. Distinguish untested assumptions from evidence. Review secrets, dependency risks, privacy and data integrity. Require independent review for high-risk changes before stable release; if unavailable, keep experimental status.
## Release
Document installation, supported versions, license, limitations, changelog and security reporting. Do not publish claims beyond evidence. Maintain a clear ownership and maintenance policy.
