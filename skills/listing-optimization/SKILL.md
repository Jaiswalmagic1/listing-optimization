---
name: listing-optimization
description: Strict marketplace listing optimization workflow. Ask the platform first, collect required inputs exactly one question at a time with the exact Seller Central location for each field, never optimize during intake, review proposed keyword exclusions with the seller before final output, and return marketplace-specific optimized fields with a before-vs-updated comparison table.
---

# Listing Optimization

## Mandatory conversation rules

1. Start every new run by asking ONLY: **Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?**
2. After the platform is selected, ask exactly ONE required input per message. Never list the remaining inputs.
3. Every data-request question MUST state the exact marketplace interface location where the seller can find that field, using the format **Marketplace → Section → Field** whenever known.
4. During intake, only acknowledge the received input and ask for the next single input. Do not optimize, analyze, audit, recommend changes, or preview strategy.
5. The current run's inputs are the only source of truth. Do not reuse a previous product's details.
6. If the user supplies multiple requested inputs in one message, record them and ask only for the next missing input.
7. Do not generate final listing content until every required input has been received.
8. Before final output, show important proposed keyword/attribute exclusions with a concrete reason for each and ask: **Do you want to override any of these exclusions?** Wait for the answer.
9. Never introduce unsupported or false product claims.

# Amazon Workflow

When Amazon is selected, collect the following in EXACTLY this order, one question per message. The order follows the Amazon Seller Central sections: Product Identity → Description → Product Details. Search-performance evidence is collected first because it drives the optimization.

### 1. SKU
Ask only: **Please provide the SKU ID for this listing, if available.**

Use the SKU for the chat naming convention: **[SKU] - [Platform] - Listing Optimization**. If no SKU is available, use **[Platform] - Listing Optimization**.

### 2. ASIN
Ask only: **Please provide the ASIN for this listing. You can find it in Amazon Seller Central under: Product Identity → ASIN.**

### 3. ASIN-level Search Query Performance
Ask only: **Please provide the Search Query Performance data for this ASIN. You can find it in Amazon Seller Central under the Search Query Performance report/dashboard for the ASIN.**

### 4. Brand-level Search Query Performance
Ask only: **Please provide the Brand-level Search Query Performance data for your brand. You can find it in Amazon Seller Central under the Brand-level Search Query Performance report/dashboard.**

### 5. Product Identity — Item Name
Ask only: **Please provide the current Item Name. You can find it in Amazon Seller Central under: Product Identity → Item Name.**

### 6. Product Identity — Item Highlight
Ask only: **Please provide the current Item Highlight. You can find it in Amazon Seller Central under: Product Identity → Item Highlight. It is a single field with a 125-character limit.**

### 7. Description — Product Description
Ask only: **Please provide the current Product Description. You can find it in Amazon Seller Central under: Description → Product Description.**

### 8. Description — Bullet Points
Ask only: **Please provide the current Bullet Points. You can find them in Amazon Seller Central under: Description → Bullet Points.**

### 9. Product Details — Generic Keywords
Ask only: **Please provide the current Generic Keywords. You can find them in Amazon Seller Central under: Product Details → Generic Keywords.**

### 10. Product Details — Set Name
Ask only: **Please provide the current Set Name. You can find it in Amazon Seller Central under: Product Details → Set Name.**

### 11. Product Details — Occasion
Ask only: **Please provide the current Occasion selection. You can find it in Amazon Seller Central under: Product Details → Occasion. Occasion should represent the specific event or celebration for which the jewelry item is designed or appropriate to wear.**

### 12. Product Details — Holiday Type
Ask only: **Please provide the current Holiday Type selection. You can find it in Amazon Seller Central under: Product Details → Holiday Type. Holiday Type is selected from an Amazon dropdown.**

### 13. Pendant Description
Ask only: **If this listing has a pendant, please provide the current Pendant Description. You can find it in Amazon Seller Central in the pendant-related product attribute/details field. It has a 100-character limit. If the product does not have a pendant, tell me that.**

### 14. Main/First Listing Image
Ask only: **Please upload the first/main image of the listing. You can find/manage the listing images in Amazon Seller Central under the listing's Images section.**

### 15. Additional Listing/Product Images
Ask only: **Please upload the remaining product/listing images. You can find/manage them in Amazon Seller Central under the listing's Images section. If there are no additional images, tell me that.**

Do not begin analysis until all 15 steps are complete.

# Amazon Analysis

Analyze the ASIN SQP, Brand SQP, current listing fields, product facts, main image, and additional images together. Image recommendations must follow the Image Recommendation Rule; do not manufacture image problems or suggest changes without evidence.

Prioritize keywords using factual relevance, ASIN performance, brand performance, search demand, impressions, ASIN share, click/cart/purchase signals, brand shares, opportunity/conversion signals, and natural placement. Search volume alone is never sufficient.

Use images to verify visible product type, design, shape, color/finish, visible quantity, chains/threads/tassels/hooks/clasps, pearls/stones/beads/coins/charms, layers, patterns, and other clearly supported features. Do not treat appearance alone as proof of material/composition.

# Image Recommendation Rule

Never recommend changing, replacing, adding, or redesigning an image merely because a different image might look better. Suggest an image change only when there is a specific, evidence-based reason: a clear marketplace requirement/compliance issue visible in the image, an objectively identifiable product-presentation problem, or performance data that supports an image-related hypothesis. Clearly separate observed facts from hypotheses. If the existing images satisfy requirements and there is no meaningful evidence that an image change is needed, explicitly leave the images unchanged.

# Exclusion Review

Identify important terms or attributes that should be excluded because of product mismatch, unsupported attributes, misleading implications, different product type/quantity/configuration, competitor brand/ASIN, irrelevant intent, or unnecessary duplication.

For each exclusion, state the term and reason. Then ask exactly:

**Do you want to override any of these exclusions?**

Wait for the seller's response before generating the final listing.

# Amazon Final Output

Return the following fields when applicable:

1. **Updated Item Name** — maximum 75 characters.
2. **Updated Item Highlight** — one single field, maximum 125 characters.
3. **Updated Product Description**.
4. **Updated Bullet Points**.
5. **Updated Generic Keywords**.
6. **Updated Set Name** — under Product Details. Use the manufacturer's official name if supplied. If no official name exists, summarize the set type and number of components. Never invent an official manufacturer name. If the product is not a set, say Not applicable.
7. **Updated Occasion** — specific event/celebration selections appropriate to the jewelry item, using Amazon's available values.
8. **Updated Holiday Type** — holiday/holidays genuinely associated with the item, using Amazon's available values.
9. **Updated Pendant Description** — maximum 100 characters, when applicable.

## Mandatory Before-vs-Updated Comparison

After the exclusion-review approval and before/alongside the final optimized listing, ALWAYS provide a comparison table showing the seller's original value and the proposed updated value.

Use this structure:

| Field | Previous Value | Updated Value |
|---|---|---|
| Item Name | Original value | Proposed value |
| Item Highlight | Original value | Proposed value |
| Product Description | Original value | Proposed value |
| Bullet Points | Original value | Proposed value |
| Generic Keywords | Original value | Proposed value |
| Set Name | Original value | Proposed value |
| Occasion | Original value | Proposed value |
| Holiday Type | Original value | Proposed value |
| Pendant Description | Original value | Proposed value |

Include only applicable fields, but do not omit a field merely because the value is unchanged. If no change is recommended, write **No Change** in the Updated Value column. Preserve the complete previous value where practical; for long fields, clearly identify the original content without misleadingly truncating it.

Then provide the final optimized fields in copy-ready form.

Then provide brief **Optimization Notes** explaining the main keyword strategy, important changes, exclusions, seller-approved overrides, and any fields intentionally left unchanged.

Do not provide an overall score, ranking, or unsupported performance prediction.

# Generic Keyword Rules

Do not include competitor brand names, ASINs, irrelevant terms, unsupported attributes, misleading terms, excessive repetition, or terms describing a different product type/material/quantity/configuration.

# Meesho and Flipkart

When Meesho or Flipkart is selected, use the corresponding marketplace reference. Keep the same core rules: platform first, one question at a time, every data-request question includes the marketplace location of the field, no premature optimization, image review, factual verification, exclusion approval, and a mandatory previous-vs-updated comparison table in the final output.

# Final Quality Gate

Before final output verify: correct marketplace; every required input received; every intake question included the field location; one-question intake was followed; no early optimization occurred; product claims are supported; images were reviewed; keyword strategy uses performance evidence and product relevance; exclusions were shown; overrides were considered; the previous-vs-updated comparison table is present; all final fields are complete; generic keywords contain no competitor brands or ASINs; and no unsupported attributes were introduced.
