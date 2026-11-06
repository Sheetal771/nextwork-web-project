# Notifications go only to a Discord webhook, and Contact Messages are not stored

Notifications for each Contact Message are posted to a Discord webhook. We chose this over AWS SNS (the obvious choice in this AWS-learning repo) to avoid setting up AWS credentials on the Owner's laptop, and over SMTP or Slack because a Discord webhook needs no extra accounts or apps. Contact Messages are not saved anywhere, so the app stays stateless: if the webhook call fails, the only fallback is a server log line holding the full Contact Message.

## Consequences

- The webhook URL is a secret, read from the `DISCORD_WEBHOOK_URL` environment variable and never committed.
- A Contact Message sent while Discord is unreachable never reaches the Owner, and the Visitor still sees a success message.
- There is no spam protection because the app only runs locally. Revisit this, along with storage, before any public deployment.
