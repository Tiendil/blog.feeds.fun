---
title = "Why Feeds Fun normalizes tags — and how"
tags = ["documentation", "tags", "rules"]
published_at = "2025-10-12T12:00:00+00:00"
seo_description = "How Feeds Fun normalizes tags and why it is important."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

/// note | Read this post if

- You want to use Feeds Fun rules more efficiently.
- You're looking for a deeper understanding of how tags work in Feeds Fun.
- You self-host Feeds Fun and want to configure tag normalization.
- You are interested in tagging and approaches to it.

///

Tags are the real source of power in Feeds Fun. They allow you to rank, filter, and sort news how you want, saving your time and energy.

However, tagging is not as simple as it seems. There is no strict definition of what a tag is, nor is there a standard for naming them.

We may agree that a tag is a short string that describes the text or part of it. But…

- How short should it be? Is `this-text-is-about-modern-politics-in-central-asia` a tag or not?
- What about `nowadays-politics` and `modern-politics` — are they different tags or forms of the same tag?
- Which one of the tags `book-review`, `book-reviews`, `books-review`, `books-reviews` should we use?

There are numerous questions like that, and no clear answers.

The situation is even more complicated because Feeds Fun uses multiple independent sources of tags, called "tag processors", each of which may have its own rules and conventions for tags. Some tags even come from the feed itself and, therefore, may take any form.

## Are multiple tag forms a problem?

Imagine you are interested in news about science fiction books and want to prioritize them in your feed.

The rule should be simple, such as:

> If a news entry is about books and science fiction, then increase its score by 10 points.

However, with at least 4 tags for book reviews `book-review`, `book-reviews`, `books-review`, `books-reviews`, and at least 3 tags for science fiction `science-fiction`, `sci-fi`, `scifi`, you will need to create `4 * 3 = 12` rules to cover all the possible combinations.

It will be really inconvenient, and you would probably miss some of the tags or combinations, and therefore, miss some of the news you are interested in.

That is why Feeds Fun tries its best to normalize tags — to convert different forms of the same tag to a single canonical form.

This allows you to create a single rule, such as `book-reviews + science-fiction => +10`, that will cover all the news you are interested in.

## Feeds Fun's approach to tag normalization

There is no standard for tags, and we don't want to invent one. Instead, we use a set of [heuristics](https://en.wikipedia.org/wiki/Heuristic) that convert most tags to a canonical form. By "canonical" we mean a form that is readable enough and understandable enough to be convenient for most users.

Our strategy is to grow the set of normalization rules until we cover most tags we see in the wild. We call such rules "tag normalizers".

You can find the detailed description of the current tag normalization rules in our [repository](https://github.com/Tiendil/feeds.fun/blob/main/ffun/ffun/tags/fixtures/tag_normalizers.toml)

Here, let's briefly discuss the high-level heuristics we follow.

/// note | Standartized representation as the basis for normalization

Before we start normalizing anything, we should have it in some standardized representation.

In the case of Feeds Fun it is a hyphen-separated lowercase ASCII string in English, for example: `book-review`, `science-fiction`, `300-spartans`.

It is not the only best possible representation — just plain and simple enough to work with.

///

## English as the base language

One concept can be expressed in different languages, keeping the same meaning: `book`, `книга`, `livre`, `Buch`, `كتاب`.

Feeds Fun uses English as the base language for tags, so all tags are translated to English before any further processing.

We plan to support other languages in the future by translating already normalized tags to different languages. That should help us to keep normalization rules simple and effective, without losing the expressiveness of tags.

## A simple tag is a good tag

The shorter and more precise the tag is, the easier it is to use.

We try to simplify tags without losing their meaning:

- Remove "unnecessary" parts, like `a`, `the`, `now`, and so on: `a-book-review` => `book-review`, `things-that-make-me-happy` => `things-make-me-happy`.
- Prefer single-part tags over multi-part ones, if single-part is idiomatic enough: `e-mail` => `email`, `web-site` => `website`, `to-do` => `todo`.
- Prefer general terms over jargon: `cuz-i-can` => `because-i-can`.

## Two simple tags are better than one complex

Between `animation-in-video-games` and `animation + video-games`, we prefer the latter.

It may seem that having a lot of hyper-specialized tags is beneficial for creating precise rules. However, in practice, it leads to tag explosion, when each news entry is accompanied by dozens of rare tags that are not suitable for most users.

Also, complex tags are harder to produce: it is much simpler to detect that an article is about `animation` or `video-games` than to detect that it is precisely about `animation-in-video-games`. That means the complex-tag approach not only leads to tag explosion but also results in a loss of information.

At the same time, the loss of precision in rules is not so significant, due to the power of Feeds Fun's rule system. There are multiple ways to target posts related to `animation-in-video-games`:

- Create two rules: `animation => +5` and `video-games => +5`, so that posts about both topics will get +10.
- Create a rule `animation + video-games => +10` to target posts about both topics.

You can tune the ranking with negative rules paired with positive ones if needed, like:

- `animation => -3` to reduce the score of all posts about animation, so most of them will have a rank below 0, except those that are ranked with one of the above rules.
- `animation + not(video-games) => -5` to reduce the score of posts about animation outside of video games;
- `animation + cartoon => -5` to reduce the score of posts about a specific animation topic.

## A not-so-good canonical form is better than no canonical form

A single not-so-readable tag is better than multiple readable ones because it simplifies rule creation and navigation.

Our current approach is to iterate over combinations of singular/plural forms of each part of the tag and choose the statistically most probable one.

For example, for book reviews, we try forms `book-review`, `book-reviews`, `books-review`, `books-reviews` and choose `book-review`.

This approach works for most tags, but there are some complicated cases described below that we plan to fix as we grow the set of normalization rules.

## 99.9…% of correctly normalized tags is enough

Although we strive to provide the best possible tags for each news entry, there is always a chance that some tags may be normalized to a not-so-good form. This is mostly because human languages, as well as our culture and reality, are complex — there are always exceptions.

You can always track our progress on the path to perfection on our [roadmap](https://github.com/users/Tiendil/projects/1), where we have a whole section dedicated to tagging improvements.

Just to give you an idea of possible mistakes (as of October 2025):

- Some proper names may be broken: `emacs` => `emac`.
- Some terms can lose meaning: `arms-control` => `arm-control`.
- Some special word forms may be normalized wrongly: `glasses-case` => `glass-case`.
- There may be multiple tag versions for abbreviations: `ai-regulation`, `artificial-intelligence-regulation`.

## How to help make Feeds Fun better

We need your feedback on our tagging system. Please, tell us how you use it and how it can be improved.

There are two special places where you can share your thoughts on tags:

- Comment on tasks in our [roadmap](https://github.com/users/Tiendil/projects/1).
- Tell us your ideas or report tag-related problems in the [megathread on Reddit](https://www.reddit.com/r/feedsfun/comments/1o186to/place_for_tag_ideas_reports/).

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
