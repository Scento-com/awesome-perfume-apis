# Awesome Perfume APIs [![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

> A curated list of perfume and fragrance APIs, MCP servers, datasets and tools for developers.

If you are building something that needs perfume data (a note pyramid for an app, a fragrance tool for an AI assistant, a dataset for a model), this list helps you compare the options in one place. Entries are factual one-liners: type, access, and what the provider says it covers. Figures marked "claimed" come from the provider's own pages and were not independently counted. Information was read from public pages and docs on 21 Oct 2026; please open an issue or pull request if something has changed.

Sections and the entries inside them are sorted alphabetically. A product that offers both a REST API and an MCP server appears in both sections. Scento maintains this list and its own entries are in the same alphabetical order as everyone else's.

## Contents

- [APIs (REST)](#apis-rest)
- [Datasets](#datasets)
- [MCP servers](#mcp-servers)
- [Tools and wrappers](#tools-and-wrappers)
- [Contributing](CONTRIBUTING.md)

## APIs (REST)

- [Fraganty](https://fraganty.ai/api-docs) - REST API with JSON responses and open CORS covering perfumes, accords, notes, dupes and bottle images; free API key on request by email.
- [FragDB](https://fragdb.net/api) - Metered REST API plus downloadable CSV/Parquet files built on Fragrantica-derived data; Bearer key, free test key, $100 minimum spend per 180 days; 140,000+ fragrances claimed, 23 languages.
- [Fragella](https://api.fragella.com) - REST API with note pyramid, accord percentages, longevity, sillage, season, perfumers and purchase links; API key, free tier of 20 requests a month, paid from $12 a month; 100,000+ fragrances claimed.
- [Fragrance API by Fragplace](https://rapidapi.com/freeyourmusic-fragplace/api/fragrance-api) - Search API on RapidAPI over the Fragplace catalogue (fragrances, brands, perfumers, notes, accords); RapidAPI key, free plan of 1,000 requests a month, paid from $19 a month; 12 languages, 100,000+ perfumes claimed.
- [FragranceFinder API](https://rapidapi.com/remote-skills-remote-skills-default/api/fragrancefinder-api) - Search and similar-perfume endpoints on RapidAPI; RapidAPI key, free plan of 20 requests a month, paid from $30 a month.
- [Noteboxd](https://developers.noteboxd.com) - REST API (OpenAPI 3.2) with pyramids, accords, perfumers, reviews and wearing stats; account and Bearer key, free tier of 50 calls a day, pay-as-you-go above.
- [Parfum Bible](https://parfumbible.com/developers/) - Read-only REST API (OpenAPI 3.1) for catalogue search, details, comparison and verified retailer offers; no key, no account; offers default to the US.
- [ParfumDB](https://parfumdb.net) - Metered API and downloadable files derived from Parfumo, with GTIN-13 and review data; free sample, purchase required for full data; 236,000+ perfumes claimed.
- [Scento Perfume API](https://www.scento.com/developers) - REST API described in OpenAPI 3.1 (12 read-only answers); no key, no account, open CORS; 1,400+ perfumes, 400+ raw materials, 140+ houses; code samples in [Scento-com/perfume-api](https://github.com/Scento-com/perfume-api).
- [ScentRev](https://mcp.scentrev.com) - REST access alongside its MCP server; key required, free during the current period at 300 calls a day; 126,000+ scents claimed.

## Datasets

Static files, not live APIs. Check each licence before use.

- [FragDB fragrance-database](https://github.com/FragDB/fragrance-database) - Open sample and specification of the FragDB files on GitHub; licence listed as NOASSERTION / CC BY-NC.
- [Fragrantica Perfumes (Kaggle)](https://www.kaggle.com/datasets/ledecanteur/fragrantica-perfumes) - Community-published CSV and JSONL of Fragrantica data with ratings, notes, accords and perfumers; 140,228 perfumes stated; CC BY-NC-SA 4.0; scraped, unofficial.
- [TidyTuesday Parfumo dataset](https://github.com/rfordatascience/tidytuesday/tree/main/data/2024/2024-12-10) - Parfumo ratings, notes, perfumers and release years as a CSV for data-analysis practice (week of 10 Dec 2024).

## MCP servers

- [Blue Perfumery MCP](https://github.com/recepgocmen/blue-perfumery-mcp-server) - Self-hosted MCP server (5 tools) over one shop's catalogue with Shopier purchase links; needs your own MongoDB; MIT.
- [Fragplace MCP](https://fragplace.com/en/connect) - Hosted MCP with Fragplace sign-in (OAuth), read-only beta; catalogue search, details, similar fragrances and prices, plus your own diary and lists; 96,000 fragrances claimed.
- [Noteboxd MCP](https://github.com/Noteboxd/mcp) - Hosted MCP (OAuth) and local npm stdio server, MIT; account needed, shares the REST API's free tier; in the official MCP Registry.
- [Parfica](https://github.com/parfica/mcp-server-parfica) - Free keyless MCP with 3 tools (search, fragrance info with pyramid and accords, dupes), Ukrainian-first, MIT; in the official MCP Registry.
- [Parfum Bible](https://parfumbible.com/developers/) - Free keyless MCP with 4 tools (search, details, compare, verified retailer offers), alongside its REST API; English.
- [Perfume Picks](https://perfumepicks.app/mcp) - Free keyless MCP, 8 tools (pyramid, accords, community wear, curated dupes with match percentages, trending); remote or npm; 13,000+ perfumes claimed; in the official MCP Registry.
- [Scento Perfume API (MCP server)](https://www.scento.com/developers) - Remote MCP with 12 read-only tools over Scento's verified perfume database, no key and no account, ten languages for links; 1,400+ perfumes, 400+ raw materials, 140+ houses; registry name `com.scento/perfume-api`; npm and PyPI bridges as `scento-perfume-api` (also `perfume-mcp-server`, `perfume-database`); source [Scento-com/perfume-mcp-server](https://github.com/Scento-com/perfume-mcp-server).
- [ScentRev](https://mcp.scentrev.com) - MCP with 22 tools (longevity, sillage, season, accords, similar, wardrobe); OAuth or Bearer key, free at 300 calls a day; 126,000+ scents claimed.
- [ScentVerdict](https://scentverdict.com/connect) - Free keyless MCP with 6 tools (verdict, notes, similarity, live bottle prices from retailers); English; 31,000+ to 47,000+ perfumes claimed (its pages differ); in the official MCP Registry.

## Tools and wrappers

Unofficial scrapers and wrappers around community sites (Fragrantica publishes no official API). Mind the source site's terms.

- [Decodo Fragrantica Scraper API](https://decodo.com/scraping/web/fragrantica-scraper-api) - Hosted scraping API template for Fragrantica pages, part of Decodo's Web Scraping API; key, free starter plan, then paid.
- [Fragrantica Scraper (Apify)](https://apify.com/solidcode/fragrantica-scraper) - Community actor on Apify returning notes, accords, perfumers, ratings and optional reviews; pay per result, from $2 per 1,000 results.
- [fragscrape](https://github.com/HurleySk/fragscrape) - Open-source TypeScript scraping API for Parfumo (and Fragrantica, per its description), self-hosted, also on npm; MIT.

## Contributing

Additions are welcome; read [CONTRIBUTING.md](CONTRIBUTING.md) first. Short version: one factual line per entry, alphabetical, no superlatives, and say how it is accessed and what it costs.

## Licence

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.
