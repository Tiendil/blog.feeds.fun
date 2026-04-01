title = "March 2026 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-04-01T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in March 2026."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is a monthly recap of Feeds Fun.

- We made 11 releases with interface improvements, new Gemini model support, and an updated news deprecation policy.
- 5.2M news entries were loaded, 32 new users registered.

<!-- more -->

## Updates

The most noticeable change for both [feeds.fun](https://feeds.fun) users and self-hosted users is the updated news deprecation policy.

The previous policy limited the maximum number of news entries per feed to 10000, which worked well for a long time, but, in the long run, it led to uncontrollable growth in database size and performance degradation.

The new policy keeps the 10000 news restriction, but also limits the age of news entries to 30 days. Since Feeds Fun is designed to be a tool for news discovery, a month looks like a reasonable time frame. This way, we can ensure that the database size remains manageable and the performance remains optimal. We also introduced a lower limit of 100 news entries per feed that cannot be removed by the deprecation policy — this should help keep low-traffic feeds manageable.

All these parameters can be configured in the self-hosted version — check [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md) for the details.

**What improved for users of [feeds.fun](https://feeds.fun)**:

- Coloring of tags on the rules view now respects the rule score.
- Active Gemini model changed to `gemini-2.5-flash-lite`.
- We split a huge scientific papers collection into multiple specialized collections, to simplify subscription to what really matters for you.
- Feeds Fun now correctly processes native feed tags (that are specified by the feed source) when they are in Unicode (i.e., when tags use non-English words). Huge thanks to [raphaelbahat](https://github.com/raphaelbahat) for reporting this issue.

**What improved for self-hosted users**:

Upgrading the self-hosted version requires manual operations. Please check the [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md) for the details.

- Feeds Fun now requires at least Postgres 18 as a database.
- We removed support for Gemini 2.0 models (they are deprecated by Google) and added support for Gemini 2.5.
- CLI command added `ffun feeds unlink <feed_ids>` to unlink feeds from all users.

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

We continue working on other tasks from the "Quality of life" section of the roadmap.

Our plans are dynamic, and we are always open to suggestions and improvements. React to tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for February 2026

- `5.2M` news entries were loaded.
- `32` new users registered.
- `~14.1 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
