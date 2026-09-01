---
title = "August 2026 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-08-01T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in August 2026."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is a monthly recap of Feeds Fun.

- We made 2 releases, introducing quality-of-life improvements in the interface, and the foundation for the upcoming "news tokens" system.
- 2.6M news entries were loaded, and 12 new users registered.

<!-- more -->

## Updates

**What improved for all users:**

- We improved the styles of buttons and info panels to make them more consistent and visually appealing.
- We changed visual markers for "read" and "unread" news entries. "Read" news entries no longer shift to the right.
- At the top of the News view, you may notice a new tools panel. Currently, it contains only a news tokens counter. In the future, the panel will contain tools to interact with news entries, such as "mark all as read", free text search, and more.

**What improved for self-hosted users**:

We started moving away from user-provided API keys to a "news tokens" system because of the security risks of storing API keys and the inconvenience for users in managing the resources they spend on news processing.

Please follow the instructions in the [changelog](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md) to upgrade your self-hosted instance to the latest version.

You don't need to change your tag processors configuration to keep the old behavior.

The new approach is a single admin-owned API key per LLM processor, with optional tokens granted to users by the admin. The user spends one token per news entry processed by all tag processors. You can change the `FFUN_DISPATCHER_ENFORCE_ENTITLEMENTS` setting to switch between "we tag all news for every user" and "we tag only news for users with tokens" modes.

There are three types of tokens:

- **daily tokens** — fixed amount of tokens refilled every day.
- **monthly tokens** — fixed amount of tokens refilled every month.
- **lifetime tokens** — one-time granted tokens that never expire.

Tokens are spent from the daily pool first, then the monthly pool, then the lifetime pool.

You can grant tokens to users via the `ffun benefits` CLI tool. To do that, you should:

1. Configure benefit packages; we have an [example](https://github.com/Tiendil/feeds.fun/tree/main/docs/examples/single-user-with-entitlements).
2. Grant a benefit package to a user either as a subscription period (for daily or monthly tokens) or as a one-time grant (for lifetime tokens).

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

We finished the task [Consistent display of published/collected dates](https://github.com/Tiendil/feeds.fun/issues/480). That finishes the "Quality of life" plans for the core functionality of Feeds Fun; however, we'll continue making small interface improvements.

We'll focus on the unfinished tracks from the roadmap's core stage.

Our plans are dynamic, and we are always open to suggestions and improvements. React to tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for August 2026

- `2.6M` news entries were loaded.
- `12` new users registered.
- `~37.3 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
