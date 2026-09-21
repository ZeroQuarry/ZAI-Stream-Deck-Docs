# Z.ai Usage Deck — Docs

The public documentation and support site for **Z.ai Usage Deck**, an Elgato Stream Deck plugin that keeps
your Z.ai / GLM Coding Plan quota in view. The plugin's source lives in a private repository; this repo
holds only the site.

**Live at: [zaideck.zeroquarry.com](https://zaideck.zeroquarry.com)** — deployed by Netlify from `main`.

## Editing the site

The whole site is one file, `index.html` — no build step, no dependencies. The screenshots it embeds live
in `shots/` and are rendered from the real face builders by the plugin's own tooling; to refresh them,
run this in the private source repository and copy the `docs/shots/*.png` files here:

```bash
npx rollup -c rollup.test.config.mjs --input test/shots.ts && node build/tests/shots.mjs
```

## Deployment

Netlify watches this repository: publish directory is the repo root, no build command. Point the
`zaideck.zeroquarry.com` DNS record (CNAME) at the Netlify site and enable HTTPS in the Netlify panel.

## Support

Questions, bugs and feature requests: [support@zeroquarry.com](mailto:support@zeroquarry.com).
