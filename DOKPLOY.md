# Dokploy deployment notes

This is a pinned operational mirror of PostHog's hobby deployment.

Differences from upstream installer:
- Caddy is removed; PostHog web/capture binds only to `POSTHOG_BIND_ADDRESS:POSTHOG_PORT`.
- Default bind is Dokploy's tailnet address `100.81.252.96:18000`.
- Other upstream host ports are removed; services communicate over the Compose network.
- Generated `compose/` entrypoints are committed for reproducible Dokploy deployments.

Set `SITE_URL` to the exact tailnet endpoint, `POSTHOG_SECRET`, `ENCRYPTION_SALT_KEYS`, and a pinned `POSTHOG_APP_TAG` in Dokploy.

Upstream snapshot: 4c9e6031ade0d73bd3bf479c190cf9a3999d3b57
