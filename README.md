# Cheaper Bright Data Alternative: What You Pay After the $4/GB Promo Ends, How ScraperAPI's Credits Really Work, and When You Should Not Switch (Plan Table and Trial Details)

Bright Data's residential proxies list at **$8/GB**; the **$4/GB** rate you see quoted everywhere is a 50% promo that runs for three months and then expires. Monthly plans start at **$499** (about 141 GB, roughly $3.54/GB), and the SERP and Web Scraper APIs each carry their own **$499/month** entry point. ScraperAPI starts at **$49/month** for 100,000 credits and 20 concurrent threads, and the trial gives you 7 days and 5,000 credits without a credit card.

Whether that's cheaper for your workload depends on which Bright Data product you're actually replacing. A team using the proxy network and a team using the Unlocker API are buying different things, and only one of them can move to a credit-based API without giving something up.

> **Short version:** if you use Bright Data's Unlocker, SERP, Scraper, Browser or Crawl APIs, ScraperAPI's Hobby plan at $49/month is the cheapest way to test a replacement, and the 5,000-credit trial costs nothing. If you only rent exit IPs by the gigabyte, ScraperAPI is the wrong product and per-GB vendors start at $0.49/GB.
>
> 👉 [See ScraperAPI's current plans and start the 7-day, 5,000-credit trial](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## Which Bright Data product are you replacing?

Bright Data sells at least four things that people lump together as "Bright Data": a residential/datacenter/ISP proxy network, Web Unlocker, a Scraper API with prebuilt scrapers, and a SERP API. Each has separate pricing and separate minimums, which is why two readers comparing "Bright Data vs. cheaper alternatives" often get different answers.

ScraperAPI replaces the API layer. You send a URL or a query and get HTML, markdown or structured JSON back, with proxy rotation, retries, CAPTCHA handling and browser rendering handled on their side. There is no standalone proxy product and no per-GB plan, so it cannot replace a raw proxy subscription.

That single distinction decides most of the cases below.

## ScraperAPI's plans and what each one buys

| Plan | Credits and concurrency | Price and billing | Purchase link |
| --- | --- | --- | --- |
| Free | 1,000 credits/month | $0 | [ Start on the free plan](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Hobby | 100,000 credits, 20 concurrent threads | $49/month | [ Open Hobby at $49/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Startup, Business, Scaling (intermediate tiers) | Credits and concurrency step up between Hobby and Advanced; geotargeting goes global from Business | Listed on the pricing page | [ Check the current intermediate tiers](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Advanced | 21,500,000 credits, 500 concurrent threads | $1,975/month | [ See the Advanced tier](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Enterprise | Custom volume | Quote through sales | [ Request enterprise pricing](https://www.scraperapi.com/pricing/?fp_ref=coupons) |

Self-serve checkout tops out at $1,975/month; anything above that goes through sales. The intermediate tiers exist and their names show up in ScraperAPI's own documentation (geotargeting is US and EU only on Hobby and Startup, global from Business, and pay-as-you-go starts at Scaling). Their exact credit counts and prices change, so check the page rather than a screenshot from someone's blog. I've left those numbers out on purpose instead of guessing at them.

Two things worth knowing before you pick a tier:

- **7 days, 5,000 credits, no card.** At 1 credit per standard page that's 5,000 pages. At 25 credits per Google query it's 200 queries. Run your real target list through the trial before you choose a plan.
- **Pay-as-you-go starts at Scaling.** On Hobby and Startup, running out of credits means the pipeline stops until the next cycle.

## Where Bright Data's bill actually comes from

The $4/GB headline is a promotional rate, not the price. Bright Data's list price for pay-as-you-go residential traffic is $8/GB, and the 50% discount lasts three months before reverting to $8. Budget the renewal at $8 or you'll be back to searching for alternatives in month four.

The $499 floor is the bigger constraint for small teams. One r/proxies user described the shape of it: there's "no real middle ground between pay-as-you-go ($1.50/1K, prohibitive for volume) and the $499 monthly commitment." If your monthly usage is 20 GB, you either pay the higher pay-as-you-go rate or commit to a plan sized for someone else.

API products carry separate minimums. The SERP API starts at $499/month for 380,000 results. The Web Scraper API starts at $499/month for 384,000 records. Buying both means two $499 entry points, not one.

Bright Data also bills in four different units across its catalogue: per GB for proxies, per IP for datacenter plans, per 1,000 requests, and per 1,000 records. Comparing a $499 Web Scraper plan against a $49 credit plan requires converting between units, and the conversion depends entirely on your target mix.

Two more details that affect the first week:

- **The trial requires KYC.** ID upload, sometimes a video call, and a use-case review before residential access opens. Trial credits of $25 to $50 are typically gone in under 1 GB of residential traffic.
- **Mobile proxies are no longer orderable on new accounts.** As of September 2026 they've disappeared from Bright Data's proxy pricing page and product navigation, and the old mobile pricing page redirects. There was no announcement. Treat it as "you can't sign up for this" rather than "the product is discontinued."

If your workflow is API calls against retail or search targets, none of that overhead buys you anything you'll use.

👉 [Check what $49 buys on the Hobby plan](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## Your bill is measured in credits, and credits are not 1:1

One credit per standard page is the best case. The multiplier depends on where you're scraping.

| Target | Credits per request | 1,000 requests cost at Hobby ($49/100K credits) |
| --- | --- | --- |
| Standard HTML page | 1 | $0.49 |
| Amazon | 5 | $2.45 |
| Google or Bing | 25 | $12.25 |
| Ultra-premium targets | 30 | $14.70 |
| JavaScript rendering | +10 on top of the above | adds $4.90 per 1,000 |

That table is the whole reason to trial first. A plan sized on "pages per month" can be off by a factor of 25 if most of your traffic is search results.

The tier you pick changes the unit economics too. At Advanced ($1,975 for 21.5M credits), 1,000 standard pages cost about **$0.09** and 1,000 Google queries about **$2.30**, against $0.49 and $12.25 on Hobby.

For context on Bright Data's side of that math: SERP at $499 for 380,000 results works out to about **$1.31 per 1,000 results**, and Web Scraper at $499 for 384,000 records is about **$1.30 per 1,000 records**. If your entire workload is high-volume Google SERP, Bright Data's per-unit rate at the $499 tier is lower than ScraperAPI's Advanced rate, and moving won't save money. If your workload is mostly standard pages and product data at 1 to 5 credits, the gap runs the other way by more than an order of magnitude. These aren't identical units (a Bright Data "record" can carry more fields than a ScraperAPI page), so treat it as a sizing exercise, not a benchmark.

One billing rule is genuinely different from proxy pricing. ScraperAPI charges only for **successful 200 and 404 responses**; failed 500 requests are free. On a per-GB proxy plan, a request that gets blocked still burns bandwidth. If your success rate on a hard target sits at 70%, that difference shows up in the invoice every month and never appears in a per-GB comparison.

Volume limits on the non-API tooling: DataPipeline runs scheduled projects of up to 100,000 URLs, and Async batch jobs accept up to 50,000 URLs with automatic retries for up to 24 hours.

👉 [Compare the credit tiers before you commit to one](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## What ScraperAPI cannot replace

Three limits are worth stating plainly, because discovering them after you've migrated is expensive.

**No standalone proxy product.** There's no host, port and login to drop into your own scraper. If your existing code already handles requests and you just need cheaper exit IPs, ScraperAPI doesn't sell that.

**No per-GB billing and no mobile proxies.** Neither gap can be worked around with configuration.

**Geotargeting is US and EU only on Hobby and Startup.** City-level or country-level targeting outside those regions requires Business or above, which moves you off the $49 entry point.

If any of those three is a hard requirement, the honest answer is that this isn't the cheaper Bright Data alternative for you. Per-GB vendors solve the first two; Decodo sells mobile proxies at $3.75/GB on self-serve plans, which is the direct replacement for the Bright Data mobile product new accounts can no longer order.

For everyone else, the trial settles it in an afternoon: point 5,000 credits at your actual targets, count what a typical 1,000-URL job consumes, and multiply.

👉 [Price your own target list with the free 5,000-credit trial](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## Other cheaper options, and the volume where each one wins

| Provider | Entry price | Billing unit | Where it actually beats Bright Data |
| --- | --- | --- | --- |
| Evomi | $0.49/GB on a $49/month, 100 GB plan | Per GB | Lowest listed residential rate, 54M+ IPs claimed; no published success rate or latency |
| DataImpulse | $1/GB, no subscription, traffic never expires | Per GB | Any volume, including small ones; extra charge below country-level targeting |
| Decodo | 3 GB for $11.25 ($3.75/GB) or $4/GB pay-as-you-go | Per GB | Mobile proxies at $3.75/GB and a 3-day, 100 MB residential trial; real savings appear after Bright Data's promo ends or above roughly 100 GB |
| Oxylabs | $6/GB on small buys, falling to $5 up to 20 GB, $4 up to 125 GB, $2.50 from 1,000 GB; plans from $30/month | Per GB or subscription | Small buyers pay more than Bright Data's $4 promo; it only wins clearly above 1,000 GB |
| IPRoyal | $7/GB | Per GB | Sticky sessions up to 7 days and traffic that never expires, which suits account-based work |
| Apify | $29/month Starter including $29 of platform usage; residential proxies $7–8/GB | Compute units plus proxy bandwidth | Prebuilt Actors for common targets; cost estimation before a run is the recurring complaint, including in a Capterra review from April 2026 |
| Firecrawl | Free 1,000 credits/month; Hobby $16/month annual ($19 monthly) for 5,000 credits | Per page credit | LLM-ready markdown output and an AGPL-3.0 self-hostable option; no proxy product |

The pattern in that table: Decodo and Oxylabs look cheaper on a pricing page and aren't, at least while the Bright Data promo is running. At $4/GB promotional, Decodo's $4 pay-as-you-go rate ties it and Oxylabs' $6 small-buy rate loses. The genuinely cheaper per-GB options sit at the low end (Evomi, DataImpulse), and they trade IP pool size and targeting granularity for the price.

## Which one to buy

Match your situation to a line:

- **You already have a working scraper and only pay for proxies.** Buy per-GB. DataImpulse at $1/GB or Evomi at $0.49/GB on the 100 GB plan. ScraperAPI is the wrong purchase here, and buying it will end in a refund.
- **You're replacing Bright Data's Unlocker, SERP, Scraper, Browser or Crawl API and mostly hit standard pages.** Start on Hobby at $49, confirm the credit burn on real targets, then step up.
- **Your traffic is mostly Google or Bing.** Credits disappear 25 times faster. Run the trial before choosing a tier, and expect roughly $2.30 per 1,000 queries at Advanced.
- **You need targeting outside the US and EU.** Business or above.
- **You need mobile proxies.** Neither Bright Data (new accounts since September 2026) nor ScraperAPI. Decodo at $3.75/GB is the closest self-serve replacement.
- **You need hundreds of thousands of Google results monthly and nothing else.** Bright Data's $499 SERP plan prices at about $1.31 per 1,000 results, which is hard to beat on unit cost. The trade is the $499 commitment and the KYC process.

Before you pay, two things to confirm on the page itself: the credit counts and prices of the intermediate tiers, since those are where most readers land once the trial numbers come in, and whether pay-as-you-go overage applies to your tier (it starts at Scaling, not Hobby). The 7-day trial with 5,000 credits and no card requirement is the cheapest way to answer both.

👉 [Open ScraperAPI's pricing page and pick the tier your trial numbers point to](https://www.scraperapi.com/pricing/?fp_ref=coupons)
