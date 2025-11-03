---
title = "October 2025 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2025-11-03T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in October 2025."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is the monthly recap of Feeds Fun.

- We made 4 releases. Numerous stability improvements and bug fixes were introduced.
- ???
- 2.6M news entries were loaded, 46 new users registered.

<!-- more -->

## Updates

- ff-515 — Fixed displaying text on checkboxes in the GUI (some of them displayed inverted text).
- Tag normalizer now does not try to normalize technical tag parts `-dot-`, `-plus-`, `-sharp-`.
- ff-463 — Extended CLI `ffun cleaner` functionality to remove tags that are not assigned to any entry.
- ff-517 —



**What improved for the users of [feeds.fun](https://feeds.fun)**:

- Fixed behavior of checkboxes in the GUI (some of them displayed inverted state).

**What improved for our self-hosted users**:

- CLI command `ffun cleaner clean` now removes tags that are not assigned to any entry.
- Implemented CLI command `ffun cleaner renormalize-tags` — it goes through all tags in the database and tries to (re)normalize them according to the current configs. It updates the rules and tags of entries accordingly.

This is a brief recap; for a complete, detailed list of changes, please refer to our [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

New task added to the roadmap: [Tag normalization: protect proper names from changing](https://github.com/Tiendil/feeds.fun/issues/446).

Currently, we are working on [improving registration & login interfaces](https://github.com/Tiendil/feeds.fun/issues/365).

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for October 2025

- `2.6M` news entries were loaded.
- `6.1M` unique tags total in the system.
- `46` new users registered.
- `~13.5 minutes` spent reading news in a day by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
