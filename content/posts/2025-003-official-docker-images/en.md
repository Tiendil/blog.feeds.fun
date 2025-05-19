---
title = "Official Docker images released"
tags = ["news", "docker"]
published_at = "2025-05-19T12:00:00+00:00"
seo_description = "Official Docker images for Feeds Fun are now available."
seo_image = ""
---

Hey!

We are glad to announce that **official Docker images** for Feeds Fun are now available!

Check examples of how to run Feeds Fun with Docker:

- [single-user setup](https://github.com/Tiendil/feeds.fun/tree/main/docs/examples/single-user)
- [multi-user setup](https://github.com/Tiendil/feeds.fun/tree/main/docs/examples/multi-user)

The images:

- [tiendil/feeds-fun-backend](https://hub.docker.com/r/tiendil/feeds-fun-backend) — all logic related to the backend.
- [tiendil/feeds-fun-frontend-data](https://hub.docker.com/r/tiendil/feeds-fun-frontend-data) — just copies frontend static data to wherever you need it.

Using examples should be as easy as pie:

```
git clone git@github.com:Tiendil/feeds.fun.git
cd ./feeds.fun/docs/examples/single-user
docker compose up -d
```

After services are up, you can access the web interface at [http://localhost/](http://localhost/)

Each example has an extensive README file; all config files are well commented.

But just in case, if you have any questions, feel free to post an issue on GitHub or make a pull request with your changes. We'll be grateful for feedback.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
