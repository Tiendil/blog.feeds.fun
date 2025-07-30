---
title = "Take control of the number of tags you see"
tags = ["news", "releases", "documentation", "performance", "gui"]
published_at = "2025-07-30T12:00:00+00:00"
seo_description = "Update 1.20.5 introduces a new filter option to control the number of tags displayed in Feeds Fun, enhancing performance and usability."
seo_image = ""
---

In the recent `1.20.5` update ([check it now!](https://feeds.fun)), we introduced the news filter option `Show tags`.

It significantly reduces the number of tags loaded from the server by excluding rare ones.

The general rule is:

> If a tag is encountered in news less than N times, it is considered rare and excluded from the list of tags.

We consider that when dealing with thousands of news items daily, the tags appearing in just 1 or 2 news items are not particularly important most of the time.

Currently, the filter allows you to set the threshold to 2-5 tags, and, of course, you can load all tags if you want.

By default, the threshold is set to 2 (at least two news items with the tag should be present). That allows us to reduce the number of loaded tags up to 75% and the traffic up to 1.5 times!

In future updates, we plan to make filter settings persistent, so they save between sessions and devices.

**Please, tell us what you think about this feature!** We are eager to hear your feedback and suggestions on how to improve it further.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
