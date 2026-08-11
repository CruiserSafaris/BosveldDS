# Bosveld Draughting Service — Website Notes

The site is live at **https://www.bosvelddraughtingservice.co.za/** 🎉 — this file now covers what's already done, a quick post-launch checklist, and how to make future updates.

## Files in this folder

- `index.html` — the website itself (one page)
- `robots.txt` — tells search engines and AI crawlers (GPTBot, ClaudeBot, PerplexityBot, etc.) they're welcome to read the site
- `sitemap.xml` — tells search engines what pages exist
- `llms.txt` — a plain-language summary of the business for AI assistants to read directly
- `bd-logo.svg`, `bd-mark.svg`, `bd-badge.svg` — logo files (full lockup, small icon mark, circular badge) for reuse elsewhere (letterheads, social profile pictures, etc.)

All SEO-relevant addresses (canonical link, Open Graph tags, structured data, sitemap, robots.txt) now point to `https://www.bosvelddraughtingservice.co.za/`, and every email reference on the site uses `johan@bosvelddraughtingservice.co.za`.

## Post-launch checklist

A few things worth confirming now that it's live, roughly in order:

1. **Visit the live site on desktop and mobile** and click through every nav link, the "Request a Quote" / "Chat on WhatsApp" buttons, and the quote form's "Send via WhatsApp" and "Send via Email Instead" buttons — confirm the email one now opens a draft to `johan@bosvelddraughtingservice.co.za`.
2. **Check HTTPS is enforced** — the address bar should show a padlock with no "not secure" warning. If it doesn't yet, go to the GitHub repo → Settings → Pages and tick **Enforce HTTPS** (this only becomes available once DNS has fully propagated).
3. **Submit the sitemap to Google Search Console** (search console.google.com, add the property, verify via the HTML file or DNS method, then submit `https://www.bosvelddraughtingservice.co.za/sitemap.xml`) — this is what gets the site properly indexed rather than waiting for Google to stumble onto it.
4. **Set up Bing Webmaster Tools** the same way if you want Bing/Copilot coverage too — it's a five-minute add once Search Console is done since Bing can import verified Search Console sites directly.
5. **Test the email inbox** — send a test message to `johan@bosvelddraughtingservice.co.za` from another address to confirm it's actually receiving mail before relying on it for enquiries.

## Making future updates

The site is a single `index.html` file with everything inline (no build step). To change anything — text, prices, adding real portfolio photos — edit `index.html` directly and re-upload it to the GitHub repo (via **Add file → Upload files**, overwriting the existing one) or push via git if you're comfortable with that. Changes usually go live within a minute or two of committing.

If the business details ever change again (name, phone, email, town, services), the same handful of spots need updating together for the SEO markup to stay accurate: the `<title>` and meta tags near the top of `index.html`, the two `application/ld+json` structured data blocks (business info and FAQ), the header/footer logo text, the hero circular badge, the quote form's `EMAIL_ADDRESS` variable, `llms.txt`, and `robots.txt`'s sitemap line. I'm happy to make that pass whenever something changes — just let me know what's new.

## Notes on the AI/SEO setup already built in

- Structured data (JSON-LD) describing the business, services, and founder is embedded so Google and AI systems can extract facts directly rather than guessing from prose.
- An FAQ section with common questions and direct answers — this is the format AI answer engines tend to quote most reliably.
- `robots.txt` explicitly allows the major AI crawlers (GPTBot, ClaudeBot, PerplexityBot, and their "user" variants that fetch pages live when someone asks a chatbot a question) rather than leaving them to a default that might block them.
- The whole site is static HTML with real text in the initial page load — no JavaScript rendering required to see the content, which matters because most AI crawlers don't execute JavaScript.

Worth doing every few months: search your own business name plus "Lephalale" or "Thabazimbi" in ChatGPT, Claude, and Perplexity to see whether Bosveld Draughting Service gets cited, and check Google Search Console for real traffic and search-query data once it's set up.
