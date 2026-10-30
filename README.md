# Awesome-Application-Marketplace

# Awesome-Application-Marketplace

**Top Application Marketplace (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Multi-Vendor Marketplaces, Extension Registries, App Store Infrastructure & Vendor Payouts*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Application Marketplaces**. These tools enable operators to build, launch, and scale marketplaces where multiple vendors or developers sell products, apps, or extensions—from fully managed enterprise marketplaces with buyer networks and billing infrastructure to self-hosted multi-vendor platforms and federated registries that give operators complete control over listings, commissions, and payouts.



**Examples** include Salesforce AppExchange, Shopify App Store, Atlassian App Hub, AWS Marketplace, Microsoft Commercial Marketplace, HubSpot App Marketplace, Google Workspace Marketplace, ServiceNow Store, Slack App Directory, and Zendesk Marketplace (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted application marketplaces, multi-vendor commerce, and open extension registries. **Critical note**: The open-source landscape splits into two distinct categories—**multi-vendor commerce platforms** (Mercur, Medusa, Saleor, GrandNode) that handle vendors, commissions, and payouts for physical or digital goods, and **extension registries** (Open VSX, ownCloud Marketplace) that distribute apps or plugins without transaction processing. No open-source project replicates Salesforce AppExchange's security review pipeline or AWS Marketplace's enterprise procurement integration.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Salesforce AppExchange](https://appexchange.salesforce.com/)**

  **Enterprise app marketplace** for the Salesforce ecosystem with security review, partner program, and billing integration. **Pricing**: Listing fees and revenue share vary; security review required. **Free tier**: Free apps available; commercial listings paid. **Best for**: ISVs building Salesforce apps wanting enterprise distribution with trust signals.



- **[Shopify App Store](https://apps.shopify.com/)**

  **Shopify's official app marketplace** for merchants to discover and install apps. **Pricing**: Revenue share model (Shopify takes a percentage of app revenue). **Free tier**: Free app listings available. **Best for**: developers building Shopify apps wanting distribution to millions of merchants with integrated billing.



- **[Atlassian App Hub](https://marketplace.atlassian.com/)**

  **App marketplace** for Jira, Confluence, and other Atlassian products. **Pricing**: Revenue share model; free and paid apps supported. **Free tier**: Free app listings available. **Best for**: developers building Atlassian ecosystem extensions wanting enterprise user access.



- **[AWS Marketplace](https://aws.amazon.com/marketplace)**

  **Cloud software and services marketplace** for AWS customers with enterprise procurement integration. **Pricing**: AWS takes a percentage of sales; private offers available. **Free tier**: Free trials and free products available. **Best for**: software vendors wanting enterprise distribution through AWS procurement.



- **[Microsoft Commercial Marketplace](https://azuremarketplace.microsoft.com/)**

  **Unified marketplace** for Azure, Dynamics 365, Microsoft 365, and Power Platform solutions. **Pricing**: Revenue share model; private offers available. **Free tier**: Free trials available. **Best for**: Microsoft partners wanting distribution across the Microsoft ecosystem.



- **[HubSpot App Marketplace](https://ecosystem.hubspot.com/marketplace/apps)**

  **App marketplace** for HubSpot CRM ecosystem. **Pricing**: Revenue share model; free apps available. **Free tier**: Yes. **Best for**: developers building HubSpot integrations for CRM users.



- **[Google Workspace Marketplace](https://workspace.google.com/marketplace)**

  **App marketplace** for Google Workspace integrations. **Pricing**: Free listings; Google takes a share of paid app revenue. **Free tier**: Free app listings available. **Best for**: developers building Google Workspace add-ons.



- **[ServiceNow Store](https://store.servicenow.com/)**

  **App marketplace** for ServiceNow platform. **Pricing**: Revenue share model; certified apps available. **Free tier**: Free apps available. **Best for**: partners building ServiceNow applications for enterprise customers.



- **[Slack App Directory](https://slack.com/apps)**

  **Official directory of publicly available Slack apps**. **Pricing**: Free listings; paid apps handled through Slack billing. **Free tier**: Yes. **Best for**: developers building Slack integrations wanting discovery by workspace admins.



- **[Zendesk Marketplace](https://www.zendesk.com/marketplace/)**

  **App marketplace** for Zendesk customer service platform. **Pricing**: Revenue share model; free apps available. **Free tier**: Yes. **Best for**: developers building Zendesk integrations for support teams.



## Open-Source GitHub Projects



- **[Mercur](https://github.com/mercurjs/mercur)**

  **Open-source marketplace platform built on MedusaJS** (license per repo) — **the most purpose-built open-source application marketplace engine** for multi-vendor commerce, with production-ready B2C support . **Features**: **Vendor onboarding and management** with dedicated vendor panel for products, orders, and store settings; **admin panel** for categories, vendors, commissions, and rules; **offer-based selling**—sellers list offers against master products with their own SKU, price, and stock; **checkout splitting**—one payment becomes one order per seller; **commission computation per order**; **Stripe Connect payouts** to seller accounts on a schedule; customizable storefronts for B2B and B2C; built-in Stripe and Resend integrations . **Tech stack**: MedusaJS 2.0 (Node.js, TypeScript), PostgreSQL, Redis. **Deploy**: Self-hosted (PostgreSQL + Redis + Mercur API server + worker + admin + vendor panel) or Medusa Cloud . **Trade-off**: **Commerce marketplace engine, not a SaaS app store**—it handles product offers, orders, and payouts, not app manifests, plugin lifecycles, or developer SDKs for app packaging. You own infrastructure, vendor onboarding policy, and payment processor relationships. No transaction fees on GMV . **Best for**: operators wanting full source control over a multi-vendor marketplace with automated commissions and Stripe Connect payouts—without per-transaction platform fees.



- **[Medusa](https://github.com/medusajs/medusa)**

  **Open-source headless commerce platform** (MIT) — **the foundation Mercur is built upon**, with modular commerce primitives for building custom marketplaces . **Features**: Modular architecture with separate modules for cart, payment, fulfillment, and pricing; API-first; TypeScript stack; the building blocks for advanced ecommerce stores, marketplaces, or any product needing commerce primitives . **Tech stack**: Node.js, TypeScript, PostgreSQL. **Deploy**: Self-hosted or Medusa Cloud. **Trade-off**: **Not a marketplace out of the box**—you build vendor management, commissions, and payouts yourself. Mercur adds those layers. **Best for**: developers wanting a modern, MIT-licensed commerce foundation to build a custom marketplace upon.



- **[Saleor](https://github.com/saleor/saleor)**

  **GraphQL-first headless commerce platform** (BSD-3-Clause) — **a mature composable framework with a growing app ecosystem** . **Features**: Single GraphQL endpoint; official TypeScript/JavaScript SDK; the **`saleor/apps` repository** is a central space for Saleor Apps, integrations, and the App Store; apps are deployed separately and communicate with Saleor via API . **Tech stack**: Python (Django), GraphQL, PostgreSQL. **Deploy**: Self-hosted or Saleor Cloud. **Trade-off**: **Platform, not a marketplace engine**—Saleor Apps is an app ecosystem, but multi-vendor marketplace capabilities (vendor onboarding, commissions, payouts) require custom development or third-party plugins. **Best for**: teams wanting a GraphQL-native commerce backend with an app ecosystem model.



- **[GrandNode](https://github.com/grandnode/grandnode2)**

  **Open-source cross-platform eCommerce platform** (GPL-3.0) — **supports multi-vendor business models on .NET Core and MongoDB** . **Features**: Explicitly supports B2B, B2C, Multi-Store, **Multi-Vendor**, Multi-Tenant, Multi-Language, and Multi-Currency models; built for ASP.NET Core with MongoDB/NoSQL storage . **Tech stack**: C# (.NET Core), MongoDB / Azure CosmosDB / Amazon DocumentDB / LiteDB. **Deploy**: Self-hosted. **Trade-off**: **.NET ecosystem-specific**—multi-vendor support is a business model option, but vendor governance and commission automation depth requires evaluation against your requirements. **Best for**: .NET teams wanting an open-source commerce platform with multi-vendor support in a NoSQL stack.



- **[Open VSX](https://github.com/eclipse/openvsx)**

  **Vendor-neutral open-source extension registry** (EPL-2.0) — **the most mature open-source application/extension marketplace infrastructure**, now at **1.0.0** with **600M+ extension downloads per month** . **Features**: Extension publishing, discovery, and distribution for VS Code-compatible editors (VSCodium, Eclipse Theia, Gitpod, Google Cloud Workstations, Salesforce Code Builder, SAP Business Application Studio); web application for browsing; CLI for publishing; TLS-secured Redis connections; read-only mode; security hardening . **Tech stack**: Java (Eclipse Vert.x), PostgreSQL, Redis. **Deploy**: Self-hosted (Docker) or public Open VSX Registry. **Trade-off**: **VS Code extension ecosystem specific**—not a general-purpose app marketplace. No transaction processing, vendor payouts, or multi-vendor commerce features. **Best for**: editor/IDE vendors wanting to offer a vendor-neutral extension registry independent of Microsoft's marketplace.



- **[ownCloud Marketplace](https://github.com/owncloud/marketplace)**

  **Backend-free, Git-backed app marketplace** — **the most radical open-source marketplace architecture** found in this research . **Features**: **Zero backend, zero database, zero server-side processing**—the Git repository is the source of truth; the catalogue is static JSON; **publishing an app is a pull request**; review happens on GitHub in public; the static site regenerates on merge. 42 apps, 324 releases, 36 publishers, 8 categories, plus 13 web extensions. Security properties follow from architecture: no server to compromise, no database to exfiltrate, no session tokens to steal . **Tech stack**: Static site generation, GitHub repository. **Deploy**: Static hosting (GitHub Pages or any static host). **Trade-off**: **Distribution only**—no payments, no vendor payouts, no multi-vendor commerce. It is a catalogue for free apps and extensions. **Best for**: open-source projects and foundations wanting a transparent, auditable, backend-free marketplace where publishing is a PR and the rules are public.



- **[Bagisto](https://github.com/bagisto/bagisto)**

  **Open-source Laravel eCommerce and multi-vendor marketplace platform** (license per repo) — **a full-stack option with a dedicated Multi Vendor Marketplace extension** . **Features**: Admin manages sellers, commissions, product approvals, and order handling; vendors get a dedicated dashboard for catalog, orders, and transactions; also supports B2B, multi-tenant SaaS marketplaces, POS, and headless commerce . **Tech stack**: Laravel (PHP), Vue.js. **Deploy**: Self-hosted (Docker one-liner available). **Trade-off**: **Full platform adoption required**—the marketplace is an extension, not a bolt-on to an existing store. Commission and payout automation depth varies by configuration. **Best for**: Laravel developers wanting a batteries-included commerce platform with native multi-vendor capabilities.



### Additional Strong Open-Source Options



- **Mobazha** — Open-source peer-to-peer commerce platform (Go, v0.3.0-rc.1) with storefronts, marketplaces, and crypto payments (BTC, BCH, LTC, BNB Chain). **Note**: Decentralized commerce, not a traditional app marketplace—vendors own their backend, and discovery happens across a network rather than a central catalogue . **Best for**: operators wanting a decentralized, vendor-owned marketplace model.

- **AppNest** — App store platform specification (Codeberg) with moderation, transparency, API, and plugin architecture. **Note**: **Specification/design document**, not a working implementation—describes intended features for an international app ecosystem . **Best for**: reference for app store requirements and governance design.

- **Open Store** — Decentralized blockchain app store (MIT). **Note**: Frontend landing page and blockchain-based distribution concept; no transaction processing or vendor payouts. **Best for**: exploring decentralized app distribution models .

- **Gerege Nexus App Store** — Go-based app store modules (registry, publisher, review, SSO clients) on the Gerege Nexus platform. **Note**: Early-stage (v0.1.0), platform-dependent, limited documentation . **Best for**: reference for modular app store architecture in Go.



**Frameworks for building custom systems**: Combine **Mercur** as the multi-vendor commerce engine for paid app or plugin distribution with **Open VSX** as the registry infrastructure for extension discovery, **ownCloud Marketplace** as the federated Git-backed catalogue pattern for free apps, and **Medusa** or **Saleor** as the commerce foundation—creating an application marketplace stack. **None of these provide the security review pipeline, enterprise procurement integration, or buyer network effects** of Salesforce AppExchange or AWS Marketplace; those require commercial platforms or significant custom development.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Application marketplace platforms handling developer credentials, billing data, and app permissions must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate security controls for app distribution and vendor payouts.

- **The "multi-vendor commerce platform" vs. "extension registry" vs. "federated catalogue" distinction is critical.** **Mercur, Bagisto, GrandNode, Medusa, and Saleor** are **commerce platforms**—they handle vendors, products, orders, commissions, and payouts. **Open VSX** is an **extension registry**—it publishes and distributes VS Code extensions but does not process payments or payouts. **ownCloud Marketplace** is a **federated, Git-backed catalogue**—publishing is a PR, there is no backend, no payments, and no vendor payouts . **No open-source project provides a turnkey Salesforce AppExchange or AWS Marketplace replacement.**

- **Mercur is the most purpose-built open-source marketplace engine** for multi-vendor commerce with commission calculation and Stripe Connect payouts . **The trade-off**: it is built for product offers and orders, not app/plugin packaging with manifests and developer SDKs. Adapting it for an app marketplace would require custom work on app validation and lifecycle management.

- **Open VSX is the most mature open-source registry infrastructure**—1.0.0, 600M+ monthly downloads, and adoption by Google, Salesforce, SAP, and Gitpod . **The trade-off**: it is VS Code extension-specific, not a general-purpose app marketplace.

- **ownCloud Marketplace's architecture is a statement.** By making the Git repository the catalogue and the PR the submission process, it makes marketplace governance auditable and removes the operator's ability to silently reject apps . **This is philosophically aligned with open-source values but practically limited**: no monetization, no security review pipeline, and discovery depends on Git commits.

- **Pricing opacity is universal across commercial ecosystem marketplaces.** Salesforce, Shopify, Atlassian, AWS, Microsoft, HubSpot, Google, ServiceNow, Slack, and Zendesk all have revenue share or listing fee models that vary by app type, volume, and negotiation. **Validate with direct vendor conversations against your app's pricing model and target ecosystem.**

- Self-hosted open-source solutions require proper server setup (PostgreSQL, Redis for Mercur), security hardening, vendor onboarding processes, and ongoing maintenance. **Marketplace platforms handle payments and developer credentials**—ensure your hosting meets PCI DSS requirements where applicable and your organization's security standards before processing transactions.



---



**Made for developers, platform teams, and organizations building transparent application marketplace solutions.**

Let's make Application Marketplaces more open, data-driven, and vendor-friendly.
