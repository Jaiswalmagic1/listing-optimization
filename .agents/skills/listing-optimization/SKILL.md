---
name: listing-optimization
description: Strict marketplace listing optimization workflow. Ask the platform first, then collect required inputs exactly one question at a time. Never optimize during intake. Before final output, present important keyword exclusions for seller approval.
---

# Listing Optimization

## Mandatory conversation rules

1. At the start of every new run, ask ONLY:
   **Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?**

2. After the platform is selected, ask exactly ONE required input per message.
   - Wait for the user's answer.
   - Then ask the next input.
   - Never list future inputs.
   - Never ask for multiple files/details in one message.

3. During intake, ONLY acknowledge the received input and ask for the next single input.
   Do not:
   - optimize or rewrite listing content
   - analyze keywords
   - audit the listing
   - recommend changes
   - preview the final strategy
   - infer the product from previous chats
   - refer to a previous product as the current product

4. The current run's inputs are the only source of truth.

5. After all required inputs are received, analyze them together.

6. Before generating final listing content, show important proposed keyword/attribute exclusions with a concrete reason for each, then ask:
   **Do you want to override any of these exclusions?**
   Wait for the seller's response.

7. Never introduce unsupported or false product claims, even if a keyword has high search demand.

---

# Amazon Workflow

When the user selects Amazon, ask these inputs in EXACTLY this order, one per message. The order follows the section order shown in Amazon Seller Central: Product Identity, Description, Product Details, then listing images. Search-performance data is collected first because it is the optimization evidence.

### 1. ASIN
Ask only:
**Please provide the ASIN for this listing.**

### 2. ASIN-level Search Query Performance
Ask only:
**Please provide the Search Query Performance data for this ASIN.**

### 3. Brand-level Search Query Performance
Ask only:
**Please provide the Brand-level Search Query Performance data for your brand.**

### 4. Product Identity — Item Name
Ask only:
**Please provide the current Item Name. You can find it in Amazon Seller Central under Product Identity.**

### 5. Product Identity — Item Highlight
Ask only:
**Please provide the current Item Highlight. You can find it in Amazon Seller Central under Product Identity. It is a single field with a 125-character limit.**

### 6. Description — Product Description
Ask only:
**Please provide the current Product Description. You can find it in Amazon Seller Central under Description.**

### 7. Description — Bullet Points
Ask only:
**Please provide the current Bullet Points. You can find them in Amazon Seller Central under Description.**

### 8. Product Details — Generic Keywords
Ask only:
**Please provide the current Generic Keywords. You can find them in Amazon Seller Central under Product Details.**

### 9. Main/First Listing Image
Ask only:
**Please upload the first/main image of the listing.**

### 10. Additional Listing/Product Images
Ask only:
**Please upload the remaining product/listing images.**

If there are no additional images, accept that answer and continue.

Do not begin analysis until all 10 steps are complete.

---

# Amazon Analysis

Analyze all collected evidence together:

- ASIN-level Search Query Performance
- Brand-level Search Query Performance
- Current listing fields
- Main image
- Additional images
- Explicit product facts supplied by the seller

Prioritize keywords based on:

- factual product relevance
- ASIN performance
- brand performance
- search demand/volume
- impressions
- ASIN impression share
- click share
- cart-add share
- purchase share
- brand impression/click/cart/purchase share
- available opportunity or conversion signals
- natural placement in the appropriate Amazon field

Search volume alone is never sufficient.

Brand-level performance is useful only when the keyword is relevant to the current product.

## Product verification

Use supplied facts and images to verify visible/product-supported details such as:

- product type
- design and shape
- color/finish
- visible quantity
- chains, threads, tassels, hooks, clasps and closures
- pearls, stones, beads, coins, charms and motifs
- layers and patterns
- other clearly supported visible features

Do not treat visual appearance alone as proof of material/composition when that fact cannot be established from the evidence.

## Exclusion review

Before final generation, identify important terms/attributes that should be excluded.

Typical reasons include:

- product mismatch
- unsupported attribute
- misleading implication
- different product type
- different quantity/configuration
- competitor brand
- ASIN
- irrelevant search intent
- unnecessary duplication

For every proposed exclusion, state the term and the reason.

Then ask exactly:
**Do you want to override any of these exclusions?**

Wait for the seller's answer before generating the final listing.

---

# Amazon Final Output

Only after all inputs are received AND the exclusion checkpoint is resolved, provide:

## Updated Item Name

## Updated Product Description

## Updated Bullet Points

## Updated Generic Keywords

## Updated Item Highlight

## Optimization Notes

Keep the notes brief and explain the main keyword strategy, important listing changes, exclusions, and any seller-approved overrides.

Do not provide an overall score, ranking, or unsupported performance prediction.

---

# Generic Keyword Rules

Do not include:

- competitor brand names
- ASINs
- irrelevant terms
- unsupported attributes
- misleading terms
- excessive repetition
- terms describing a different product type, material, quantity, or configuration

Follow marketplace-specific limits and formatting rules from the relevant reference.

---

# Meesho and Flipkart

When Meesho or Flipkart is selected:

- Ask platform-specific required inputs one at a time.
- Do not use Amazon field names/rules unless the marketplace reference explicitly supports them.
- Collect the main image and additional images separately.
- Do not generate anything until all required inputs are received.
- Run the same exclusion approval checkpoint.
- Generate only fields appropriate to that marketplace.

Use the corresponding marketplace reference file for marketplace-specific requirements.

---

# Final Quality Gate

Before final output, verify:

- correct marketplace
- every required input received
- no multiple-input request was made
- no early optimization was provided
- product claims are supported
- images were reviewed
- keyword strategy uses performance evidence and product relevance
- important exclusions were shown
- seller overrides were considered
- final fields are complete
- generic keywords contain no competitor brands or ASINs
- no unsupported attributes were introduced


## Amazon field-location and length guidance

When requesting current Amazon fields, tell the seller where to find each field:
- Item Name: Product Identity.
- Item Highlight: Product Identity. It is a single field with a 125-character limit.
- Product Description: Description tab.
- Bullet Points: Description tab.
- Generic Keywords: Product Details.

For Amazon Item Name optimization, treat **75 characters as the target title limit for this workflow**. Keep the optimized Item Name within 75 characters and use Item Highlight to carry important relevant product details that cannot fit naturally in the title. Do not force keywords into the title at the expense of readability.