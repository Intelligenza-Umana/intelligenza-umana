# Contributing

Thanks for being here. Whether you want to fix something small, share an idea or ask a question, you are welcome to contribute. You do not need write access, prior open-source experience or a particular level of seniority. The foundation is maintained by its founder, and reviews happen as time allows, so replies may take a while.

## Find a place to start

Not sure where to start? Browse the [open issues](https://github.com/Intelligenza-Umana/intelligenza-umana/issues) in the repository that interests you. The [project registry](docs/PROJECT_REGISTRY.md) can help you choose a repository. A small, clearly scoped issue is a good first step; if the repository uses a `good first issue` label, look for that too. You do not need to arrive with a complete solution.

Before you begin, read the issue and any linked discussion. If the goal or scope is unclear, ask a question in the issue; asking first is welcome and helps everyone agree on what a good solution looks like. If you have noticed a problem that is not tracked yet, open an issue with its context, evidence and expected outcome. For a larger or architectural change, start a discussion before implementing it. For a new project, use the [proposal template](lab/PROPOSAL_TEMPLATE.md).

## Fork, make a branch and open a pull request

1. On GitHub, open the repository and select **Fork**. This gives you a copy to work on under your account.
2. Clone your fork and enter the repository directory:

   ```sh
   git clone https://github.com/YOUR-USERNAME/intelligenza-umana.git
   cd intelligenza-umana
   ```

   Replace `YOUR-USERNAME` with your GitHub username. If you are contributing to another repository in the [project registry](docs/PROJECT_REGISTRY.md), replace `intelligenza-umana` with that repository's name.
3. Create a branch for your change:

   ```sh
   git switch -c docs/short-description
   ```

4. Make a focused change, then run the relevant checks and note the commands and actual results. Commit and push your branch to your fork:

   ```sh
   git add path/to/changed-file
   git commit -m "Describe your change"
   git push -u origin docs/short-description
   ```

   Replace `path/to/changed-file` with the path to your changed file, and `short-description` with a few words describing your change.

5. When you are ready, open a pull request from your fork's branch to the original repository's `main` branch. Describe the problem and your change, include verification commands and results, and mention security or data-integrity implications and known limitations. If you could not run a check, just say so.
6. Review feedback is a normal part of contributing. If a comment is unclear, ask; you and the reviewers can work through the change together. Maintainers decide whether and when to merge, and a passing check alone is not approval.

## Submitting an AI-agent skill

If you are sharing a new or changed skill, this checklist helps other people understand and verify it:

- [ ] **Inputs:** Say what context or parameters the skill expects, and how it handles missing or untrusted input.
- [ ] **Outputs:** Describe the expected result, its format and any side effects.
- [ ] **Examples:** Show a representative input and expected output; include an error or edge case when relevant.
- [ ] **Limitations:** State unsupported cases, dependencies, risks and when a person should review the result.
- [ ] **Verification:** Give reproducible setup steps and exact commands, with actual results. Separate tests of the skill's files from tests of its behavior in a host.
- [ ] **Host behavior:** Name each host and version you actually tested and what you checked, such as installation, discovery or invocation. Mark other hosts or behaviors as untested assumptions; evidence from one host does not verify another.

The [engineering standard](docs/ENGINEERING_STANDARD.md) explains evidence and verification expectations. Check the [project registry](docs/PROJECT_REGISTRY.md) for known project status and host-verification gaps; don't claim support beyond what you tested.

AI tools are fine to use. Please understand, review and take responsibility for your changes, and disclose material AI assistance. See the [engineering standard](docs/ENGINEERING_STANDARD.md), [definition of done](docs/DEFINITION_OF_DONE.md) and [code of conduct](community/CODE_OF_CONDUCT.md).

Please do not post vulnerabilities or secrets in public issues. If you find a vulnerability, follow the private reporting instructions in [SECURITY.md](SECURITY.md).
