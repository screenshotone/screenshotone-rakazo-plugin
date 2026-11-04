<img src="assets/logo.svg" alt="ScreenshotOne" width="64" height="64">

# ScreenshotOne for Rakazo

Capture clean website screenshots and PDFs, split long pages into readable slices, extract pages as Markdown, and check your ScreenshotOne usage from your Rakazo bots. This official plugin connects to the [ScreenshotOne hosted MCP server](https://screenshotone.com/mcp/) at `https://mcp.screenshotone.com` over Streamable HTTP, with browser-based OAuth sign-in.

You need a [ScreenshotOne account](https://dash.screenshotone.com) with available quota. Every render uses your organization's quota and plan limits; see [pricing](https://screenshotone.com/pricing/).

## What's included

- `plugin.json`: the [Agent Plugins](https://agent-plugins.org) manifest.
- `mcp.json`: the hosted ScreenshotOne MCP server.
- `skills/screenshotone/SKILL.md`: teaches bots which tool to use and how to handle results.

## Tools

- `render-website-screenshot`: capture a page as a temporary image link, optionally full page, split into vertical slices, and with the page's HTML or Markdown from the same render.
- `render-website-screenshot-as-file`: return the screenshot or a PDF as a file, in JPG, PNG, WebP, GIF, JP2, TIFF, AVIF, HEIF, or PDF (up to 5 MB).
- `extract-website-markdown`: return a page's cleaned Markdown as text.
- `get-usage`: report the connected account's quota and concurrency usage.

Ads and cookie banners are blocked by default. Result URLs are temporary; download anything you want to keep.

## Install and connect

1. In Rakazo, open **Integrations** → **+** → **From GitHub**.
2. Paste `https://github.com/screenshotone/screenshotone-rakazo-plugin` and choose **Preview**, then **Connect**.
3. Choose **Add skills** under Skills to add the ScreenshotOne skill.
4. Choose **Sign in** on the ScreenshotOne server, sign in to ScreenshotOne in the browser, and approve access. Rakazo discovers OAuth from the server and registers itself automatically; no API key is needed.
5. With a bot selected, choose **Use in this bot**.

## Try it

- "Capture a full-page screenshot of https://stripe.com with slices and describe its visual hierarchy."
- "Save https://example.com as a PDF."
- "Extract https://screenshotone.com/pricing as Markdown and compare the plans in a table."
- "How much ScreenshotOne quota do I have left?"

## Limits

ScreenshotOne reaches public HTTP and HTTPS pages only. It cannot reach `localhost` or private networks, and it cannot reuse your signed-in browser session. Use it only for pages you own or are authorized to process.

## Support

- MCP overview: https://screenshotone.com/mcp/
- Documentation: https://screenshotone.com/docs/
- Support: https://screenshotone.com/support/ or support@screenshotone.com
- Privacy policy: https://screenshotone.com/privacy-policy/
- Terms of service: https://screenshotone.com/terms-of-service/

## License

[MIT](LICENSE). Icon notices are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
