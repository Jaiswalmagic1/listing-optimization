# Amazon Listing Optimization Reference

## Seller Central section order

Use this order when collecting current listing fields:

1. **Product Identity**
   - Item Name — maximum 75 characters for this workflow.
   - Item Highlight — one single field, maximum 125 characters.
   - Occasion — controlled dropdown, maximum 5 selections.

2. **Description**
   - Product Description.
   - Bullet Points.

3. **Product Details**
   - Generic Keywords.
   - Set Name.
   - Holiday Type — controlled dropdown.

4. **Additional product field**
   - Pendant Description — maximum 100 characters, when applicable.

5. **Images**
   - Main/first listing image.
   - Additional listing/product images.

## Keyword methodology

Use ASIN-level and Brand-level Search Query Performance together. Prioritize factual product relevance first, then ASIN performance, brand performance, demand, visibility, clicks, cart adds, purchases, and natural placement.

High search volume alone does not make a keyword suitable.

## Exclusion review

Flag terms when the product is not a set, lacks a named feature, material is not confirmed, quantity/configuration differs, product type differs, the query is irrelevant, or it contains a competitor brand/ASIN. Always show important exclusions before final generation and ask whether the seller wants to override them.

## Image review

Use the first image and additional images to verify visible product characteristics. Do not claim composition/material from appearance alone when it is not established.

## Field rules

### Item Name
Keep within **75 characters**. Use Item Highlight for important relevant details that cannot fit naturally in the title. Do not force keywords at the expense of readability.

### Item Highlight
One single field, maximum **125 characters**. Use it for concise product features/details not already adequately represented by the title.

### Occasion
Controlled Amazon dropdown. Up to **5 selections**. Select only genuinely relevant occasions supported by the product/context.

### Product Description
Customer-facing paragraph describing unique features, product line details, and specifications without unsupported claims.

### Bullet Points
Customer-facing feature/benefit bullets. Do not use unsupported attributes or unnecessary keyword stuffing.

### Generic Keywords
Relevant customer-search terms without competitor brands, ASINs, irrelevant terms, unsupported attributes, or unnecessary repetition.

### Set Name
Located under Product Details. Provide the manufacturer's official product-set name when available. If no official name exists, summarize the type and number of components. Never invent an official manufacturer name. If the product is not a set, treat as not applicable.

### Holiday Type
Located under Product Details. Select the appropriate holiday or holidays from Amazon's controlled dropdown. Holidays should be culturally recognized collective celebrations and genuinely associated with the item/context. Do not select holidays solely for keyword coverage.

### Pendant Description
Maximum **100 characters** when applicable. Keep concise and product-specific. Describe relevant visible/design characteristics without unsupported material or feature claims.

## Output

Return:
- Updated Item Name
- Updated Item Highlight
- Updated Occasion
- Updated Product Description
- Updated Bullet Points
- Updated Generic Keywords
- Updated Set Name
- Updated Holiday Type
- Updated Pendant Description when applicable
- Brief Optimization Notes
