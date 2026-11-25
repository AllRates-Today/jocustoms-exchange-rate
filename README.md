# Jordan Customs Department Exchange Rates API — jocustoms-exchange-rate

[![npm version](https://img.shields.io/npm/v/jocustoms-exchange-rate.svg)](https://www.npmjs.com/package/jocustoms-exchange-rate)
[![license](https://img.shields.io/npm/l/jocustoms-exchange-rate.svg)](https://github.com/AllRates-Today/jocustoms-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/jocustoms-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/JOD today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fjocustoms%3Fsource%3DUSD%26target%3DJOD&query=%24.rate&label=USD%2FJOD%20official%2C%20Jordan%20Customs%20Department&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/tax-authority-rates-api/jocustoms/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fjocustoms%3Fsource%3DUSD%26target%3DJOD&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/tax-authority-rates-api/jocustoms/)

**Official Jordan Customs Department (Jordan) monthly exchange rates for Node.js and TypeScript. The published tax authority rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Jordan Customs Department itself prints, every month.**

## 🚀 Why this client?

- 🏛️ **Official rates** — Jordan Customs Department's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2014** — point-in-time tables and daily series for any past date
- 🔀 **Official vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Jordan Customs Department itself published, fixed once printed and carrying the tax authority's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📈 Latest official table

[![Latest Jordan Customs Department table](https://allratestoday.com/api/open/central-bank/jocustoms/table.svg)](https://allratestoday.com/tax-authority-rates-api/jocustoms/)

The image is rendered live from the keyless endpoint, so it follows the tax authority's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the tax authority publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-11-02 by Jordan Customs Department — 43 rates. Updated 2026-11-25.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | JOD | reference | 0.193 |
| AUD | JOD | reference | 0.498 |
| AZN | JOD | reference | 0.417 |
| BDT | JOD | reference | 0.0057 |
| BHD | JOD | reference | 1.88 |
| CAD | JOD | reference | 0.506 |
| CHF | JOD | reference | 0.86 |
| CNY | JOD | reference | 0.1063 |
| DKK | JOD | reference | 0.106 |
| DZD | JOD | reference | 0.0053 |
| EGP | JOD | reference | 0.013 |
| EUR | JOD | reference | 0.795 |
| GBP | JOD | reference | 0.948 |
| HKD | JOD | reference | 0.0904 |
| HUF | JOD | reference | 0.00217 |
| IDR | JOD | reference | 0.000039 |
| ILS | JOD | reference | 0.228 |
| INR | JOD | reference | 0.0075 |
| JPY | JOD | reference | 0.00452 |
| KRW | JOD | reference | 0.000536 |
| KWD | JOD | reference | 2.281 |
| LYD | JOD | reference | 0.111 |
| MAD | JOD | reference | 0.0723 |
| MYR | JOD | reference | 0.174 |
| NOK | JOD | reference | 0.076 |
| NZD | JOD | reference | 0.404 |
| OMR | JOD | reference | 1.841 |
| PHP | JOD | reference | 0.0111 |
| PKR | JOD | reference | 0.0026 |
| PLN | JOD | reference | 0.181 |
| QAR | JOD | reference | 0.195 |
| RON | JOD | reference | 0.149 |
| SAR | JOD | reference | 0.189 |
| SEK | JOD | reference | 0.071 |
| SGD | JOD | reference | 0.554 |
| SYP | JOD | reference | 0.0058 |
| THB | JOD | reference | 0.021 |
| TND | JOD | reference | 0.237 |
| TRY | JOD | reference | 0.014 |
| TWD | JOD | reference | 0.0218 |
| USD | JOD | reference | 0.709 |
| YER | JOD | reference | 0.003 |
| ZAR | JOD | reference | 0.043 |

</details>

Source: [Official rates published by JOCUSTOMS, served by AllRatesToday](https://allratestoday.com/tax-authority-rates-api/jocustoms/). Rates are as printed by the tax authority; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install jocustoms-exchange-rate
```

```bash
yarn add jocustoms-exchange-rate
```

```bash
pnpm add jocustoms-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/jocustoms-exchange-rate`](https://www.npmjs.com/package/@allratestoday/jocustoms-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'jocustoms-exchange-rate';

const pair = await getRate('USD', 'JOD', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Jordan Customs Department rate, on the tax authority's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest official table
- [Full official table](#full-official-table) — everything the tax authority printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the tax authority does not print directly are resolved from its table and flagged (see *Official vs derived rates* below).

```js
const pair = await getRate('USD', 'JOD', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'jocustoms',
  name: 'Jordan Customs Department',
  rate_date: '2026-11-02',   // Jordan Customs Department's own publication date
  source: 'USD',
  target: 'JOD',
  rate: 0.709,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full official table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'jocustoms-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'jocustoms',
  name: 'Jordan Customs Department',
  rate_date: '2026-11-02',
  rates: [
    { "base": "USD", "quote": "JOD", "type": "reference", "value": 0.709 },
    // … the rest of the official table (46 currencies vs JOD)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2014 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'jocustoms-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'JOD' });
```

**Response:**

```javascript
{
  bank: 'jocustoms',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'jocustoms-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'JOD', from: '2026-01-01', to: '2026-11-02' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'jocustoms',
  source: 'USD',
  target: 'JOD',
  from: '2026-01-01',
  to: '2026-11-02',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-11-02', rate: 0.709, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Jordan Customs Department currently publishes rates covering **46 currencies** against the JOD (as of the latest table):

🇦🇪 `AED` · 🇦🇺 `AUD` · 🇦🇿 `AZN` · 🇧🇩 `BDT` · 🇧🇭 `BHD` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇳 `CNY` · 🇩🇰 `DKK` · 🇩🇿 `DZD` · 🇪🇬 `EGP` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇭🇰 `HKD` · 🇭🇺 `HUF` · 🇮🇩 `IDR` · 🇮🇱 `ILS` · 🇮🇳 `INR` · 🇮🇶 `IQD` · 🇮🇷 `IRR` · 🇯🇵 `JPY` · 🇰🇷 `KRW` · 🇰🇼 `KWD` · 🇱🇾 `LYD` · 🇲🇦 `MAD` · 🇲🇾 `MYR` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇴🇲 `OMR` · 🇵🇭 `PHP` · 🇵🇰 `PKR` · 🇵🇱 `PLN` · 🇶🇦 `QAR` · 🇷🇴 `RON` · 🇷🇺 `RUB` · 🇸🇦 `SAR` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇸🇾 `SYP` · 🇹🇭 `THB` · 🇹🇳 `TND` · 🇹🇷 `TRY` · 🇹🇼 `TWD` · 🇺🇸 `USD` · 🇾🇪 `YER` · 🇿🇦 `ZAR`

## 🏛️ Source

The exchange rates Jordan Customs applies to convert foreign-currency invoice values into dinars for customs duty and sales tax on imports. The table is set administratively and changes at irregular steps, roughly monthly, for about 60 currencies.

- Publisher's own page: [Customs exchange rates (administrative tables)](https://asytrade.customs.gov.jo/customs/rates/search?lang=en) · [asytrade.customs.gov.jo](https://asytrade.customs.gov.jo/)
- Publication: every month; the exact schedule, freshness status and any current delay are on the [Jordan Customs Department rates page](https://allratestoday.com/tax-authority-rates-api/jocustoms/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Jordan Customs Department quotes **JOD per 1 unit of foreign currency** (e.g. `base: "USD", quote: "JOD"` means JOD per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the tax authority's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Jordan Customs Department rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/jocustoms/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('jocustoms')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate jocustoms ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Official vs derived rates

If Jordan Customs Department does not print a pair directly, the API resolves it from the tax authority's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The tax authority printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via JOD from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Jordan Customs Department |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'jocustoms-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('jocustoms-exchange-rate');

getRate('USD', 'JOD', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once a month — cache the official table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the official table |
| `getLatestRates({ apiKey })` | Free | The tax authority's full latest official table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2014 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same official tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/jocustoms.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/jocustoms/latest.json`

## 🔗 Links

- **Website:** [allratestoday.com](https://allratestoday.com)
- [Jordan Customs Department rates page](https://allratestoday.com/tax-authority-rates-api/jocustoms/) — live table, publication cadence, FAQ
- [All tax authority sources](https://allratestoday.com/tax-authority-rates-api/) · [Full list of 120+ central banks and 50+ tax authorities](https://allratestoday.com/central-bank-rates-api/institutions/) — one API, the same response shape for every source
- [Download central bank rates](https://allratestoday.com/download-central-bank-rates/) — every bank's latest table and history as Excel, CSV or JSON
- [Bank Exchange Rate API](https://allratestoday.com/bank-exchange-rate-api/) — live buy and sell rates from 1,200+ commercial banks in 120+ countries · [npm](https://www.npmjs.com/package/bank-exchange-rates) · [GitHub](https://github.com/AllRates-Today/bank-exchange-rates)
- [Package docs on the site](https://allratestoday.com/docs/sdk/jocustoms-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [ChatGPT app](https://chatgpt.com/plugins/plugin_asdk_app_6ae1e76098f48191a285ac3f5ab7a83b) — ask ChatGPT for live and official central bank rates
- [OpenAPI reference on Bump.sh](https://bump.sh/allratestoday/doc/allratestoday-api) — also on [SwaggerHub](https://app.swaggerhub.com/apis-docs/allratestoday/allratestoday-exchange-rate-central-bank-rates-api/2.2.0)
- [GitHub](https://github.com/AllRates-Today/jocustoms-exchange-rate)

## 📜 License

MIT
