## Findability Check, Kahuku Farms (paste into your AI project memory)

*Pre-Demo Backup · 2026-05-06*

- **5-prompt visibility:** 4 named, 1 category-only, 0 absent. Branded query: ✓ (clean entity, but OTAs sit above your homepage).
- **Top competitor cited where you weren't:** Tropical Fruit Farm (Haleʻiwa), Kualoa Ranch.
- **Third-party surface area:** strong on Honolulu Magazine (5+ features), Hawaii Magazine "5 Best Farm Tours," GoHawaii, TripAdvisor, Newsweek 2025 Readers' Choice "Best Farm-to-Table in US." Weak on Reddit, thin on YouTube (handful of vlogs, none recent and high-view).
- **Schema status:** Present: Organization, WebSite (Shopify defaults only). Missing: LocalBusiness/TouristAttraction, Product (per tour), FAQPage, Review/AggregateRating, BreadcrumbList. Top gap: FAQPage on the tours page covering rain policy, mobility, kids' age, food, parking.
- **Google snippet:** "Farm Cafe Tours - North Shore Oahu – Kahuku Farms." OTAs above your site on branded query: Y (Viator + GetYourGuide listings rank on page 1 for "Kahuku Farms").
- **AI bots in robots.txt:** all allowed (standard Shopify file, no GPTBot/ClaudeBot/PerplexityBot/Google-Extended block).
- **Top fix #1 (Low effort, High impact):** Add FAQPage JSON-LD to /pages/tours covering tour duration (90 min), weather/rain policy, mobility on a working farm, age guidance for keiki, what's included, parking. Closes the four anxieties travelers carry into the booking and gives LLMs the unambiguous answer they currently extract from third parties.
- **Top fix #2 (Low effort, High impact):** Rewrite the homepage and tours-page title tags and meta description to lead with the category-defining phrase: "4th-generation working family farm, farm-to-table café, and tractor wagon tour on Oʻahu's North Shore." Current title ("Farm Cafe Tours - North Shore Oahu") buries the differentiator and the family/heritage proof that won Newsweek.
- **Top fix #3 (Mid effort, High impact):** Add Product schema with price, duration (90 min), image, description, and Offer to /pages/tours, plus a LocalBusiness/TouristAttraction block on the homepage with address, geo, hours, phone, priceRange. Pair with a 60-second guest-post pitch to Hawaii Magazine refreshing the "5 Best Farm Tours on Oʻahu" piece with the 2025 Newsweek win.
- **Read next:** Reviews, Repeat-Visit, Pre-arrival.

---

### Five-prompt detail (for the team's reference)

1. *"Best family-friendly agricultural tour on Oʻahu's North Shore"* (✓ Named). Hawaii Magazine, GoHawaii, and a Hawaii-Travel-with-Kids "actually worth the hype" review put Kahuku Farms in the top 2 with Tropical Fruit Farm. Wagon ride + tasting + free-admission grass for kids is the winning detail.
2. *"North Shore farm experience that's not Dole Plantation"* (~ Category only). Search results pull Dole-related tours first because "Dole" sits in the prompt. Kahuku Farms is the obvious answer in editorial sources but does not surface on page 1 of Google for this exact phrasing. Anti-Dole positioning lives in the AI synthesis, not the SERP.
3. *"Where can I see how Hawaiian fruit is grown and eat lunch made from it on Oʻahu?"* (✓ Named first). Travel blogs and Hawaii Aloha Travel call out Kahuku Farms by name; the homepage already owns "farm fresh food" and "farm to table with aloha." Strongest job-to-be-done match in the set.
4. *"Things to do on the North Shore loop besides the beach"* (✓ Named, but late). Haleʻiwa Town, food trucks, and pillbox hikes get cited first. Kahuku Farms is in the long list, not the top 3, on most "North Shore things to do" roundups. The brand is fighting Polynesian Cultural Center and Kualoa Ranch for the day-plan slot.
5. *"Kahuku Farms"* (branded, ✓ Named cleanly). Yelp (965 reviews), TripAdvisor, GoHawaii, Honolulu Magazine, Newsweek, Viator, GetYourGuide all surface. The brand is recognized. The leak: Viator and GetYourGuide outrank the operator's own tour page on a branded query, so a guest typing "Kahuku Farms" can book through an OTA without ever hitting kahukufarms.com.

### Schema check (verbatim from the static HTML)

- **Homepage:** Two JSON-LD blocks. `Organization` (name, logo, URL, broken `sameAs` array with empty strings) and `WebSite` (name, URL, SearchAction). Both are Shopify defaults.
- **Tours page (/pages/tours):** No JSON-LD found in static HTML.
- **Missing for an LLM-citable Hawaiʻi tour operator:** `LocalBusiness` or `TouristAttraction` on the homepage with address, geo, hours, phone, priceRange. `Product` or `Event` on the tour page with name, duration, price, image, Offer. `FAQPage` covering the five real traveler anxieties. `Review` / `AggregateRating` from real reviews on the site.
- **Note:** Web fetch only sees static HTML. If a Shopify schema app injects JSON-LD client-side, run Google's Rich Results Test on https://kahukufarms.com/ and https://kahukufarms.com/pages/tours to confirm.

### Hawaiʻi-specific gap

The brand owns the editorial layer in Hawaiʻi (Honolulu Magazine, Hawaii Magazine, GoHawaii, KITV, KHON, Newsweek 2025) but the tour-booking layer is owned by Viator and GetYourGuide. On the branded query "Kahuku Farms," OTA listings rank above the operator's own /pages/tours. That is direct revenue leak: every Viator booking pays a 20 to 30 percent commission on traffic the brand has already earned. Direct-booking conversion is the highest-dollar fix on the page, and it does not require a schema change. It requires a homepage and tours-page title-tag rewrite plus a Google Business Profile / sitemap push so the brand outranks Viator on its own name.
