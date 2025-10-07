---
title = "Short summary of the last two months of Feeds Fun"
tags = ["news", "performance"]
published_at = "2024-10-12T20:00:00+00:00"
seo_description = "Short summary of the last two month updates of Feeds Fun: performance improvements."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

It's been a productive two months for Feeds Fun!

I don't want to bother you with a post for every release (there have been 15 since the last post). Instead, I'll periodically post summaries of the most significant updates. I hope this approach is more convenient for everyone. If you're interested in every release, you can always subscribe to the [repository](https://github.com/Tiendil/feeds.fun) or check the [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

The current version of Feeds Fun is **1.14.2**.

Here are the most significant improvements from the last two months:

1. The time to load the latest news has been reduced by a factor of 4!
2. LLM prompts have been improved to produce fewer tags of better quality.
3. Fixed an issue where, after removing a feed on the Feeds page, the feeds list was not updated.
4. Added tracking of some user activity events.

### A Few Words About Tracking Events

Event tracking is essential to better understand how users interact with the reader, how they use it, where they face difficulties, and more. This is particularly important for Feeds Fun because much of its functionality is experimental, and it's easy to head in the wrong direction — such as implementing an interface no one needs or prioritizing the wrong feature for improvement. Tracking these events will help deliver the right features more quickly.

All new events are strictly for internal use:

- None of the events leave the Feeds Fun server.
- None of the events are directly tied to email addresses or other personal information.
