# nickfedor.com

This is the source repository for [nickfedor.com](https://nickfedor.com/).

## Development

This website is a static site built with [Hugo](https://gohugo.io/).

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

## License

This project is licensed under the AGPLv3 License. See `LICENSE.md` for details.
