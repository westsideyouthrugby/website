# Future: CMS Setup

**Date:** 2026-02-10
**Status:** deferred

## Recommendation

Sveltia CMS over Decap CMS — lighter, more modern, actively maintained.

## Setup Steps

1. Create `static/admin/index.html` pointing to Sveltia CMS CDN
2. Create `static/admin/config.yml` defining content collections
3. Register a GitHub OAuth app (Settings → Developer settings → OAuth Apps)
4. Deploy a Cloudflare Worker as the OAuth proxy (free tier sufficient)
5. Configure the OAuth callback URL in the GitHub OAuth app

## References

- https://github.com/sveltia/sveltia-cms
- https://decapcms.org/docs/
