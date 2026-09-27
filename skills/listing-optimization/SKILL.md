---
name: listing-optimization
description: Optimize e-commerce marketplace listings using marketplace-specific rules, search performance data, existing listing content, and product images. Ask for the marketplace first, collect required inputs one question at a time, do not generate final copy until all required inputs are received, and review proposed keyword exclusions with the seller before final output.
---

# Listing Optimization

Use this skill when the user wants to optimize a marketplace product listing.

## Mandatory workflow

1. Ask the platform first. Ask exactly one question: "Which platform is this listing for? (Amazon, Meesho, Flipkart, or Other)"
2. Ask one thing at a time. Wait for each answer before asking the next required input. Never send the full checklist at once.
3. Do not generate the optimization early. Acknowledge received information, but do not draft, rewrite, rank keywords, or provide final listing content until all required inputs are collected.
4. Do not invent facts. Never assume material, size, quantity, closure, set composition, feature, certification, or other product attributes from a keyword alone.
5. Review images. Use the first/main image and additional listing images to verify visible product characteristics.
6. Run an exclusion checkpoint before final output. Identify important keywords or attributes you recommend excluding, explain why, and ask the seller whether they want to override any. Do not generate final copy until the seller has had that opportunity.
7. Respect seller overrides where factually supportable. Do not make a false product claim merely because the seller wants a keyword included.

## Amazon intake order

When Amazon is selected, ask in this order, one question at a time:

1. ASIN
2. ASIN-level Search Query Performance data
3. Brand-level Search Query Performance data
4. Current Item Name
5. Current Product Description
6. Current Bullet Points
7. Current Generic Keywords
8. Current Item Highlight
9. Main/first listing image
10. Other listing/product images

If an input is missing or unusable, request that specific input and stop the workflow until it is received.

## Amazon analysis

Use the Amazon reference file in references/amazon.md.

Analyze ASIN Search Query Performance, Brand Search Query Performance, current listing fields, product facts, and product images.

Prioritize keywords using:
- factual product relevance;
- ASIN performance;
- brand performance;
- search demand;
- visibility opportunities;
- click/cart/purchase signals;
- natural placement in the appropriate field.

High volume alone does not make a keyword suitable.

Consider available metrics such as Search Query, Search Query Score, Search Query Volume, impressions, ASIN share, click share, cart-add share, purchase share, brand shares, and explicit opportunity/conversion flags. Never fabricate missing metrics.

## Image analysis

Check visible:
- product type;
- shape/design;
- color/finish;
- visible quantity;
- chains, threads, tassels, hooks, clasps or closures;
- pearls, stones, beads, coins, charms or motifs;
- layers and patterns;
- relative size where the image supports it.

Image appearance alone is not definitive proof of composition/material when that fact is not established.

## Exclusion checkpoint

Before final generation, present meaningful exclusions with the term and reason. Typical reasons:
- product is not a set;
- feature is not present;
- material is unconfirmed;
- quantity/configuration differs;
- product type differs;
- keyword is irrelevant;
- competitor brand or ASIN;
- keyword would create a misleading expectation.

Ask whether the seller wants to override any exclusion.

## Final output

After all inputs and the exclusion checkpoint are complete, return the platform-specific optimized fields.

For Amazon return:
1. Updated Item Name
2. Updated Product Description
3. Updated Bullet Points
4. Updated Generic Keywords
5. Updated Item Highlight

Also provide a compact explanation of the main keyword strategy and important changes.

## Generic keyword rules

Do not use competitor brand names, ASINs, irrelevant terms, unsupported attributes, or unnecessary repetition. Follow marketplace-specific search-term limits and formatting rules from the relevant reference file.

## Other marketplaces

For Meesho, Flipkart, and future marketplaces, keep the same core workflow but use only the marketplace-specific rules in the relevant reference file. Do not import Amazon-specific field names, limits, or ranking assumptions into another marketplace.
