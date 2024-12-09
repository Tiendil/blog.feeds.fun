---
title = "Short Summary of the Last Two Months of Feeds Fun"
tags = ["news", "performance"]
published_at = "2024-10-12T20:00:00+00:00"
seo_description = "Short summary of the last two month updates of Feeds Fun: performance improvements."
seo_image = ""
---

I don't want to bother you with a post per release (there were 15 of them since the last post), instead I'll periodically post summaries of the most significant updates. Hope, it is more convinient for everyone. If you are interested in every release, you can always subscribe to the [repository](https://github.com/Tiendil/feeds.fun) or check the [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

The actual version of Feeds Fun is 1.14.2.

There are few significant improvements in the last two months:

1. Time to load the latest news is reduced 4 times!
2. LLM prompts are improved to produce less tags of better quality.
3. Fixed a situation when, after removing a feed on the Feeds page, the feeds list was not updated.
4. Added tracking of some user activity events.

I want to add a few words about tracking events.

Events are required to better understand how users interact with the reader, how they use it, where they have difficulties, and so on. It is especially important for Feeds Fun, because a lot of its functionality are experimental and it is too easy to choose wrong direction of work, for example, to implementing interface that no one require or choose wrong feature to improve. Tracking such events will help to faster deliver right features.

All new events are for internal use only:

- no one of them leave Feeds Fun server;
- no one of them directly attached to email or other personal info.
