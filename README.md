<a href="https://selzix.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg">
    <img alt="Mahidhar Kakumani — Founder, Selzix. I build commerce platforms end to end, from the Postgres schema to the cluster, for humans and AI agents." src="assets/header-dark.svg" width="100%">
  </picture>
</a>

<p>
  <a href="https://selzix.com"><img alt="Selzix" src="https://img.shields.io/badge/selzix.com-052E1E?style=flat-square&logoColor=F0C75A&label=building&labelColor=C8941F"></a>
  <a href="https://selzix.com/demo/"><img alt="Talk to the founder" src="https://img.shields.io/badge/talk_to_the_founder-052E1E?style=flat-square"></a>
  <a href="https://www.linkedin.com/in/mahidharkakumani/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="https://x.com/mahikmc"><img alt="X" src="https://img.shields.io/badge/@mahikmc-000000?style=flat-square&logo=x&logoColor=white"></a>
</p>

I'm a founder-engineer from India. I design the schema, write the API, ship the three frontends, run the servers, and increasingly write the tools that let AI agents operate the whole thing safely.

## Now building — [Selzix](https://selzix.com)

**Give Selzix an Instagram handle and get back a real online store in minutes.**
It's built for Indian sellers and D2C brands who sell through DMs today. The AI reads the account, works out what the business is, generates the copy, design and catalogue, and publishes a storefront. Customers can find the store, pay with UPI or card, and track their order. Pricing is a flat ₹5,000/month with no Selzix transaction fee.

```mermaid
flowchart LR
  IG["Instagram<br/>or Shopify"] --> AI["AI pipeline<br/>infer → generate → compose"]
  AI --> API["Hono API on Bun<br/>+ background workers"]
  AG(["AI agents"]) <--> MCP["MCP servers<br/>admin · seller"]
  MCP --> API
  API --- DATA[("Postgres · Redis<br/>Meilisearch")]
  API --> APPS["Storefront · Seller · Admin<br/>TanStack Start"]
  API --> EXT["Razorpay · Stripe · Dodo · UPI<br/>Shiprocket · Delhivery"]
```

| | |
|:--|:--|
| **~224k** lines of TypeScript, in one Turborepo monorepo | **1** engineer (me) |
| **~100** Postgres tables, fully typed from DB to UI | **3** apps: storefront, seller panel, admin panel |
| **33** storefront sections, including shoppable lookbooks, before/after sliders, bookings and multi-outlet delivery | **2** MCP servers with scoped keys, plus a screenshot service, so AI agents can build, edit and visually check stores |
| **3** payment gateways, plus UPI, COD, GST invoicing and 29 currencies | Vitest, Playwright E2E and **visual regression** test suites |

<sub>Also inside: a form builder, a blog with scheduling and SEO, stay bookings with iCal sync, custom domains, abandoned-cart recovery, customer segments, conversion funnels, web push and a seller-assist AI.</sub>

## Selected work

<table>
<tr>
<td width="50%" valign="top">

**Comparify** — quick-commerce price comparison<br>
Queries Zepto, Blinkit and Swiggy Instamart in parallel and matches the same product across all three into one comparison card.<br>
<sub>Hard part: matching the same product across three catalogues, and staying up when one of them goes down (circuit breaker + Redis cache).</sub><br>
<sub>`TypeScript` `Express` `Redis` `Docker`</sub>

</td>
<td width="50%" valign="top">

**Telegram bots on the edge**<br>
Serverless bots, including an affiliate-link rewriter and a single codebase that serves several ringtone-search bots.<br>
<sub>Hard part: zero-ops. Every bot is a Cloudflare Worker, so there are no servers to babysit.</sub><br>
<sub>`Cloudflare Workers` `Hono` `grammY`</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Price Tracker** — Telegram Mini App<br>
Tracks product prices, keeps the price history and sends alerts. I built it twice: first in Node/Hono, then in FastAPI with a Redis job queue.<br>
<sub>Hard part: scheduling price checks in the background without hammering the source sites.</sub><br>
<sub>`Hono` `Telegraf` `FastAPI` `Redis queue` `MongoDB` `Telegram Mini Apps`</sub>

</td>
<td width="50%" valign="top">

**Earlier, in public**<br>
[anonymousQA](https://github.com/ursmahi/anonymousQA) · [shorturl](https://github.com/ursmahi/shorturl) · [write-something](https://github.com/ursmahi/write-something) · [color-guesser](https://github.com/ursmahi/color-guesser) · [youtube-react](https://github.com/ursmahi/youtube-react) · [IoT pet feeder](https://github.com/ursmahi/Iot-based-pet-fedder-arduino)<br>
<sub>From an Arduino pet feeder in 2019 to React apps in 2023. Everything since then lives in private repos.</sub>

</td>
</tr>
</table>

## How I build

- **Agents are users too.** If an AI agent can't use a feature through a well-scoped tool, the feature isn't finished.
- **One type system, end to end.** The Postgres schema, API validation and UI forms all come from the same types.
- **Screenshots before claims.** Visual regression and E2E tests run before anything ships to real sellers.
- **Own the whole path.** From `docker compose up` in production to the checkout button, I'd rather understand every layer than rent it.
- **Ship, then sharpen.** Early users teach you more than a perfect roadmap does.

## Stack

<p>
  <img alt="Languages" src="https://skillicons.dev/icons?i=ts,js,py,java&theme=dark" height="40">&nbsp;&nbsp;
  <img alt="Frontend" src="https://skillicons.dev/icons?i=react,vite,tailwind&theme=dark" height="40">&nbsp;&nbsp;
  <img alt="Backend" src="https://skillicons.dev/icons?i=bun,nodejs,fastapi,spring&theme=dark" height="40">&nbsp;&nbsp;
  <img alt="Data" src="https://skillicons.dev/icons?i=postgres,redis,mongodb&theme=dark" height="40">&nbsp;&nbsp;
  <img alt="Infra" src="https://skillicons.dev/icons?i=docker,kubernetes,aws,cloudflare,nginx,githubactions,linux&theme=dark" height="40">
</p>

<p>
  <img alt="Hono" src="https://img.shields.io/badge/Hono-E36002?style=flat-square&logo=hono&logoColor=white">
  <img alt="TanStack" src="https://img.shields.io/badge/TanStack-FF4154?style=flat-square&logo=reactquery&logoColor=white">
  <img alt="Drizzle" src="https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black">
  <img alt="Zod" src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white">
  <img alt="Turborepo" src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white">
  <img alt="Meilisearch" src="https://img.shields.io/badge/Meilisearch-FF5CAA?style=flat-square&logo=meilisearch&logoColor=white">
  <img alt="Better Auth" src="https://img.shields.io/badge/Better_Auth-000000?style=flat-square&logo=betterauth&logoColor=white">
  <img alt="MCP" src="https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white">
  <img alt="Vercel AI SDK" src="https://img.shields.io/badge/AI_SDK-000000?style=flat-square&logo=vercel&logoColor=white">
  <img alt="Razorpay" src="https://img.shields.io/badge/Razorpay-0C2451?style=flat-square&logo=razorpay&logoColor=white">
  <img alt="Stripe" src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white">
  <img alt="Helm" src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white">
  <img alt="Sentry" src="https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=sentry&logoColor=white">
</p>

## Latest from the Selzix blog

<!-- BLOG-POST-LIST:START -->
- [Customer Retention for Small D2C Brands: How to Get Repeat Buyers Without Ads](https://selzix-blog.selzix.com/blog/customer-retention-d2c-small-business)
- [How to Start an Online Store in India: The Complete 2026 Beginner's Checklist](https://selzix-blog.selzix.com/blog/start-online-store-india-checklist)
- [The Hidden Cost of "Free" Online Store Builders in India](https://selzix-blog.selzix.com/blog/hidden-cost-of-free-store-builders)
- [How to Turn Instagram Followers Into Paying Customers (Not Just Likes)](https://selzix-blog.selzix.com/blog/turn-instagram-followers-into-customers)
- [How to Write Product Descriptions That Sell (Not Just Instagram Captions)](https://selzix-blog.selzix.com/blog/product-descriptions-that-sell)
<!-- BLOG-POST-LIST:END -->

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ursmahi/ursmahi/output/snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/ursmahi/ursmahi/output/snake.svg">
  <img alt="Contribution graph being eaten by a snake" src="https://raw.githubusercontent.com/ursmahi/ursmahi/output/snake.svg" width="100%">
</picture>

---

<p align="center">
  <sub>Selling on Instagram? <a href="https://selzix.com">Try Selzix free for 14 days</a>. Building something in commerce or AI agents? <a href="https://x.com/mahikmc">Say hi</a>.</sub><br>
  <sub><i>There is no END to Learning.</i></sub>
</p>
