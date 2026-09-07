# ballsdeepinternational.com

Static mirror of the site, taken off Neocities on 2026-09-07 and served from GitHub Pages.

## Why it moved

The `.com` lapsed while the Namecheap account was locked and entered pendingDelete on
2026-09-03. Neocities only supports custom domains on its paid Supporter plan, so keeping
the site on Neocities meant paying $5 a month on top of the domain. GitHub Pages serves a
custom domain for free, which leaves the domain renewal as the only cost.

## Turning the custom domain on

Do this only once `ballsdeepinternational.com` is registered again:

1. Already done. `CNAME` holds `ballsdeepinternational.com` and Pages is configured for it.
   Until the name resolves here Pages simply serves nothing, which is deliberate: without
   the CNAME this project page would have been served under
   `www.betlegendpicks.com/ballsdeepinternational/`, because that is the custom domain on
   the `nimadamus.github.io` user site, and this content does not belong under the betting
   brand.
2. At the registrar, point the apex at GitHub Pages:
   `A 185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`,
   and `CNAME www -> nimadamus.github.io`.
3. Wait for the Pages settings page to report the certificate issued, then tick
   Enforce HTTPS.

## URL shape

Neocities served extensionless URLs and 301'd `/x.html` to `/x`. GitHub Pages serves
`/x` from `x.html` as well, verified before the move, so internal links, canonicals and
the sitemap all keep working unchanged. `.nojekyll` is present so nothing is rewritten
by Jekyll and filenames starting with digits or underscores are served as they are.

The Neocities copy at https://ballsdeepinternational.neocities.org stays live as a
fallback and is not being deleted.
