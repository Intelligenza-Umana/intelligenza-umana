# Community platform integrations

- ID: IU-IDEA-002
- Created: 2026-11-28
- Area: Community / operations
- Status: Deferred

## Current decision

GitHub is the source of truth for repositories, issues, pull requests, releases and project evidence. Discord is the structured discussion space; Sentinel assists with moderation and owner-approved administration. Membership is optional and manually reviewed. No additional platform, bot, credential or infrastructure is created by this note.

## Incremental options

1. A single Discord channel for selected public GitHub events (new issues, opened/merged pull requests, releases). Start with a native GitHub-compatible Discord incoming webhook, or a small filtered integration if needed. Avoid forwarding all pushes, comments or stars by default.
2. If event volume warrants it, use an organization webhook or GitHub App to receive repository and pull_request events. Verify signatures, use delivery IDs for deduplication, handle retries/rate limits, and route by immutable repository ID. Sentinel or a narrowly scoped worker may create a discussion channel/thread for a public repository after an explicit policy/approval; avoid auto-provisioning channels for private, archived or inactive repositories. Preserve manual permissions and never grant administrative access. Filter private payloads, secrets, mentions and sensitive issue content; do not expose private repositories or membership requests in public channels.
3. Consider one optional Telegram group (no bot or broadcast channel initially) only if contributors actually want it. Do not duplicate technical discussions or decisions across chat platforms: link to GitHub. No invite exists yet. Do not publish a placeholder link. A future Telegram integration would require separate authorization and an actual demonstrated need.
4. Twitch or other public channels may be explored if the community grows and people want live collaboration or educational content. No publishing schedule or commitment.

## Revisit criteria

Prefer manual coordination until maintaining notifications, discussion channels or membership consumes meaningful time. Start with one low-noise notification channel if useful, measure its value, then extend only after reviewing failures and privacy. Do not automatically create a Discord channel for every repository simply because the event exists.

## References

- [Discord incoming webhooks](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks)
- [GitHub webhook events and payloads](https://docs.github.com/en/webhooks/webhook-events-and-payloads)
- [Organization webhooks](https://docs.github.com/en/rest/orgs/webhooks)

Recheck permissions, event support and API details before implementation.
