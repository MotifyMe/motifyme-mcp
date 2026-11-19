# MotifyMe MCP server

UK car checks, running costs, fuel prices and used car listings for AI assistants.

MotifyMe is a UK automotive platform. This is its public, read-only Model Context Protocol (MCP) server. It lets an AI assistant answer questions about UK vehicles using the same public data shown on [motifyme.co](https://motifyme.co).

- **Endpoint:** `https://motifyme.co/mcp` (streamable HTTP)
- **Authentication:** none. No account or API key is needed.
- **Official MCP Registry name:** `co.motifyme/motifyme`
- **Explorer and setup guide:** https://motifyme.co/mcp-explorer

This repository holds documentation only. The server is hosted by MotifyMe; there is nothing to install or run.

## What you can ask

- "What car is AB12 CDE, and is its MOT and tax valid?"
- "Is this car ULEZ compliant?"
- "What is the price of diesel in the UK today?"
- "Find used automatic hatchbacks under £8,000 near Reading."
- "What does a Ford Fiesta cost to run each year?"
- "Which cars have the best MOT pass rates?"

## Tools

### Vehicle checks
| Tool | What it does |
| --- | --- |
| `free_vehicle_check` | Free check by registration: make, model, colour, fuel, year, MOT status and expiry, tax status and due date, safety recall status. |
| `vehicle_history_check` | Explains the separate paid vehicle history check and links to it for the registration given. |
| `ulez_check` | Whether a vehicle meets the ULEZ and Clean Air Zone emissions standard. |
| `vehicle_tax_estimate` | Estimated vehicle tax for a vehicle. |
| `mot_statistics` | MOT pass rates and common failure reasons by make and model. |
| `mot_pass_rate_rankings` | Rankings of makes and models by MOT pass rate. |

### Used cars and dealers
| Tool | What it does |
| --- | --- |
| `search_marketplace` | Search used car listings from UK dealers. |
| `ai_car_search` | Plain-English used car search. |
| `get_listing` | Details of one listing. |
| `search_dealers` | Find dealers by name or area. |
| `get_dealer` | A dealer's public storefront details. |
| `list_makes_and_models` | Makes and models currently listed. |

### Running costs and calculators
| Tool | What it does |
| --- | --- |
| `car_running_costs` | Running cost estimate for a make and model. |
| `fuel_cost_calculator` | Fuel cost for a journey or mileage. |
| `ev_charging_cost_calculator` | Cost to charge an electric vehicle. |
| `company_car_tax_calculator` | Company car (benefit in kind) tax estimate. |
| `uk_fuel_prices` | Latest UK average petrol and diesel prices. |

### Local information
| Tool | What it does |
| --- | --- |
| `ev_chargers_near` | Public EV chargers near a location. |
| `clean_air_zones` | UK Clean Air Zones and their charges. |
| `road_closures` | Current road closures near a location. |
| `vehicle_crime_near` | Recorded vehicle crime near a location. |

### Guides and news
| Tool | What it does |
| --- | --- |
| `search_blog` / `get_blog_post` | MotifyMe guides and articles. |
| `list_site_pages` / `get_site_page` | Public pages on motifyme.co. |
| `uk_car_news` | UK motoring news headlines. |
| `about_motifyme` | What MotifyMe is and what it offers. |

<!-- tools:start -->
## Full tool list

This list is rebuilt automatically from the live server, so it always matches what is available. 27 tools.

| Tool | What it does |
| --- | --- |
| `about_motifyme` | Who MotifyMe is, what it offers and the main public urls. |
| `ai_car_search` | Describe the used car you want in plain English, for example "diesel estate under 8000 no older than 8 years" or "2.0L Audi Q3 automatic", and get matching live MotifyMe marketplace listings. |
| `car_running_costs` | Vehicle tax, MOT and other running-cost facts for a UK-registered vehicle. |
| `clean_air_zones` | List of UK clean air and low emission zones with daily charges and the official page for each. |
| `company_car_tax_calculator` | Benefit-in-kind tax on a company car using the same bands as the MotifyMe calculator. |
| `ev_chargers_near` | Nearest public EV charging locations within 10 miles of a UK postcode. |
| `ev_charging_cost_calculator` | Cost to drive an electric car a given distance. |
| `free_vehicle_check` | Free check of a UK vehicle by registration plate. |
| `fuel_cost_calculator` | Cost of a journey or a year of driving for a petrol or diesel car. |
| `get_blog_post` | Full text of one published blog post by slug or url. |
| `get_dealer` | Public storefront summary for one dealer slug including a sample of their current stock. |
| `get_listing` | Full public details of one listing (spec, description, features, dealer, photos). |
| `get_site_page` | Readable text of a public motifyme.co page listed by list_site_pages (guides, fuel price city pages, tool pages). |
| `list_makes_and_models` | Makes (and optionally models of one make) currently in stock with counts and the matching motifyme.co hub page url. |
| `list_site_pages` | List public motifyme.co pages (guides, tools, finance pages, fuel price pages) from the sitemap, optionally filtered by keyword. |
| `mot_pass_rate_rankings` | Ranks UK car models by first-time MOT pass rate with tests counted and average mileage at test, from DVSA anonymised MOT data under the Open Government Licence v3.0. |
| `mot_statistics` | First-time MOT pass rate, most common failure areas and specific failures, average mileage at test and results by year of registration for a UK car model (for example make "Ford", model "Fiesta"), calculated from DVSA an |
| `road_closures` | Current National Highways road closures (public data), optionally filtered by road such as M6. |
| `search_blog` | Search published MotifyMe blog posts (UK car buying, selling, finance introductions, running costs, fuel, tax, MOT). |
| `search_dealers` | Find dealers on the marketplace by name or town. |
| `search_marketplace` | Search live used vehicle listings on the MotifyMe marketplace (UK dealers). |
| `uk_car_news` | Latest UK motoring and automotive news headlines with short summaries and links to the full stories, supplied by Autosnip (FullyAuto). |
| `uk_fuel_prices` | Latest UK average petrol and diesel pump prices (pence per litre) from the weekly DESNZ road fuel prices, with weekly change. |
| `ulez_check` | Whether a UK-registered vehicle is compliant with the London ULEZ and other clean air zones. |
| `vehicle_crime_near` | Latest month of police-reported vehicle crime near a UK postcode, with the most affected streets. |
| `vehicle_history_check` | What the paid MotifyMe vehicle history check covers and the link to run it: stolen markers, insurance write-offs (Cat S, Cat N and older categories), outstanding finance, scrapped or salvaged, imported or exported, plate |
| `vehicle_tax_estimate` | Estimated annual vehicle excise duty from CO2, engine size and first registration month, using the MotifyMe car tax logic. |
<!-- tools:end -->

## Add it to your assistant

Most MCP clients accept a remote server URL. Add a custom connector with:

```
https://motifyme.co/mcp
```

Step-by-step instructions for each assistant are at https://motifyme.co/mcp-explorer.

## Data, privacy and limits

- Everything is read-only and public. The server exposes nothing private or account-specific, and it cannot change anything.
- No personal data is requested. A registration number is only used to look up that vehicle.
- Requests are rate limited to keep the service fair.
- The free check covers MOT, tax and safety recalls. It does not cover outstanding finance, insurance write-offs or stolen records. Those are in the separate paid vehicle history check, with data provided by Experian.
- Cars are sold by the dealer or seller shown on each listing, not by MotifyMe.
- MotifyMe is an Introducer Appointed Representative of Presto Finance Ltd and can introduce customers to Presto Finance for car finance on dealer vehicles. MotifyMe does not lend and does not give advice. Finance is subject to status and is not guaranteed.

## Links

- Website: https://motifyme.co
- Terms and conditions: https://motifyme.co/terms-and-conditions
- Privacy policy: https://motifyme.co/privacy-policy
- Support: hello@motifyme.co

MotifyMe is a registered trade mark of MotifyMe Ltd.
