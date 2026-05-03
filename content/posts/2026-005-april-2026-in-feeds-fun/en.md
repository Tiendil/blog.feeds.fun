---
title = "April 2026 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2026-04-01T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in April 2026."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

Hey everyone! This is a monthly recap of Feeds Fun.

- We made 2 releases with improved support of popular news sources (YouTube, Reddit, GitHub, ArXiv, Hacker News) and better estimation of spending for those who set up API keys.
- 2.5M news entries were loaded, 31 new users registered.

<!-- more -->

## Updates

We introduced an integration plugin system to customize Feeds Fun's behavior for particular news sources.

From the box, Feeds Fun now provides better support for YouTube, Reddit, GitHub, ArXiv, and Hacker News. We'll continue adding new integrations; self-hosted users can add their own by following the documentation in the repository.

Thanks to the plugin system, Feeds Fun began to:

- correctly discover news feeds for the mentioned sources;
- better display news entries from those sources.

**What improved for users of [feeds.fun](https://feeds.fun)**:

- On the top of the opened news body, you can find a list of resources and entities it mentions: from the link to the authors' page to the comments, linked videos, and images.
- If an image or YouTube video is attached to the news entry, it will be displayed on top of the news body.
- YouTube videos inlined in the news body are now displayed as playable videos instead of empty spaces.
- API usage now takes into account failed requests (e.g., due to quota limits, access issues, etc.) and assumes their cost as zero. That should reduce cases of rapid, fake spending growth caused by failed requests.

**What improved for self-hosted users**:

- You can configure a list of integration plugins and implement your own plugins to customize Feeds Fun's behavior for particular news sources. Check [README](https://github.com/Tiendil/feeds.fun#configure-integrations-with-new-sources) for the details.
- Improved HTML cleaning for LLM needs, now it removes all semantically meaningless attributes such as `class`, `id`, `style`, etc. That should lead to fewer tokens spent.

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

We finished the task [Specialized display of news from major content providers](https://github.com/Tiendil/feeds.fun/issues/351).

New tasks were added to the Roadmap:

- [Tag processor to create a tag for each news author ](https://github.com/Tiendil/feeds.fun/issues/511)
- [Random news sorting](https://github.com/Tiendil/feeds.fun/issues/513)
- [Tag processor for integration-specific tags](https://github.com/Tiendil/feeds.fun/issues/512)
- [Transform relative URLs in the body of the news to absolute URLs](https://github.com/Tiendil/feeds.fun/issues/515)
- [Purify the entry title and body on the server side](https://github.com/Tiendil/feeds.fun/issues/514)

We continue working on other tasks from the "Quality of life" section of the roadmap.

Our plans are dynamic, and we are always open to suggestions and improvements. React to tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for April 2026

- `2.5M` news entries were loaded.
- `31` new users registered.
- `~13.8 minutes/month` spent reading news by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
