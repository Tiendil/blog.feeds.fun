---
title = "December 2025 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-01-04T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in December 2025."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is the monthly recap of Feeds Fun.

- We made 1 huge release with a fully refactored registration & authentication system — made it more user-friendly and extensible.
- 2.5M news entries were loaded, 49 new users registered.

<!-- more -->

## Updates

**What improved for the users of [feeds.fun](https://feeds.fun)**:

Changes in our authentication system should be mostly invisible to you, what you may notice is:

- Simpler invitation to login or register on the [home page](https://feeds.fun) of the site.
- You can now log in with your Google, GitHub, or X (Twitter) accounts. If you've already registered with an email (which is the same as your social account's email), you'll be asked to confirm it. This way, you can link your social account to your existing Feeds Fun account.

**What improved for our self-hosted users**:

Some environment variables were renamed or removed. Please, check [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md) for the `1.22.0` version.

- If you host Feeds Fun in the single-user mode, no changes besides renaming some environment variables are required.
- If you host Feeds Fun in the multi-user mode, you should configure your own OIDC flow, including Identity Provider, and migrate your SuperTokens users there. We have [full-fledged example of multi-user setup](https://github.com/Tiendil/feeds.fun/tree/main/docs/examples/multi-user) with [Keycloak](https://www.keycloak.org/), [OAuth2-Proxy](https://oauth2-proxy.github.io/oauth2-proxy/) and [Caddy](https://caddyserver.com/).

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

- The task [Improve registration & login interfaces](https://github.com/Tiendil/feeds.fun/issues/365) is completed.

We continue working on other tasks from the "Quality of life" section of the Roadmap.

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for September 2025

- `2.5M` news entries were loaded.
- `49` new users registered.
- `~16.1 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
