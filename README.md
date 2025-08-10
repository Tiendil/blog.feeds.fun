
# The content of the Feeds Fun [blog](https://blog.feeds.fun)

[feeds.fun](https://feeds.fun) — news reader with tags. Self-hosted, if it is your way.

- Reader automatically assigns tags to news.
- You create rules to score news by tags.
- Filter and sort news how you want  ⇒ read only what you want.

Blog is powered by [Brigid](https://github.com/Tiendil/brigid).


# After Brigid update

We need to recompile our custom theme after each Brigid upgrade.

```
rm -rf ./default-css/theme-templates/*
poetry run python -m brigid.cli templates copy ../default-css/theme-templates/
```
