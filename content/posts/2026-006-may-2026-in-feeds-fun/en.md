---
title = "May 2026 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-04-01T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in May 2026."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is a monthly recap of Feeds Fun.

- We made 4 releases, improving broken feed parsing, Reddit posts parsing, and internal tagging logic.
- Per-feed `entries/day` statistics introduced to better understand feed activity.
- 2.5M news entries were loaded, 21 new users registered.

<!-- more -->

## Updates

**What improved for users of [feeds.fun](https://feeds.fun)**:

- In the `Feeds` view you can find a new column with an average news/day metric for each feed. If you click on a feed, you'll find a detailed 30-day feed activity chart in the feed details.
- In the feed details on the `Feeds` view, you can now found both urls: the feed URL and the website URL of the feed source.
- When parsing feeds, entries with malformed external URLs now do not cause the whole feed parsing to fail.
- Improved parsing and visualization of a special case of `video+text` Reddit posts.

**What improved for self-hosted users**:

- We refactored how tag processor get entries to process: from going over all entries to queue-based dispatching.
- As a result, we partially changed the configuration of tag processors. Now it should be more clear and agile. Check [changelog](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md) for `1.27.0` version for instrouctions on how to update your custom `tag_processors.toml` configs.

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

We finished the task [Add information about the intensity of the news flow for each feed](https://github.com/Tiendil/feeds.fun/issues/225).

We continue working on other tasks from the "Quality of life" section of the roadmap.

Our plans are dynamic, and we are always open to suggestions and improvements. React to tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for May 2026

- `2.5M` news entries were loaded.
- `21` new users registered.
- `~13.9 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
