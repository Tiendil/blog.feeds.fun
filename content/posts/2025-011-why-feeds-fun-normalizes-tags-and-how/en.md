---
title = "Why Feeds Fun normalizes tags and how"
tags = ["documentation", "tags"]
published_at = "2025-10-12T12:00:00+00:00"
seo_description = ""
seo_image = ""
---

<!-- TODO: add documentation section -->
<!-- TODO: add cover image -->
<!-- TODO: add seo_cover image -->
<!-- TODO: add seo_description -->

Tags are the real source of power in Feeds Fun. They allow you to rank, filter and sort news how you want, saving you time and energy.

Hovewer, tagging is not so simple as it seems. There is no strict definition of what a tag is, nor there is a standard for naming them.

We may agree, that tag is a some short string that describes the text or a part of it. But…

- How short it should be, is `this-text-is-about-modern-politics-in-the-central-asia` a tag or not?
- What about `politics` or `modern-politics` — are they different tags or the same?
- Which one of the tags `book-review`, `book-reviews`, `books-review`, `books-reviews` should we use?

There are numerous questions like that, and no clear answers.

The situsation even more complicated, because Feeds Fun uses different independent sources of tags, named `tag processors`, each of them may have its own rules and conventions for tags.

## Are multiple tag forms a problem?

Imagine you are interested in news about science fiction books and want prioritize them in your feed.

The rule should be simple like `if the news entry is about book(s) and science fiction, then increase its score by 10`.

However, with at least 4 tags for book reviews: `book-review`, `book-reviews`, `books-review`, `books-reviews` and at least 3 tags for science fiction: `science-fiction`, `sci-fi`, `scifi` you will have to create `3 * 4 = 12` (!) rules to cover all the possible combinations.

It will be really inconvenient, and you will probably miss some of the tags or combinations, and, therefore, miss some of the news you are interested in.

That is why Feeds Fun tries its best to normalize tags, so that different forms of the same tag will be converted to a single canonical form.

So, you'll be able to create a single rule like `book-reviews + science-fiction -> +10` and be sure that it will cover all the possible tag forms and all the news you are interested in.

## Feeds Fun approach to tags normalization

<!-- the first sentence is awkward, try to reformulate -->

Since there is no standard for tags, we don't try to invent one. Instead, we use a set of simple [heuristics](https://en.wikipedia.org/wiki/Heuristic) that bring most of the tags (but not every) to a common form.

Our strategy is to grow the set of normalization rules until we begin to normalize most of the tags we see in the wild into convenient-enough forms. We call such rules `tag normalizers`.

/// note | There are always may be "wrong" tags

Despite we strive to provide the best possible tags for each news entry, there is always a chance that some tags will be normalized to a not-so-good form.

Especially, while Feeds Fun is young and the set of normalization rules is not so big yet.

You can always track our progress on the path to perfection on our [roadmap](https://github.com/users/Tiendil/projects/1), where we have the whole section dedicated to tagging improvements.

Just to give you an idea of possible mistakes (at the November 2025):

- Some proper names may be normalized to a wrong form: `emacs -> emac`.
- Some terms may be normalized to a wrong form: `arms-control -> arm-control`.
- Some special word forms may be normalized to a wrong form: `glasses-case -> glass-case`.
- There may be multiple versions of the tags with abbreviations: `ai-regulation`, `artificial-intelligence-regulation`.

///

You can find detailed descriptions of the current tag normalization rules in our [repository](https://github.com/Tiendil/feeds.fun/blob/main/ffun/ffun/tags/fixtures/tag_normalizers.toml)

Here let's briefly discuss the general approaches we choose.

### The simple tag is a good tag

The shorter and preciser the tag is, the easier it is to use it.

We try to simplify tags without losing their meaning:

- Remove unnecessary parts, like `a`, `the`, `now`, and so on: `a-book-review -> book-review`, `things-that-make-me-happy` -> `things-make-me-happy`.
- Prefere single-part tags over multi-part ones, if single-part is idiomatic enough: `e-mail -> email`, `web-site -> website`, `to-do -> todo`.
- Prefere general terms over jargon: `cuz-i-can -> because-i-can`.

### Two simple tags are better than one complex

Between `animation-in-video-games` and `animation + video-games` we prefer the latter.

It may seems that having a lot of hyper-specialized tags is good for precise targeting news by rules, but in practice it leads to tag explosion, when each news entry is accompanied by dozens of rare tags that are not suitable for most of users.

Also, complex tags are harder to produce: it is much simpler to detect that an article is about `animation` or `video-games` than to detect that it is exectly about `animation-in-video-games`. So, complex tags approach leads not only to tag explosion, but also to loss of relevant news.

The loss of precision in rules is not so significant, because of the power of Feeds Fun rules system. There are multiple approachers to target posts about `animation-in-video-games`:

- Create two rules `animation -> +5` and `video-games -> +5`, so that posts about both topics will get +10.
- Create a rule `animation + video-games -> +10` to target posts about both topics.

You can tune the ranking with negative rules in pair to positive one if required, like:

- `animation -> -3` to reduce the score of all posts about animation, so most of them will have rank below 0, except those who are ranked with one of above rules.
- `animation + not video-games -> -5` to reduce the score of posts about animation outside video games;
- `animation + cartoon -> -5` to reduce the score of posts about cartoon animation.


--------------

broken tags, `emacs` -> `emac`

check roadmap for our plant on tags normalization

we organize normalizers in a chain

tell about how we treat native feed tags

note:

- this post will be updated, as new tag normalization rules will be added
- this post will be helpfull for those who self-host Feeds Fun or thoses who want depper understand how tags work

repost to:

- r/rss
- r/self-hosted
- r/pkms
- hackernews
- my twitter, bluesky, telegram

Move arrows out of code blocks (?)

-----

add standard links suffix
