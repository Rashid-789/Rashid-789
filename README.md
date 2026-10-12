<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/header-dark.svg">
    <img src="./assets/header-light.svg" width="100%" alt="Rashid Khan, backend and mobile developer. I build backends and mobile apps for agencies that are strong on design and frontend but don't keep a deep backend bench. Rawalpindi, Pakistan, UTC+5.">
  </picture>
  
  <br><br>
  <a href="https://rashidiya-portfolio.vercel.app"><img src="https://img.shields.io/badge/Portfolio-006D77?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/rashid-khan-70a018360"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:rashidiyaoo7@gmail.com"><img src="https://img.shields.io/badge/Email-A34700?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</div>

## About

I've been shipping production web and mobile systems for a little over three years. Most of it is the part users don't see: multi-role marketplaces, payment and subscription logic, admin panels, and the database design underneath. Lately that includes Flutter apps that sit on top of backends I wrote.

Almost all of that code lives in private client repositories, so this page is the summary. The full case studies are on [my portfolio](https://rashidiya-portfolio.vercel.app/work).

## Selected work

<p align="center">
  <a href="https://rashidiya-portfolio.vercel.app/work/autonect"><picture><source media="(prefers-color-scheme: dark)" srcset="./assets/work-autonect-dark.svg"><img src="./assets/work-autonect-light.svg" width="49%" alt="Autonect. UK car-parts marketplace, 2026. A buyer types a registration, the DVLA API fills in the car, and one request reaches every matching parts supplier."></picture></a>
  <a href="https://rashidiya-portfolio.vercel.app/work/hareer-plus"><picture><source media="(prefers-color-scheme: dark)" srcset="./assets/work-hareer-plus-dark.svg"><img src="./assets/work-hareer-plus-light.svg" width="49%" alt="Hareer+. Multi-vendor commerce platform, Libya, 2026. Restaurants and clothing stores on one platform, with an order flow chosen by store type."></picture></a>
  <br>
  <a href="https://rashidiya-portfolio.vercel.app/work/chassis-doctor"><picture><source media="(prefers-color-scheme: dark)" srcset="./assets/work-chassis-doctor-dark.svg"><img src="./assets/work-chassis-doctor-light.svg" width="49%" alt="Chassis Doctor. Vehicle inspection app, UK, 2026. Live on Google Play. Audited Supabase row-level security before launch and closed 20 critical access holes in six reversible migrations."></picture></a>
  <a href="https://rashidiya-portfolio.vercel.app/work/luumilo"><picture><source media="(prefers-color-scheme: dark)" srcset="./assets/work-luumilo-dark.svg"><img src="./assets/work-luumilo-light.svg" width="49%" alt="Luumilo. Parenting app, Netherlands, 2025 to 2026. An AI assistant with conversation memory: a 20-message window, rolling summaries and carry-forward between sessions."></picture></a>
</p>

<details>
<summary><b>How each one was built</b></summary>
<br>

**[Autonect](https://rashidiya-portfolio.vercel.app/work/autonect)**: iOS, Android and web admin. Buyers were phoning scrapyards one at a time to find a used part. Here a buyer types a registration number, the app pulls the vehicle details from the DVLA API, and the request reaches every matching supplier at once. Buyers, parts suppliers and auto electricians each work and pay differently, so I chose PostgreSQL over MongoDB to keep permissions and money movement enforced by the database. Stripe covers three revenue paths: supplier subscriptions, pay-per-lead credits and commission on sales.

**[Hareer+](https://rashidiya-portfolio.vercel.app/work/hareer-plus)**: backend and admin panel. Restaurants and clothing stores only look alike from the outside: one sells food with short fulfilment windows, the other sells stock with sizes and variants. I built two separate order flows, picked automatically by the store type a vendor chooses at onboarding. I owned the backend architecture and the admin panel, and wrote the technical spec the build ran from. NestJS with Redis and BullMQ for notifications, order events and settlement runs, hosted in AWS Milan for latency to North Africa, with LYPay and cash on delivery.

**[Chassis Doctor](https://rashidiya-portfolio.vercel.app/work/chassis-doctor)**: backend, admin panel and security audit. Before launch I audited Supabase row-level security across every table. Twenty critical holes came out of it, where data scoped to one user was reachable by any signed-in client. I fixed them in six sequential migrations rather than one large change, so each step could be reviewed and reversed on its own. The app is [live on Google Play](https://play.google.com/store/apps/details?id=com.chassisdoctor.app).

**[Luumilo](https://rashidiya-portfolio.vercel.app/work/luumilo)**: web and mobile. The AI assistant forgot everything between sessions, so parents re-explained their child's age each time they opened it. The fix was conversation memory on the backend: a 20-message sliding window, rolling summaries so older context survives, and carry-forward between sessions. I also built the React frontend, landing page and admin panel, and set up deployment on S3 and CloudFront with GitHub Actions.

</details>

## Stack

<table>
  <tr>
    <td width="110"><b>Backend</b></td>
    <td>
      <picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=nodejs,nestjs,express,postgres,mongodb,prisma,redis&theme=dark"><img src="https://skillicons.dev/icons?i=nodejs,nestjs,express,postgres,mongodb,prisma,redis&theme=light" height="44" alt="Node.js, NestJS, Express, PostgreSQL, MongoDB, Prisma, Redis"></picture>
      <br><sub>Plus BullMQ for background jobs</sub>
    </td>
  </tr>
  <tr>
    <td><b>Frontend</b></td>
    <td><picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=react,nextjs,ts,tailwind&theme=dark"><img src="https://skillicons.dev/icons?i=react,nextjs,ts,tailwind&theme=light" height="44" alt="React, Next.js, TypeScript, Tailwind CSS"></picture></td>
  </tr>
  <tr>
    <td><b>Mobile</b></td>
    <td>
      <picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=flutter,dart&theme=dark"><img src="https://skillicons.dev/icons?i=flutter,dart&theme=light" height="44" alt="Flutter, Dart"></picture>
      <br><sub>Riverpod for state</sub>
    </td>
  </tr>
  <tr>
    <td><b>Infra</b></td>
    <td>
      <picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=aws,supabase,githubactions,vercel,firebase&theme=dark"><img src="https://skillicons.dev/icons?i=aws,supabase,githubactions,vercel,firebase&theme=light" height="44" alt="AWS, Supabase, GitHub Actions, Vercel, Firebase"></picture>
      <br><sub>AWS: EC2, S3, RDS, CloudFront</sub>
    </td>
  </tr>
  <tr>
    <td><b>Services</b></td>
    <td>Stripe · RevenueCat · Firebase FCM · Twilio · OpenAI</td>
  </tr>
</table>

## How I work

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/how-i-work-dark.svg">
  <img src="./assets/how-i-work-light.svg" width="100%" alt="UTC+5, UK hours covered: based in Pakistan, with a full UK working-day overlap and part of the US morning. A written update every day, posted at the end of each working day. Questions asked once, clearly, instead of guessing and rebuilding later. White-label by default: your client never hears my name unless you want them to.">
</picture>

## Contact

<a href="mailto:rashidiyaoo7@gmail.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/contact-dark.svg">
    <img src="./assets/contact-light.svg" width="100%" alt="One developer for your backend and mobile builds. Email rashidiyaoo7@gmail.com. I reply within one working day.">
  </picture>
</a>

<p align="center"><sub>rashidiyaoo7@gmail.com · Rawalpindi, Pakistan (UTC+5) · I reply within one working day</sub></p>
