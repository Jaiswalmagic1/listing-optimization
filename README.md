# Listing Optimization

An AI-powered, marketplace-aware skill for optimizing e-commerce product listings using search performance data, existing listing content, and product images.

The skill is designed to help sellers improve product listings while keeping keyword usage relevant, natural, and consistent with the actual product.

## What It Does

**Listing Optimization** collects the information needed to understand a product and its marketplace search performance, then produces an optimized listing for the selected marketplace.

The skill is designed around a controlled workflow:

1. Select the marketplace.
2. Collect required listing and performance data.
3. Analyze the product images.
4. Analyze marketplace search-query performance.
5. Identify relevant high-value keywords.
6. Identify keywords or attributes that should be excluded.
7. Ask the seller to review and override exclusions if desired.
8. Generate the final optimized listing.

The skill does **not** generate the final listing before all required information has been collected.

## Supported Marketplaces

### Amazon

Currently supported with a detailed optimization workflow.

Amazon output includes:

* Item Name
* Product Description
* Bullet Points
* Generic Keywords
* Item Highlight

### Meesho

Marketplace-specific support is structured for future expansion.

### Flipkart

Marketplace-specific support is structured for future expansion.

Additional marketplaces can be added without changing the core optimization workflow.

## Amazon Optimization Methodology

Amazon optimization uses multiple sources of information rather than relying only on keyword volume.

### 1. ASIN Search Query Performance

The skill analyzes product-level search performance such as:

* Search Query
* Search Query Score
* Search Query Volume
* Impressions
* ASIN Share
* Click Share
* Cart Add Share
* Purchase Share
* Visibility opportunities
* Conversion opportunities

### 2. Brand Search Query Performance

Brand-level search performance is used to identify search terms where the seller's brand is already receiving meaningful visibility, clicks, cart activity, or purchases.

This allows the optimization to leverage existing brand search relevance instead of starting keyword research from zero.

### 3. Existing Listing

The current:

* Item Name
* Product Description
* Bullet Points
* Generic Keywords
* Item Highlight

are reviewed before creating replacements.

### 4. Product Images

The main image and additional product images are analyzed to identify and verify product attributes such as:

* Design
* Shape
* Color
* Material appearance
* Product components
* Patterns
* Closures
* Chains
* Threads
* Stones
* Pearls
* Layers
* Other visible characteristics

The skill should not introduce unsupported product attributes simply because they appear in a keyword dataset.

## Keyword Strategy

The skill prioritizes keywords using a combination of:

* Search demand
* Search performance
* Brand-level performance
* ASIN-level performance
* Relevance to the product
* Existing listing coverage
* Product-image verification
* Marketplace-specific rules

High search volume alone does not automatically make a keyword suitable.

For example, a keyword containing an attribute such as `ghungroo`, `layered`, `german silver`, or `set` should not automatically be used if the product does not support that attribute.

## Keyword Exclusion Review

Before generating the final listing, the skill identifies important keywords or attributes that it recommends excluding.

For each exclusion, it explains the reason.

Examples:

* Attribute does not match the product.
* Material is not confirmed.
* Product type does not match.
* Keyword implies a set but the product is a single item.
* Keyword implies a feature that is not visible or supported.
* Keyword may create misleading product expectations.

The seller is given an opportunity to override the exclusion.

The final listing is generated only after this review.

## One-Question-at-a-Time Workflow

The skill intentionally collects information sequentially.

It does not ask the seller to provide a large checklist in one message.

For example:

> Which platform is this listing for?

After the seller answers:

> Please provide the ASIN.

Then the next required input is requested.

This makes the workflow easier to use and allows the skill to validate information as it is provided.

## Typical Amazon Workflow

```text
Start
  ↓
Select Marketplace
  ↓
Amazon
  ↓
ASIN
  ↓
ASIN Search Query Performance
  ↓
Brand Search Query Performance
  ↓
Current Item Name
  ↓
Current Product Description
  ↓
Current Bullet Points
  ↓
Current Generic Keywords
  ↓
Current Item Highlight
  ↓
Main Product Image
  ↓
Additional Product Images
  ↓
Keyword + Product Analysis
  ↓
Proposed Keyword Exclusions
  ↓
Seller Review / Override
  ↓
Final Optimized Listing
```

## Design Principles

### Accuracy over keyword stuffing

Keywords should describe the actual product.

### Search performance over assumptions

Available marketplace search data should be used whenever possible.

### Relevance over raw volume

A lower-volume keyword that closely matches the product may be more useful than a high-volume keyword describing a different product.

### Existing brand strength matters

Brand-level search performance can reveal search terms where the seller already has relevance.

### Images are evidence

Visible product characteristics should be considered when deciding whether a keyword or product claim is appropriate.

### Seller remains in control

The skill identifies recommendations and exclusions, but the seller gets an opportunity to review important exclusions before the final listing is produced.

## Repository Structure

```text
listing-optimization/
│
├── .agents/
│   └── skills/
│       └── listing-optimization/
│           │
│           ├── SKILL.md
│           │
│           └── references/
│               ├── amazon.md
│               ├── meesho.md
│               ├── flipkart.md
│               └── README.md
│
└── README.md
```

## Extending the Skill

The skill is designed to support additional marketplaces.

A new marketplace should generally contain:

* Marketplace-specific fields
* Title rules
* Description rules
* Bullet/feature rules
* Search-term rules
* Character limits
* Restricted terminology
* Marketplace-specific keyword behavior
* Required attributes
* Image requirements
* Output format

The core workflow should remain consistent while marketplace-specific rules are maintained separately.

## Intended Users

This skill can be used by:

* Marketplace sellers
* E-commerce brands
* Listing optimization specialists
* Catalog managers
* E-commerce agencies
* Marketplace consultants
* AI agents working with product catalogs

## Status

**Current version:** 1.0

**Primary marketplace:** Amazon

**Expansion planned:** Meesho, Flipkart and additional marketplaces

## Contributing

Marketplace rules and search behavior change over time.

Contributions that improve:

* Marketplace-specific rules
* Keyword analysis
* Listing quality checks
* Product attribute validation
* Search performance interpretation
* Image-based product verification

are welcome.

When adding marketplace rules, keep them in the relevant marketplace reference file rather than changing the core workflow unnecessarily.

## License

Choose an appropriate open-source license before publishing this repository for public use.


## Download the latest skill

The repository automatically publishes the latest version of the portable skill whenever the `main` branch is updated.

**[Download the latest Listing Optimization Skill ZIP](https://github.com/Jaiswalmagic1/listing-optimization/releases/latest/download/listing-optimization.zip)**

The download contains the current `listing-optimization` skill folder and its marketplace reference files. You do not need to manually create the ZIP after future updates.

## Using the skill in ChatGPT

If your ChatGPT workspace has Skills enabled:

1. Open the sidebar and select **Plugins**.
2. In the Plugin Directory, select the **Skills** tab.
3. Select **Create** → **Upload from your computer**.
4. Upload a ZIP whose single top-level folder is `listing-optimization`, containing `SKILL.md` and the `references` directory.
5. Install/enable the skill.
6. In a new chat, invoke **Listing Optimization** explicitly (for example with the skill's @-mention if shown) or simply ask to optimize a marketplace listing when the skill is enabled.

The workflow then starts by asking which platform the listing is for and continues one question at a time. It does not generate final listing copy until all required inputs are collected and the keyword-exclusion checkpoint has been resolved.

For the current Amazon workflow, the required inputs are ASIN, ASIN-level Search Query Performance, brand-level Search Query Performance, current listing fields, and the first/main plus additional product images.

If the Skills tab is not available in your ChatGPT account or workspace, the skill cannot be installed through the ChatGPT UI on that account. The repository remains the portable source of truth and can be used with other Agent Skills-compatible tools.
