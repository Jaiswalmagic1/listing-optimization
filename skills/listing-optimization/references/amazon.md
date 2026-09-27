# Amazon Listing Optimization Reference

## Required inputs

Collect, one at a time:

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

## Final fields

Return:

- Item Name
- Product Description
- Bullet Points
- Generic Keywords
- Item Highlight

## Keyword methodology

Use ASIN-level and brand-level Search Query Performance together.

Prioritize relevant terms using:

1. Product relevance and factual fit.
2. ASIN-level performance.
3. Brand-level performance.
4. Search volume/demand.
5. Visibility opportunities.
6. Click, cart-add, and purchase signals.
7. Natural placement in the relevant Amazon field.

Do not equate search volume with suitability.

If a query contains an attribute that is not supported by the product, flag it for exclusion rather than inserting it merely because it performs well.

## Exclusion examples

Common reasons to exclude a query include:

- Product is not a set but query says set.
- Product does not contain ghungroo.
- Product is not layered.
- Material is not confirmed.
- Product does not include earrings/necklace/accessory implied by the query.
- Query implies a quantity or configuration that is not present.
- Query is a competitor brand or ASIN.
- Query is irrelevant despite search demand.

Always show important exclusions before final generation and ask whether the seller wants to override them.

## Amazon Seller Central field locations

- Item Name: Product Identity.
- Item Highlight: Product Identity. It is a single field with a 125-character limit.
- Product Description: Description tab.
- Bullet Points: Description tab.
- Generic Keywords: Product Details.

For this workflow, keep the optimized Amazon Item Name within **75 characters**. Important relevant details that do not fit naturally in the title should be considered for the single Item Highlight field, which has a 125-character limit.

## Existing listing review

Compare the current fields against the keyword evidence. Identify:

- Strong relevant terms missing from visible fields.
- Overused or redundant terms.
- Unsupported claims.
- Important product attributes missing from the copy.
- Opportunities to improve clarity and search relevance.

## Image review

Use the first image and additional images to verify visible product characteristics. Do not claim composition/material from appearance alone when it is not established.

## Output guidance

Keep copy customer-readable. Avoid keyword stuffing. Use the strongest relevant terms naturally in the appropriate fields. Generic keywords should avoid competitor brands, ASINs, and unnecessary repetition.



## Amazon Pendant Description

For listings with a pendant, include **Pendant Description** in the Amazon optimization output.

- Field: Pendant Description
- Maximum length: **100 characters**
- Keep it concise and product-specific.
- Describe the pendant's relevant visible/design characteristics without unsupported material or feature claims.
- Treat it as a separate output field; do not merge it into Item Highlight or Product Description.


## Amazon Occasion and Set Name

- **Occasion:** controlled dropdown field; maximum 5 selections.
- **Set Name:** provide the manufacturer's official product-set name. If no official name exists, summarize the type and number of components. Never invent an official manufacturer name. If not a set, treat it as not applicable.
