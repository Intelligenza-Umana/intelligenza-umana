# Contributing

We start with a real problem, consider alternatives and verify results. Read the [manifesto](MANIFESTO.md). Issues and pull requests are welcome. The foundation is currently maintained by its founder; review happens as capacity allows and there is no guaranteed response time. You do not need write access or a particular level of seniority to contribute.

1. Check [beginner-friendly issues across the organization](https://github.com/search?q=org%3AIntelligenza-Umana+is%3Apublic+is%3Aissue+is%3Aopen+no%3Aassignee+label%3A%22good+first+issue%22&type=issues) or the [foundation issues](https://github.com/Intelligenza-Umana/intelligenza-umana/issues) and the [project registry](docs/PROJECT_REGISTRY.md). Open an issue in the relevant repository with the problem, context, evidence and expected outcome.
2. Discuss substantial or architectural changes before implementation. For a new project, use the [proposal template](lab/PROPOSAL_TEMPLATE.md).
3. Fork the repository, make a focused change and open a pull request. Explain your reasoning, verification commands and actual results, security and data-integrity implications, and known limitations. If a check could not be run, say so.
4. Respond to review and improve the change together. Maintainers decide whether and when to merge; a passing check alone does not constitute approval.

AI assistance is allowed. Contributors must understand, review and take responsibility for their changes and disclose material AI assistance. See the [engineering standard](docs/ENGINEERING_STANDARD.md), [definition of done](docs/DEFINITION_OF_DONE.md) and [code of conduct](community/CODE_OF_CONDUCT.md).

**Do not post vulnerabilities or secrets in public issues.** Follow the private reporting instructions in [SECURITY.md](SECURITY.md).

## First pull request

Fork the relevant public repository, clone your fork, create a focused branch, edit and test, commit and push to your fork, then open a PR against the upstream default branch. Ask questions when the scope or review feedback is unclear. Never claim checks you did not run.

## AI-agent skill submissions

Document inputs and untrusted or missing context, expected outputs and side effects, representative and failure examples, limitations, reproducible verification commands and actual results. Separate static package checks from runtime behavior; identify the tested host and version and mark untested hosts explicitly.

## Membership and permissions

Membership is optional and is reviewed manually, including applicants who demonstrate relevant experience outside IU. It does not automatically grant write or maintainer permissions. See [onboarding](community/ONBOARDING.md).
