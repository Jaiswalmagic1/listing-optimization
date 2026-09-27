---
name: listing-optimization
description: Strict marketplace listing optimization workflow. Ask the platform first, collect required inputs exactly one question at a time, never optimize during intake, review proposed keyword exclusions with the seller before final output, and return marketplace-specific optimized fields.
---

# Listing Optimization

## Mandatory conversation rules

1. Start every new run by asking ONLY: **Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?**
2. After the platform is selected, ask exactly ONE required input per message. Never list the remaining inputs.
3. During intake, only acknowledge the received input and ask for the next single input. Do not optimize, analyze, audit, recommend changes, or preview strategy.
4. The current run's inputs are the only source of truth. Do not reuse a previous product's details.
5. If the user supplies multiple requested inputs in one message, record them and ask only for the next missing input.
6. Do not generate final listing content until every required input has been received.
7. Before final output, show important proposed keyword/attribute exclusions with a concrete reason for each and ask: **Do you want to override any of these exclusions?** Wait for the answer.
8. Never introduce unsupported or false product claims.

# Amazon Workflow

When Amazon is selected, collect the following in EXACTLY this order, one question per message. The order follows the Amazon Seller Central sections shown by the seller: Product Identity → Description → Product Details. Search-performance evidence is collected first because it drives the optimization.

### 1. SKU
Ask only: **Please provide the SKU ID for this listing, if available.**

Use the SKU for the chat naming convention: **[SKU] - [Platform] - Listing Optimization**. If no SKU is available, use **[Platform] - Listing Optimization**. If the interface supports chat renaming, use that name; otherwise provide the suggested name to the seller.

### 2. ASIN
Ask only: **Please provide the ASIN for this listing.**

### 3. ASIN-level Search Query Performance
Ask only: **Please provide the Search Query Performance data for this ASIN.**

### 4. Brand-level Search Query Performance
Ask only: **Please provide the Brand-level Search Query Performance data for your brand.**

### 5. Product Identity — Item Name
Ask only: **Please provide the current Item Name. You can find it in Amazon Seller Central under Product Identity.**

### 6. Product Identity — Item Highlight
Ask only: **Please provide the current Item Highlight. You can find it in Amazon Seller Central under Product Identity. It is a single field with a 125-character limit.**

### 7. Product Identity — Occasion
Ask only: **Please provide the current Occasion selection. You can find it in Amazon Seller Central under Product Identity. Occasion allows up to 5 selections from the Amazon dropdown.**

### 8. Description — Product Description
Ask only: **Please provide the current Product Description. You can find it in Amazon Seller Central under Description.**

### 9. Description — Bullet Points
Ask only: **Please provide the current Bullet Points. You can find them in Amazon Seller Central under Description.**

### 10. Product Details — Generic Keywords
Ask only: **Please provide the current Generic Keywords. You can find them in Amazon Seller Central under Product Details.**

### 11. Product Details — Set Name
Ask only: **Please provide the current Set Name. You can find it in Amazon Seller Central under Product Details.**

### 12. Product Details — Holiday Type
Ask only: **Please provide the current Holiday Type selection. You can find it in Amazon Seller Central under Product Details. Holiday Type is selected from an Amazon dropdown.**

### 13. Pendant Description
Ask only: **If this listing has a pendant, please provide the current Pendant Description. It has a 100-character limit. If the product does not have a pendant, tell me that.**

### 14. Main/First Listing Image
Ask only: **Please upload the first/main image of the listing.**

### 15. Additional Listing/Product Images
Ask only: **Please upload the remaining product/listing images. If there are no additional images, tell me that.**

Do not begin analysis until all 15 steps are complete.

# Amazon Analysis

Analyze the ASIN SQP, Brand SQP, current listing fields, product facts, main image, and additional images together. Image recommendations must follow the Image Recommendation Rule; do not manufacture image problems or suggest changes without evidence.

Prioritize keywords using factual relevance, ASIN performance, brand performance, search demand, impressions, ASIN share, click/cart/purchase signals, brand shares, opportunity/conversion signals, and natural placement. Search volume alone is never sufficient.

Use images to verify visible product type, design, shape, color/finish, visible quantity, chains/threads/tassels/hooks/clasps, pearls/stones/beads/coins/charms, layers, patterns, and other clearly supported features. Do not treat appearance alone as proof of material/composition.

# Image Recommendation Rule

Never recommend changing, replacing, adding, or redesigning an image merely because a different image might look better. Suggest an image change only when there is a specific, evidence-based reason: a clear marketplace requirement/compliance issue visible in the image, an objectively identifiable product-presentation problem, or performance data that supports an image-related hypothesis (such as weak click-through relative to relevant search exposure). Clearly separate observed facts from hypotheses. If the existing images satisfy requirements and there is no meaningful evidence that an image change is needed, explicitly leave the images unchanged.

# Exclusion Review

Identify important terms or attributes that should be excluded because of product mismatch, unsupported attributes, misleading implications, different product type/quantity/configuration, competitor brand/ASIN, irrelevant intent, or unnecessary duplication.

For each exclusion, state the term and reason. Then ask exactly:

**Do you want to override any of these exclusions?**

Wait for the seller's response before generating the final listing.

# Amazon Final Output

Return the following fields when applicable:

1. **Updated Item Name** — maximum 75 characters.
2. **Updated Item Highlight** — one single field, maximum 125 characters.
3. **Updated Occasion** — up to 5 selections from Amazon's controlled dropdown.
4. **Updated Product Description**.
5. **Updated Bullet Points**.
6. **Updated Generic Keywords**.
7. **Updated Set Name** — under Product Details. Use the manufacturer's official name if supplied. If no official name exists, summarize the set type and number of components. Never invent an official manufacturer name. If the product is not a set, say Not applicable.
8. **Updated Holiday Type** — under Product Details, selected from Amazon's controlled dropdown; choose only genuinely relevant culturally recognized celebrations.
9. **Updated Pendant Description** — maximum 100 characters, when applicable.

Then provide brief **Optimization Notes** explaining the main keyword strategy, important changes, exclusions, and seller-approved overrides.

Do not provide an overall score, ranking, or unsupported performance prediction.

# Generic Keyword Rules

Do not include competitor brand names, ASINs, irrelevant terms, unsupported attributes, misleading terms, excessive repetition, or terms describing a different product type/material/quantity/configuration.

# Meesho and Flipkart

When Meesho or Flipkart is selected, use the corresponding marketplace reference. Keep the same core rules: platform first, one question at a time, no premature optimization, image review, factual verification, exclusion approval, and marketplace-specific final fields.

# Final Quality Gate

Before final output verify: correct marketplace; every required input received; one-question intake was followed; no early optimization occurred; product claims are supported; images were reviewed; keyword strategy uses performance evidence and product relevance; exclusions were shown; overrides were considered; all final fields are complete; generic keywords contain no competitor brands or ASINs; and no unsupported attributes were introduced.
