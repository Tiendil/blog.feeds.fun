---
title = "External authentication support for self-hosted Feeds Fun"
tags = ["releases", "documentation", "news", "tutorial"]
published_at = "2025-12-26T12:00:00+00:00"
seo_description = "Feeds Fun now supports authentication via external services, making self-hosting in multi-user mode easier."
seo_image = "./cover.jpg"
---

/// brigid-images
src = "./cover.jpg"
alt = "Blog post cover image."
///

We'd like to share that Feeds Fun now supports authentication via external services.

We moved away from the SuperTokens-coupled approach because it was too restrictive and resulted in vendor lock-in.

That means Feeds Fun should be much easier to self-host in multi-user mode. Simply put, you only need to pass two headers from your authentication proxy to the Feeds Fun backend — and you're good to go.

Single-user mode is still supported as well and does not require any authentication setup at all.

Check an [example of a multi-user setup](https://github.com/Tiendil/feeds.fun/tree/main/docs/examples/multi-user) in our repo.

<!-- more -->

It is as easy as running these two steps:

```
# Step 1 — add custom domains to /etc/hosts

# Add the following lines to /etc/hosts (remove leading #):
# 127.0.0.1 feeds.fun.local
# 127.0.0.1 idp.feeds.fun.local

# Step 2 — clone the repository and start the services

git clone git@github.com:Tiendil/feeds.fun.git
cd ./feeds.fun/docs/examples/multi-user
docker compose up -d

# Go to https://feeds.fun.local/ to access the web interface.
```

The example uses:

- [Keycloak](https://www.keycloak.org/) as the Identity Provider.
- [OAuth2-Proxy](https://oauth2-proxy.github.io/oauth2-proxy/) as the authentication proxy that sits between Feeds Fun and Keycloak.
- [Caddy](https://caddyserver.com/) as the reverse proxy in front of everything.

However, any popular authentication solution should work fine, as long as it can pass the headers to the Feeds Fun backend and return HTTP 401 for unauthenticated requests to the frontend.

Please let us know if you try it out!

We also appreciate any feedback on the Feeds Fun configuration and pull requests with improvements to examples.

## Stay Connected

- Site: [feeds.fun](https://feeds.fun/)
- Reddit: [r/feedsfun](https://www.reddit.com/r/feedsfun/)
- Discord: [Feeds Fun](https://discord.com/invite/C5RVusHQXy)
- Repository: [github.com/Tiendil/feeds.fun](https://github.com/Tiendil/feeds.fun)
- Roadmap: [Roadmap](https://github.com/users/Tiendil/projects/1/views/1?pane=info)
- Full changelog: [CHANGELOG.md](https://github.com/Tiendil/feeds.fun/blob/main/CHANGELOG.md)
