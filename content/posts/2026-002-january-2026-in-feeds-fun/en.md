---
title = "January 2026 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-02-04T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in January 2026."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is a monthly recap of Feeds Fun.

- We made 4 releases. Numerous stability improvements and bug fixes were introduced.
- 2.5M news entries were loaded, 41 new users registered.

<!-- more -->

## Updates

**What improved for the users of [feeds.fun](https://feeds.fun)**:

- Improved performance, precission and stability of feeds discovery logic.
- Improved OPML import, now it better handles errors and displays user-friendly messages in case of problems.
- Tag filter is now case-insensitive.

**What improved for our self-hosted users**:

- Fixed an issue when tag processing failed because of using a custom LLM model via OpenAI-compatible API. Thanks [xylophoneengine](https://github.com/xylophoneengine) for reporting the issue and helping with debugging!
- Updated the [single-user](https://github.com/Tiendil/feeds.fun/blob/main/docs/examples/single-user) and [multi-user](https://github.com/Tiendil/feeds.fun/blob/main/docs/examples/multi-user) setup examples to reflect the changes in authentication system.
- Added the [third-party LLM models](https://github.com/Tiendil/feeds.fun/blob/main/docs/examples/third-party-models) example to demonstrate how to use any LLM model via provider with OpenAI-compatible API.

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

Tasks completed this month:

- [Improve registration & login interfaces](https://github.com/Tiendil/feeds.fun/issues/365)
- [Tokens estimation may fail with the third-party LLM setup](https://github.com/Tiendil/feeds.fun/issues/478)

New tasks added to the Roadmap:

- [Improve registration & login interfaces](https://github.com/Tiendil/feeds.fun/issues/365).
- [Consistent displaying of published/collected dates](https://github.com/Tiendil/feeds.fun/issues/480)
- [Mark all as read](https://github.com/Tiendil/feeds.fun/issues/479)

We continue working on other tasks from the "Quality of life" section of the Roadmap.

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for December 2025

- `2.5M` news entries were loaded.
- `41` new users registered.
- `~19.4 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
