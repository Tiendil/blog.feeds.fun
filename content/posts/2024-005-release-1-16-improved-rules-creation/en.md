---
title = "Version 1.16 released — improved rules creation, added a new collection"
tags = ["news", "releases", "collections", "rules"]
published_at = "2024-28-12T20:00:00+00:00"
seo_description = ""
seo_image = ""
---

I'm excited to announce the release of **Feeds Fun version 1.16**!

This update brings a lot of cool features and improvements.

**Important:** Due to significant changes, all user settings, including API keys, have been reset. Please check and update your settings.

## What's New

### Improved collections interface and logic

- You can now subscribe to individual feeds from a collection or to the entire collection.
- Feeds from collections are marked in your feed list for easy recognition.
- Each feed in a collection comes with a detailed description.
- Best of all, **all feeds in collections are tagged for free for all users!**

The old collections (gamedev, artificial intelligence) have been removed because they didn't meet the new quality standards. From now more care will be put into creating collections.

**The first new collection contains all scientific papers from arXiv!** Now, you can always stay up to date with the latest scientific research!

### Gemini support

Support for the [Gemini API](https://ai.google.dev/), Google's alternative to OpenAI's ChatGPT, has been added. You can now use Gemini for tagging in addition to OpenAI's services. This is especially exciting because Gemini offers a free tier with a limited number of requests, so you can test all the features of Feeds Fun without any extra cost.

You can set your OpenAI or Gemini API key in the settings section of the Feeds Fun website.

If you're self-hosting Feeds Fun, please see the additional notes in the [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/changes/2024-10-12T09-11-16_1.12.0.md).

### Reduced number of duplicated news entries

Sometimes, users can see the same news item multiple times in the list of recent news. That is because the same news item can appear in different feeds from the same website. For example, that can happen for Reddit and arXiv feeds.

Now Feeds Fun will do a better job of detecting and removing such duplicates.

Thank you for your support! I hope you enjoy the new features!

## Stay Connected

- Our site: [feeds.fun](https://feeds.fun/)
- Our repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)


------------

Changes:

- ff-174 — Custom API entry points for OpenAI and Gemini clients.
- ff-175 — Export feeds to OPML file.
- ff-171 — Simplified rules creation:
  - The rules creation form was moved to the tags filter.
  - Rules now allow specifying excluded tags (will not apply if the news has any of them).
  - Tags under the news caption now behave as tags in the tags filter.
  - Button `[more]` on the tags line under the news caption now opens the whole news.
  - Openned news items now always show all tags.
  - Only a single news item now can be opened.
  - Performance of the News page improved 2-3 times.
- ff-172 — Added feeds collection "Entrepreneurship & Startups". Also added cli commands `ffun estimates entries-per-day-for-collection` and `ffun estimates entries-per-day-for-feed`
- ff-199 — Fixed Reddit feeds discovery.
