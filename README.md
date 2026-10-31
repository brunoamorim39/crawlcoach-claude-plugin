# CrawlCoach for Claude

CrawlCoach finds the pages Google left out of its index and tells you what to change on each one. It reads Google's reason for each page from your Search Console data, checks up to 50,000 URLs per site, and sends a fix list. This plugin brings your fix list into Claude, so Claude Code can make the fixes in your site's code and ask CrawlCoach to recheck the pages it changed.

Account tools need a [CrawlCoach](https://crawlcoach.com) account. The robots.txt, sitemap, llms.txt, page count, and AI crawler checks work on any public site without one.

## What you can do

- Read your fix list: each fix with its page, why it matters, the exact change, and its status.
- List the pages Google left out, with Google's reason for each, and the pages it has.
- Recheck the pages you changed, so the fix status updates without waiting for the next scheduled check.
- Test pages against a live or draft robots.txt for Googlebot, Bingbot, and the AI crawlers.
- Check whether robots.txt or a firewall blocks ChatGPT, Claude, or Perplexity from a page, and whether its text is in the server HTML.
- Find sitemap problems, count a site's pages, and check or draft an llms.txt.

The first time you use an account tool, Claude asks you to sign in to CrawlCoach.

## What the plugin connects to

The plugin adds one remote MCP server, `https://crawlcoach.com/mcp`, run by CrawlCoach. It has no hooks, scripts, or local commands. Its skills only tell Claude how to use the tools, and send nothing on their own.

When Claude calls a tool, it sends that tool's inputs to the server: a site ID, page addresses, or the public site you asked to check. Sign-in uses OAuth with CrawlCoach's account system, so Claude never sees your password. Account tools return only your own sites. The free checks fetch the public site you name, the way a crawler does, and CrawlCoach stores nothing from it.

## Privacy and support

- Privacy policy: https://crawlcoach.com/privacy
- Terms: https://crawlcoach.com/terms
- Documentation: https://crawlcoach.com/docs/mcp-tools
- Support: support@crawlcoach.com

## License

MIT
