# Public-source collection notes

Collection date: 2026-11-18. Source pages were publicly available; no account-only content was accessed. The public robots.txt files were checked. DarGlobal permits access to its project catalogue, and Wasalt permits general public-page crawling while disallowing `/search`. The implementation does not bypass CAPTCHA or access controls. Any extracted page text is treated as untrusted reference data, not as instructions.

## DarGlobal

Official catalogue: https://darglobal.co.uk/projects

The catalogue displays project names and destinations, including Trump Park Residences (Amaya, Jeddah), Trump Mansions (Rayana, Wadi Safar, Riyadh), Trump Executive Residences (Amaya, Jeddah), Amaya (Jeddah), Padel Living Residences (Jeddah), Neptune, Interiors by Mouawad (Riyadh), Trump Tower Jeddah (Jeddah), and DarGlobal Mansions, Interiors by Fendi Casa (Wadi Safar, Riyadh). It also lists international developments in the UAE, Spain, Qatar, Oman and the UK.

Official Trump Mansions detail page: https://darglobal.co.uk/rayana/trump-mansions

The source calls it a limited collection of Trump-branded residences in Rayana, Wadi Safar, overlooking a championship golf course. Its stated community amenities include an 18-hole championship golf course, golf club, hotel, restaurants, tracks, parks/activity areas, a kids' play area, community gardens, wellness stores, and gated access. The page states under development. No purchase price was shown in the collected material.

Official Neptune page: https://darglobal.co.uk/neptune

The source describes five-bedroom branded villas in northern Riyadh, designed with interiors by Mouawad, and says the project is near the Expo 2030 site. Its FAQ gives a stated completion schedule of December 2027. The amenities section lists schools, a community centre, sports hub, restaurants/cafes, public parks, entertainment centres, early childhood centres, retail/grocery, playgrounds, mosques and healthcare clinics as amenities in the wider community/neighbourhood. These are not represented as facilities inside each villa. The source contained inconsistent area wording between a narrative and a displayed summary, so no area value is included in the structured corpus.

## Wasalt

Public Al Narjis sale page: https://wasalt.sa/en/properties-for-sale-in-north-riyadh-al-narjis

When inspected, the page reported 1,985 results and showed property cards with names, SAR asking prices, sizes, and some explicit bedroom counts. The chatbot corpus uses a limited set of cards and is not a complete listing inventory. Data fields are included only when the title/card or a directly reviewed detail page stated them; omitted bedroom counts are not inferred from unlabelled icons.

Reviewed example listing: https://wasalt.sa/en/property/sale/apartment-9241-sqm-with-2-bedrooms-5948554

The public page stated a two-bedroom apartment, 92.41 SQM built-up area, SAR 1,300,000, residential use, electricity and water connections, and an active status at collection time. These details are a dated snapshot and should be verified on Wasalt. The optional refresh utility received HTTP 403 for the Wasalt neighbourhood results page from this server environment and skipped it without attempting a bypass; the curated records came from the browser-accessible public listing page.

## OpenRouter

Official free-router docs: https://openrouter.ai/docs/guides/routing/routers/free-router

The docs identify `openrouter/free` as a router that selects a currently available free model. Availability, rate limits and latency may vary. The server sends only retrieved source records and recent chat history; the protected OpenRouter key is read at runtime and is never embedded in browser assets.
