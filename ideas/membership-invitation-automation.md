# Membership invitation automation

- ID: IU-IDEA-001
- Created: 2026-11-27
- Last reviewed: 2026-11-27
- Area: Community / operations
- Status: Deferred
- Related: [Onboarding](../community/ONBOARDING.md), [membership request template](../.github/ISSUE_TEMPLATE/membership_request.md), [website](https://github.com/Intelligenza-Umana/intelligenza-umana-web)

## Context and problem

Today an applicant voluntarily opens a public membership issue (or contacts the community privately). An organization owner evaluates the request and manually sends an official GitHub invitation. Membership starts only after the recipient accepts. Contributors do not need membership.

At the current early stage, manually inviting people is inexpensive and gives owners direct control. Repeated manual invitations may become unnecessary friction if the community grows.

## Proposed approach (not approved for implementation)

Use an issue-label event, for example `membership-approved`, as an explicit approval signal. A GitHub Actions workflow could obtain a short-lived installation token from a narrowly scoped GitHub App, verify authorization and send an invitation through the GitHub REST API.

Candidate flow:
1. Applicant submits a membership request using the existing form.
2. An authorized organization owner reviews it and applies the approval label.
3. Automation validates the repository, issue type, actor, current approval and applicant identity using trusted GitHub metadata (issue author and stable user ID, not arbitrary issue-body text).
4. Check whether membership or an invitation already exists; if eligible, send an invitation as a regular member, never as owner.
5. Record a minimal result, notify maintainers on failure and distinguish invitation pending from accepted membership. Acceptance remains voluntary and external to the workflow.

## Requirements and safeguards

- Never auto-approve requests or grant elevated repository, team or administrative permissions.
- Only explicitly authorized owners may approve; do not trust a label or repository write access alone. Verify actor authority at execution time and handle label removal or withdrawn applications before sending.
- Verify current API permissions and organization policies before implementation. Prefer a GitHub App with the minimum organization Members permission required; scope installation and credentials appropriately. No credentials in Git, logs or issue comments.
- Treat issue contents and usernames as untrusted input. Never interpolate issue data directly into shell scripts. Use trusted code from a protected branch and pin external actions.
- Make retries idempotent and prevent concurrent duplicate invitations; handle existing members, pending/expired invitations, rate limits, API errors and insufficient permissions safely.
- Keep a manual fallback; preserve the private request route and existing voluntary membership policy.
- Avoid exposing email addresses, private requests, sensitive applicant data or tokens in public issues or logs. Record only necessary audit metadata with appropriate access.

## Alternatives and trade-offs

- Keep manual invitations: simplest, no extra infrastructure or credentials; preferred today.
- Add an approval label solely to track review, while owners still invite manually.
- Build a dedicated app/admin interface only if actual volume justifies its complexity. Do not build a public automatic join endpoint.

## Revisit criteria

Revisit when membership requests arrive regularly and manual invitations consume meaningful maintainer time, or when several authorized maintainers need a consistent approval process. No numeric threshold or deadline has been approved; review against observed volume and security/maintenance cost.

## Acceptance criteria if promoted

- A valid owner approval results in exactly one regular-member invitation to the actual applicant.
- Unauthorized approvals, withdrawn requests, invalid issues and attempts to escalate privileges never invite anyone.
- Duplicate events and retries do not duplicate invitations; errors are visible to maintainers without leaking secrets.
- Invitation and accepted membership remain distinct; no user is enrolled without consent.
- Positive and negative cases are tested with mock API responses and a controlled test organization before production.
- Documentation, credential rotation/revocation, audit and manual fallback are verified.

## Decision and follow-up

2026-11-27: defer. The founder prefers to retain the current manual process while demand is low. No workflow, GitHub App, token, permissions or invitation automation is created by this note.

Reference for future verification: [GitHub REST API — organization members and invitations](https://docs.github.com/en/rest/orgs/members). API details and permissions must be rechecked when work is approved.
