---
title = "September 2025 in Feeds Fun"
tags = ["monthly-recap", "news"]
published_at = "2025-10-02T12:00:00+00:00"
seo_description = "Check out what happened in Feeds Fun in September 2025."
seo_image = ""
---

Hey everyone! This is the monthly recap of Feeds Fun.

Summary:

- We made 3 releases. Numerous stability improvements and bug fixes were introduced.
- Work on tags normalization, finally give some visible results, you should see much fewer tag duplicates now. Tag variations like `book-reviews`, `books-review`, `books-reviews`, `book-review` now automatically normalize to a one form `book-review`.
- 2.5M news entries were loaded, 37 new users registered.

<!-- more -->

## Updates

**What improved for the users of [feeds.fun](https://feeds.fun)**:

- Tag variations like `book-reviews`, `book-review` (and so on) now automatically normalize to a one suitable form. This should reduce the total number of tags you see in the GUI and improve the effect of rules, because they begin to apply to more news now.

ATTENTION: You may need to update your existing rules to use normalized tag forms, as some old rules may still use non-normalized forms. Or you can just wait — we'll migrate your old rules to normalized tag forms this month.

**What improved for our self-hosted users**:

- With tag normalization introduced, you may want to read [new section in README](https://github.com/Tiendil/feeds.fun/tree/main?tab=readme-ov-file#configure-tag-normalizers) and check the default [normalization configs](https://github.com/Tiendil/feeds.fun/blob/a2e96ecf21ad3e283b0d8f82deea8dd5806caeee/ffun/ffun/tags/fixtures/tag_normalizers.toml) — some normalizers may eat a significant amount of RAM and CPU time.

This is a brief recap; for a complete, detailed list of changes, please refer to our [CHANGELOG](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md).

## Roadmap

Do not forget about our [long-term development plans](https://github.com/users/Tiendil/projects/1/views/1?pane=info).

A bunch of new tasks were added to the roadmap after research on tag normalization:

- [Tag normalization: remove prefix/suffix parts of a tag to produce "parent" tag](https://github.com/Tiendil/feeds.fun/issues/421)
- [Tag normalization: abbreviations normalization](https://github.com/Tiendil/feeds.fun/issues/422)
- [Tag normalization: add parent locations for location tags](https://github.com/Tiendil/feeds.fun/issues/423)
- [Tag normalization: community-maintained tag synonyms database](https://github.com/Tiendil/feeds.fun/issues/424)
- [Tag normalization: using a synonym dictionary for tag normalization](https://github.com/Tiendil/feeds.fun/issues/425)
- [Tag normalization: normalize numbers in tags](https://github.com/Tiendil/feeds.fun/issues/426)
- [Tag normalization: removing suffixes from tag parts](https://github.com/Tiendil/feeds.fun/issues/427)
- [Tag normalization: extract idiomatic expressions that are part of a tag](https://github.com/Tiendil/feeds.fun/issues/428)
- [Tag normalization: normalize tags with pronouns](https://github.com/Tiendil/feeds.fun/issues/429)
- [Tag normalization: normalize auxiliary verbs](https://github.com/Tiendil/feeds.fun/issues/430)
- [Tag normalization: break tags by complex patterns](https://github.com/Tiendil/feeds.fun/issues/431)
- [Tag normalization: normalize interrogative words in tags](https://github.com/Tiendil/feeds.fun/issues/432)
- [Tag normalization: build tags ontology on top of a similarity metric](https://github.com/Tiendil/feeds.fun/issues/433)
- [Support setting up new tag normalizers as plugins](https://github.com/Tiendil/feeds.fun/issues/434)
- [Better (readable) tag names](https://github.com/Tiendil/feeds.fun/issues/435)
- [Tag normalization: normalize abbreviation special cases](https://github.com/Tiendil/feeds.fun/issues/440)

Currently, we are working on [improving registration & login interfaces](https://github.com/Tiendil/feeds.fun/issues/365).

Our plans are dynamic, and we are always open to suggestions and improvements. React to the tasks you like:

- **Like** to increase the priority of the task.
- **Comment** to help us better understand your needs.
- **Create a feature request** if we missed something important for you.

## Fun stats for June

- `2.5M` news entries were loaded.
- `37` new users registered.
- `~11.1 minutes` spent reading news in a day by an average active user.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
