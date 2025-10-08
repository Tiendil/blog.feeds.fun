---
title = "Why Feeds Fun normalizes tags and how"
tags = ["documentation", "tags"]
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
- You look for a deepper understanding of how tags work in Feeds Fun.
- You self-host Feeds Fun and want to configure tag normalization.
- You are interested in tagging and approaches to it.

///

Tags are the real source of power in Feeds Fun. They allow you to rank, filter and sort news how you want, saving your time and energy.

Hovewer, tagging is not so simple as it seems. There is no strict definition of what a tag is, nor there is a standard for naming them.

We may agree, that tag is a some short string that describes the text or a part of it. But…

- How short it should be, is `this-text-is-about-modern-politics-in-the-central-asia` a tag or not?
- What about `ourdays-politics` and `modern-politics` — are they different tags or forms of the same one?
- Which one of the tags `book-review`, `book-reviews`, `books-review`, `books-reviews` should we use?

There are numerous questions like that, and no clear answers.

The situsation even more complicated, because Feeds Fun uses different independent sources of tags, named "tag processors", each of them may have its own rules and conventions for tags. Some tags even come from the feed itself and, therefore, may take any form.

## Are multiple tag forms a problem?

Imagine you are interested in news about science fiction books and want prioritize them in your feed.

The rule should be simple, like: "if the news entry is about book(s) and science fiction, then increase its score by 10".

However, with at least 4 tags for book reviews: `book-review`, `book-reviews`, `books-review`, `books-reviews` and at least 3 tags for science fiction: `science-fiction`, `sci-fi`, `scifi` you will ned to create `4 * 3 = 12` (!) rules to cover all the possible combinations.

It will be really inconvenient, and you will probably miss some of the tags or combinations, and, therefore, miss some of the news you are interested in.

That is why Feeds Fun tries its best to normalize tags — convert different forms of the same tag to a single canonical form.

To allow you creating a single rule like `book-reviews + science-fiction => +10` that will cover all the news you are interested in.

## Feeds Fun approach to tags normalization

There is no standard for tags and we don't want to invent one. Instead, we use a set of [heuristics](https://en.wikipedia.org/wiki/Heuristic) that bring most of the tags (but not every) to a canonical form. By canonical we mean a form that is readable-enough and understandable-enough to be convenient for most of the users.

Our strategy is to grow the set of normalization rules until we cover most of the tags we see in the wild. We call such rules "tag normalizers".

You can find the detailed description of the current tag normalization rules in our [repository](https://github.com/Tiendil/feeds.fun/blob/main/ffun/ffun/tags/fixtures/tag_normalizers.toml)

Here let's briefly discuss the meta-heuristics we follow.

### The simple tag is a good tag

The shorter and preciser the tag is, the easier it is to use it.

We try to simplify tags without losing their meaning:

- Remove "unnecessary" parts, like `a`, `the`, `now`, and so on: `a-book-review` => `book-review`, `things-that-make-me-happy` => `things-make-me-happy`.
- Prefere single-part tags over multi-part ones, if single-part is idiomatic enough: `e-mail` => `email`, `web-site` => `website`, `to-do` => `todo`.
- Prefere general terms over jargon: `cuz-i-can` => `because-i-can`.

### Two simple tags are better than one complex

Between `animation-in-video-games` and `animation + video-games` we prefer the latter.

It may seems that having a lot of hyper-specialized tags is good for creating precise rules. However, in practice it leads to tag explosion, when each news entry is accompanied by dozens of rare tags that are not suitable for most of users.

Also, complex tags are harder to produce: it is much simpler to detect that an article is about `animation` or `video-games` than to detect that it is exectly about `animation-in-video-games`. Complex tags approach leads not only to tag explosion, but also to loss of information.

At the same time, the loss of precision in rules is not so significant, because of the power of Feeds Fun rules system. There are multiple approachers to target posts related to `animation-in-video-games`:

- Create two rules `animation => +5` and `video-games => +5`, so that posts about both topics will get +10.
- Create a rule `animation + video-games => +10` to target posts about both topics.

You can tune the ranking with negative rules in pair to positive one if required, like:

- `animation => -3` to reduce the score of all posts about animation, so most of them will have rank below 0, except those who are ranked with one of above rules.
- `animation + not video-games => -5` to reduce the score of posts about animation outside video games;
- `animation + cartoon => -5` to reduce the score of posts about specific animation topic.

### There should be only one canonical form of a tag

A single not-so-readable tag is better than multiple readable once, because it simplifies the rules creation and navigation.

Our current approach is to iterate over combinations of singular/plural forms of each part of the tag and choose the statistically most probable one.

For example, for book reviews, we try forms `book-review`, `book-reviews`, `books-review`, `books-reviews` and choose `book-review`.

This approach works for most of the tags, but there are some special cases described below, that we plan fix as we grow the set of normalization rules.

### 99.9…% of correctly normalized tags is enough

Despite we strive to provide the best possible tags for each news entry, there is always a chance that some tags will be normalized to a not-so-good form. Mostly because human languages are complex as our culture and reality — there are always exceptions to the rules.

You can always track our progress on the path to perfection on our [roadmap](https://github.com/users/Tiendil/projects/1), where we have the whole section dedicated to tagging improvements.

Just to give you an idea of possible mistakes (at the November 2025):

- Some proper names may be broken: `emacs` => `emac`.
- Some terms can lose meaning: `arms-control` => `arm-control`.
- Some special word forms may be normalized wrongly: `glasses-case` => `glass-case`.
- There may be multiple versions of the tags with abbreviations: `ai-regulation`, `artificial-intelligence-regulation`.

## How to help make Feeds Fun better

We need your feedback on our tagging system, tell us how you use it or how it can be improved.

There are two special places where you can share your thoughts on tags:

- Comment tasks in our [roadmap](https://github.com/users/Tiendil/projects/1).
- Tell us your ideas or report tag-related problems in [megathread on Reddit](https://www.reddit.com/r/feedsfun/comments/1o186to/place_for_tag_ideas_reports/).

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
