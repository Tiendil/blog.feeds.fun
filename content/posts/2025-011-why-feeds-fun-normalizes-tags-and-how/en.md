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

Our strategy is to grow the set of normalization rules until we begin to normalize most of the tags we see in the wild into convenient-enough forms.

/// note | That means there are always may be "wrong" tags

Despite we strive to provide the best possible tags for each news entry, there is always a chance that some tags will be normalized to not-so-good form.

Especially, while Feeds Fun is young and the set of normalization rules is not so big yet.

You can always track our progress on the path to perfection on our [roadmap](https://github.com/users/Tiendil/projects/1), where we have the whole section dedicated to tagging improvements.

Just to give you an idea of possible mistakes (at the November 2025):

- Some proper names may be normalized to a wrong form: `emacs -> emac`, `arms-control -> arm-control`.
- Some special word forms may be normalized to a wrong form: `glasses-case -> glass-case`.

///


--------------

broken tags, `emacs` -> `emac`

check roadmap for our plant on tags normalization

note:

- this post will be updated, as new tag normalization rules will be added
- this post will be helpfull for those who self-host Feeds Fun or thoses who want depper understand how tags work

repost to:

- r/rss
- r/self-hosted
- r/pkms
- hackernews
- my twitter, bluesky, telegram
