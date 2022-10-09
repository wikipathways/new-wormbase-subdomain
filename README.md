# new-community-subdomain

Template repository for WikiPathways subdomains

## Developers
Subdomain redirect strategy for communities (portals), etc.

1. Create new repo from the [new-community-subdomain](https://github.com/wikipathways/new-community-subdomain) template
3. Add `CNAME` file with desired subdomain name. Create [manually](./CNAME) or use Settings/Pages.
4. Turn on GitHub Pages, with the "Deploy from branch", the main branch, the `/` root.
2. Edit the [index.html](index.html) file with redirect details
5. In CloudFlare, add CNAME record to cloudflare with name = subdomain (e.g., `cptac`), target = `wikipathways.github.io` and proxy = `DNS only`

The DNS will direct sudomain traffic to the target GitHub org and then GitHub will manage the final direction to the repo containing the matching CNAME file. The repo can contain web content or a simple index.html file with redirect info (like this example).
