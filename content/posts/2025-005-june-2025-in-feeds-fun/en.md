---
title = "June 2025 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2025-07-03T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in June 2025."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

This is the first monthly recap of Feeds Fun. We hope it will become a regular occurrence, allowing you to stay up-to-date with the project.

Summary:

- We made 7 releases. Numerous stability improvements and bug fixes were introduced.
- Feeds Fun should start better processing news from small, niche, and/or non-English sites.
- Self-hosted users should upgrade their `Supertokens` instance to `11.0.4` version.
- The [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info) has been published, and we have already received your feedback. Thanks for that!
- 1.3M news entries were loaded, 43 new users registered.

<!-- more -->

## Updates

**What improved for the users of [feeds.fun](https://feeds.fun)**:

- Better validation of the values in the user settings view.
- Feeds Fun now better understands and correctly processes news with broken Unicode characters.
- Feeds Fun now smartly processes broken markup in feeds and attempts to extract as many valid entries as possible.

As a result, we should start better processing news from small, niche, and/or non-English sites.

**What improved for our self-hosted users**:

- We upgraded our auth dependency — `Supertokens` to `11.0.4` version (from `9.0.2`). If you use a multi-user setup, you should migrate your `Supertokens` instance manually. See [Supertokens CHANGELOG](https://github.com/supertokens/supertokens-python/blob/master/CHANGELOG.md) for instructions.
- Backend upgraded to `Python 3.13`. All backend dependencies are upgraded to the latest versions.
- Improved stability of feed loading — more network errors are handled and processed correctly and silently.
- `ffun` CLI command now works correctly in the official Docker images.
- `ffun cleaner` now does a better job of cleaning orphaned entries and feeds.
- LLM tag processors now trim too big entries (according to `max_tokens_per_entry` model property) to avoid overspending tokens.
- Improved performance of saving tags into the database. This fix should reduce spikes of DB connections usage and improve overall performance of the backend.
- Added support for ZSTD compression for feed loading.

This is a short recap, the full detailed list of changes you may find in our [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

## Roadmap

A few weeks ago, we published our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

We would like to thank everyone who has already checked it out and provided feedback.

Based on your input, we added new tasks:

- [Automatic translation of news to the user's language](https://github.com/Tiendil/feeds.fun/issues/391), thanks to [imalyi](https://github.com/imalyi).
- [Smart suggestion of new rules based on likes/dislikes](https://github.com/Tiendil/feeds.fun/issues/390), thanks to [nezartarbin](https://github.com/nezartarbin).
- [Summarization of news entry by the user request](https://github.com/Tiendil/feeds.fun/issues/380), thanks to [nickyfoto](https://github.com/nickyfoto)
- [Use content as a news item text if the content attribute exists in the RSS/ATOM feed](https://github.com/Tiendil/feeds.fun/issues/382), thanks to [nickyfoto](https://github.com/nickyfoto)

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for June

- `1.3M` news entries were loaded.
- `43` new users registered.
- `4` users set their OpenAI/Gemini API keys to use LLM tag processors — thank you for your support!
- `~24 minutes` spent reading news in a day by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
