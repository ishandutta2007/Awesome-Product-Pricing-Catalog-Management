# Awesome-Product-Pricing-Catalog-Management

# Awesome Product & Pricing Catalog Management

> A curated list of top Product and Pricing Catalog Management platforms — both SaaS/Hosted commercial CPQ and pricing engines and open-source alternatives for managing product masters, price books, and complex pricing rules.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Chargebee Pricing Catalog](#chargebee-pricing-catalog)
  - [DealHub Adaptive Pricebook](#dealhub-adaptive-pricebook)
  - [Salesforce CPQ Price Books](#salesforce-cpq-price-books)
  - [Conga CPQ Catalog](#conga-cpq-catalog)
  - [Zuora Product Catalog](#zuora-product-catalog)
  - [Vendavo](#vendavo)
  - [Pricefx](#pricefx)
  - [Tacton CPQ](#tacton-cpq)
- [Open-Source Software](#-open-source-software)
  - [Open Mercato Product Configurator](#open-mercato-product-configurator)
  - [entirius-django-pricemanager](#entirius-django-pricemanager)
  - [Unopim](#unopim)
  - [ERPNext (Item & Price List)](#erpnext-item--price-list)
  - [Odoo (Product & Pricelist)](#odoo-product--pricelist)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Product and Pricing Catalog Management platforms. These are not open-source but are included as reference points for feature comparison.

### Chargebee Pricing Catalog
**Type:** Billing-native product catalog with multi-dimensional pricing models
Chargebee's catalog is built directly into its subscription billing platform, supporting **Flat Fee, Tiered, Stairstep, Volume, Usage, and Seat-Based pricing models** with multi-decimal price points [citation:1]. The catalog handles hybrid billing combining recurring fees, usage-based charges, and one-time items on a single invoice. **Advanced metering** allows custom SQL configurations to define complex meters from raw usage data, with schemaless usage support so pricing metrics can change without breaking ingestion. Account hierarchies support parent-child structures up to 30 levels deep, and **Approvals on Price Points** add governance to catalog changes. The catalog is available on the Flow plan ($160/mo) and above.
**Best for:** Subscription businesses already on Chargebee wanting a billing-integrated catalog with advanced usage metering and hybrid pricing without a separate CPQ system.

### DealHub Adaptive Pricebook
**Type:** CPQ with hierarchical product structuring and multi-dimensional pricebook
DealHub provides an **Adaptive Pricebook** with hierarchical product structuring, multi-dimensional pricing, and guided quote configuration [citation:15]. The product catalog API allows programmatic management of products and bundles, with **price types including SOLID (fixed), ERP (external), and FROM_ALL_QUOTE (percentage of total)** [citation:2]. Pricing rules are evaluated sequentially in advanced mode, and product assignments can auto-add products based on conditions like region or playbook answers. The platform supports every sales motion—new business, renewals, co-terms, expansions, and amendments—with usage-based, tiered, and hybrid pricing models [citation:15].
**Best for:** Sales-led organizations needing a modern CPQ with hierarchical product structures, multi-dimensional pricebooks, and headless API quoting for self-service or PLG motions.

### Salesforce CPQ Price Books
**Type:** Enterprise CPQ with price books and layered pricing exceptions
Salesforce CPQ uses **Price Books** as the foundation—a collection of price book entries mapping products to prices [citation:3]. When a quote is created, the selected price book provides the starting price, and CPQ layers on **pricing exceptions** and adjustments. Key pricing tools beyond price books include **Block Pricing** (flat price for quantity ranges), **Percent of Total (PoT)** pricing (percentage of other products' sum), **Option Pricing Override** (different price inside a bundle), **Cost Plus Markup**, and **Contracted Pricing** (account-specific prices) [citation:3]. A critical constraint: if a product lacks a price book entry in the selected price book, it won't appear in product selection and can't be added to the quote.
**Best for:** Salesforce-centric enterprises already on the platform needing CPQ with layered pricing exceptions and the ability to maintain multiple price books for different customer segments.

### Conga CPQ Catalog
**Type:** CPQ with unified admin console for products, categories, and price lists
Conga CPQ provides a dedicated **CPQ Admin console** with primary tabs for **Products, Catalog, and Pricing** [citation:4]. The Products tab manages the product list with search filters and cloning capabilities. The Catalog tab manages categories, and the Pricing tab manages price lists. The admin console allows creating a product and associating it with categories, price lists, and price list items on a single page. Products can also be cloned to create new configurations based on existing ones.
**Best for:** Organizations needing a structured admin interface for managing product hierarchies, categories, and price lists within a CPQ for Salesforce.

### Zuora Product Catalog
**Type:** Enterprise monetization with multi-entity and multi-currency catalog
Zuora's product catalog is part of its broader subscription management platform, supporting multi-entity management to segment financial data by geography, currency, or product line [citation:5]. The platform handles consumption revenue recognition and contract modifications for usage-based offerings. Zuora CPQ for Salesforce provides guided selling, rules engine, and ramps for subscription quoting. The catalog scales to up to 500,000 or 2,000,000 active subscribers depending on edition.
**Best for:** Large enterprises with complex, multi-entity operations needing a catalog integrated with enterprise-grade billing and revenue recognition.

### Vendavo
**Type:** AI-powered pricing for massive SKU catalogs
Vendavo specializes in pricing for distributors and manufacturers with **massive SKU catalogs**, using AI to analyze cost changes, transaction history, customer segments, and market signals to recommend optimal prices [citation:6]. The platform manages bracket pricing, negotiated customer agreements, and layered pricing rules, with automation of price updates as costs change. It provides visibility into margin leakage and customer-specific price proliferation, with rebate and incentive management to control hidden margin risk.
**Best for:** Food & beverage distributors and manufacturers managing thousands of SKUs with cost volatility and bracket pricing complexity.

### Pricefx
**Type:** AI pricing software with price waterfall visibility
Pricefx provides AI-driven pricing for finance and costing teams, with a focus on **price waterfall visibility** across manufacturing, distribution, and process industries [citation:7]. It tracks costs in real-time and provides decision support for pricing rules, automation of operational processes, and collaboration with sales on data-driven insights. The platform claims 70X ROI in the first year and 8.4% margin improvement within 12 months of Go-Live.
**Best for:** Finance teams needing granular cost-to-price visibility and AI-recommended pricing across complex product hierarchies.

### Tacton CPQ
**Type:** CPQ for complex manufacturing with constraint-based configuration
Tacton CPQ is purpose-built for **complex manufacturing** with guided selling, dynamic pricing, visual configuration, and **constraint-based configuration intelligence** [citation:10]. It validates technical compatibility across software versions, hardware models, and multi-vendor solutions, with partner-specific pricing and tier-based programs. Tacton claims 30% sales/quoting labor cost savings and 60% order error cost savings. It integrates with CRM, ERP, PLM, CAD, and PIM systems.
**Best for:** Manufacturers of highly configurable products needing technical validation and BOM-driven pricing rather than simple catalog lookups.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Product and Pricing Catalog Management tools. The open-source ecosystem is **very limited** for full CPQ, but several projects cover product information management and price management.

### Open Mercato Product Configurator
**Stack:** TypeScript / PostgreSQL / Next.js | **License:** Open Source
Open Mercato's Product Configurator module is an open-source CPQ component for **configured products with rules, formulas, and bill-of-materials pricing** [citation:12]. The engine is a pure, deterministic evaluator in two steps: **structure** (definition, selections → settled selections, visibility, formulas, BOM quantities) and **price** (structure, unit prices, currency exponent → totals, hash). Model definitions are versioned JSON documents validated by zod, with publishing freezing a version and storing its hash. The **Studio** provides backend pages to author models through forms and tables, including a text expression editor and BOM row editor. "Configure and add to quote" writes a snapshot, then a quote line through the sales module, with reconciliation so retries never create duplicate lines. **Important:** This is a module within the broader Open Mercato ERP/CRM platform, not a standalone CPQ product—you need the full platform to use it.
**Best for:** Developers building an open-source sales/ERP stack who need CPQ functionality with deterministic evaluation, versioned models, and BOM-based pricing, accepting the Open Mercato platform dependency.

### entirius-django-pricemanager
**Stack:** Python / Django / PostgreSQL | **License:** MPL-2.0
entirius-django-pricemanager is a Django module for **product prices in the Entirius open-source modular ecommerce platform** [citation:13]. It stores one current price per product, sales channel, country, and currency, with an append-only history of every change. Key features include:
- **Net/gross calculation** from tax classes and country-specific tax rates
- **Special prices** with validity dates, attribute-level prices, and customer tier prices
- **Write guards**: a precedence table decides which price source may overwrite another, with bounds enforcing a floor from minimum price and minimum margin over purchase cost
- **CSV imports** for prices and tax rates via management commands
- **Admin REST API** for price editing, channels, and tax classes, used by the CMS

Requires Python 3.11+, Django 5.0+, PostgreSQL 15+. It runs inside the Entirius backend service (Volkanos) and supplies prices to the catalog and checkout [citation:13].
**Best for:** Teams building on the Entirius ecommerce platform needing price management with tax handling, history tracking, and write guards, accepting the Entirius ecosystem dependency.

### Unopim
**Stack:** PHP / Laravel | **License:** MIT
Unopim is an open-source **Product Information Management (PIM) and Digital Asset Management (DAM) platform** built on Laravel, designed to manage, enrich, and scale product data beyond **10 million products** [citation:11]. It is free forever with 10,955 GitHub stars and active development. While not a CPQ or pricing engine, it provides the **product master data foundation** that a pricing catalog depends on—managing attributes, categories, variants, and digital assets at scale.
**Best for:** Organizations needing an open-source PIM foundation to centralize product data before layering pricing logic on top, particularly those managing large catalogs.

### ERPNext (Item & Price List)
**Stack:** Python / Frappe Framework / MariaDB | **License:** GPL-3.0
ERPNext provides product catalog and pricing management through its **Item** master and **Price List** system. Items support variants, attributes, and UOMs, while Price Lists enable different pricing per customer, currency, or date range. The broader ERP includes inventory, purchasing, and selling integration. It is a full ERP rather than a dedicated CPQ or pricing engine, but provides the catalog and price list foundation within an open-source business suite.
**Best for:** Organizations already on ERPNext wanting product and price list management integrated with inventory and sales, accepting the full ERP platform scope.

### Odoo (Product & Pricelist)
**Stack:** Python / PostgreSQL | **License:** LGPL-3.0 (Community)
Odoo provides product catalog management through its **Product** model with variants, attributes, and categories, alongside **Pricelists** with rules for percentage discounts, fixed prices, and formulas based on cost or competitor price. The Community edition includes basic pricelist functionality; Enterprise adds advanced features. Like ERPNext, it is a full ERP with catalog and pricing as modules.
**Best for:** Organizations already using or adopting Odoo wanting product and pricelist management within an integrated business suite.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Product Master | Price Lists | CPQ/Configurator | Self-Hosted | Best For |
|----------|---------|-------|----------------|-------------|-------------------|-------------|----------|
| **Chargebee** | Proprietary | Cloud | ✅ | ✅ Multi-model | (CPQ add-on) | ❌ | Billing-native catalog |
| **DealHub** | Proprietary | Cloud | ✅ Hierarchical | ✅ Adaptive | ✅ CPQ | ❌ | Multi-dimensional pricebook |
| **Salesforce CPQ** | Proprietary | Cloud | ✅ | ✅ Price Books | ✅ CPQ | ❌ | Layered pricing exceptions |
| **Conga CPQ** | Proprietary | Salesforce | ✅ Admin console | ✅ Price Lists | ✅ CPQ | ❌ | Structured CPQ admin |
| **Zuora** | Proprietary | Cloud | ✅ Multi-entity | ✅ | ✅ Zuora CPQ | ❌ | Enterprise multi-entity |
| **Vendavo** | Proprietary | Cloud | ✅ Massive SKUs | ✅ Bracket pricing | ❌ | ❌ | Distribution pricing |
| **Pricefx** | Proprietary | Cloud | ✅ | ✅ Price waterfall | ❌ | ❌ | AI cost-to-price visibility |
| **Tacton** | Proprietary | Cloud | ✅ | ✅ Partner pricing | ✅ Constraint-based | ❌ | Complex manufacturing CPQ |
| **Open Mercato** | Open Source | TS/Postgres | (Catalog) | ✅ BOM pricing | ✅ Configurator | ✅ | Open-source CPQ module |
| **entirius-pricemanager** | MPL-2.0 | Django/Postgres | (Check) | ✅ Price history | ❌ | ✅ | Ecommerce price management |
| **Unopim** | MIT | PHP/Laravel | ✅ 10M+ products | ❌ | ❌ | ✅ | Open-source PIM foundation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Product or Pricing Catalog Management tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for **dedicated CPQ and pricing catalog management** is **very limited and fragmented**. **Open Mercato's Product Configurator** is the most complete open-source CPQ effort, with deterministic evaluation, versioned models, and BOM pricing, but it requires the broader Open Mercato platform [citation:12]. **entirius-django-pricemanager** provides focused price management with tax handling and history for the Entirius ecommerce stack [citation:13]. **Unopim** fills the product master data gap as a scalable PIM [citation:11]. No open-source project replicates the full breadth of Salesforce CPQ, DealHub, or Tacton for enterprise-grade CPQ with complex pricing rules and partner channels—commercial platforms remain the practical choice for production-grade pricing catalog orchestration at scale.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
