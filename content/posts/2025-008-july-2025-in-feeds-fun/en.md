---
title = "July 2025 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2025-08-03T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in July 2025."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is the monthly recap of Feeds Fun.

Summary:

- We made 5 releases. Numerous stability improvements and bug fixes were introduced.
- Greatly reduced the number of tags loaded & displayed in the UI.
- Improved parsing of OPML files produced by other RSS readers.
- 2.3M news entries were loaded, 100 new users registered.

<!-- more -->

## Updates

**What improved for the users of [feeds.fun](https://feeds.fun)**:

- We introduced the [show tags]{post:take-control-of-the-number-of-tags-you-see} news filter option. It reduces the number of tags loaded from the server by excluding rare ones. By our measurements, it allows us to reduce the number of loaded tags up to 75% and the traffic up to 1.5 times!
- Feeds Fun now better parses OPML files produced by other RSS readers, which allows you to import your feeds from other readers more easily.

**What improved for our self-hosted users**:

- Improved processing of some Gemini API errors related to content policy violations.

This is a short recap; the complete detailed list of changes you may find in our [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

Currently, we are working on [improving the quality of the generated tags](https://github.com/Tiendil/feeds.fun/issues/56).

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for June

- `2.3M` news entries were loaded.
- `100` new users registered.
- `9` users set their OpenAI/Gemini API keys to use LLM tag processors — thank you for your support!
- `~9.5 minutes` spent reading news in a day by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
