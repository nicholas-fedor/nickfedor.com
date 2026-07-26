# nickfedor.com

This is the source repository for [nickfedor.com](https://nickfedor.com/), which is a static site built with [Hugo](https://gohugo.io/) and the [Hextra](https://github.com/imfing/hextra) theme.

## New Project Setup

Follow Hextra's [guide](https://imfing.github.io/hextra/docs/getting-started/) for creating a new project and setup Hextra as a Hugo module.

## Deployment

The site is built and deployed on [Cloudflare Pages](https://pages.cloudflare.com/).

### Initial Setup

1. Create the repository on GitHub.
2. Follow Cloudflare's [Hugo deployment tutorial](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/) to connect the repository.
3. The default build settings are sufficient—no configuration changes are required.

### DNS Configuration

After the first successful build:

- If your domain is managed by Cloudflare, configure a **CNAME record** to point to the Pages deployment.
- Adding a `www` CNAME record is recommended, but optional.
- If migrating from a previous host (e.g., GitHub Pages), remove stale DNS entries and purge Cloudflare's cache to expedite propagation.

## Adding Content

To add a new blog post:

```bash
hugo new content/blog/<post number-slug>/index.md
```

## License

This project is licensed under the AGPLv3 License. See `LICENSE.md` for details.
