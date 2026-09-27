---
name: listing-optimization
description: A strict marketplace listing optimization workflow. Ask which platform first, then collect every required input one question at a time. Never ask for multiple inputs together, never begin optimization early, never infer the product from prior chats, and always present proposed keyword exclusions for seller approval before final output.
---

# Listing Optimization

## Core behavior — MUST FOLLOW

This is a structured intake-and-approval workflow, not a general listing audit.

### Rule 1 — First message

At the start of a new Listing Optimization run, ask ONLY:

**Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?**

Do not add a checklist, optimization advice, examples, or any other question in that first message.

### Rule 2 — One question at a time

After the platform is selected, ask for exactly ONE required input.

Wait for the user's response.

Then ask for the next required input.

NEVER ask for multiple inputs in one message.

Do not say "send me the product listing and screenshots" when separate inputs are required.

Do not ask the user to send all details together.

### Rule 3 — No early optimization

Until every required input for the selected marketplace has been received:

- Do not rewrite the title.
- Do not rewrite bullets.
- Do not generate keywords.
- Do not analyze keyword opportunities.
- Do not provide a listing audit.
- Do not recommend changes.
- Do not produce a partial final listing.

You may only acknowledge the input and request the next single input.

### Rule 4 — Do not use prior-chat product assumptions

Do not assume that the product is one discussed in an earlier conversation.

Do not say things such as "if this is the product we were working on."

The current run's inputs are the source of truth.

### Rule 5 — Required-input completion gate

After the final required input is received, internally verify that every required input is present and usable.

Only then begin analysis.

### Rule 6 — Exclusion approval gate

Before generating the final listing, identify important keywords or attributes that you recommend excluding.

For each, state:

- Keyword/term.
- Why it is being excluded.
- Whether the reason is product mismatch, unsupported attribute, misleading implication, irrelevance, competitor term, duplication, or another concrete reason.

Then ask:

**Do you want to override any of these exclusions?**

Wait for the seller's response.

Only after this checkpoint may the final listing be generated.

### Rule 7 — Seller overrides

If the seller wants a keyword included, consider it where factually supportable.

Never create a false product claim merely to accommodate a keyword.

If the seller provides new factual information that changes an exclusion decision, incorporate that information into the analysis.

---

# Amazon Workflow

When the user selects **Amazon**, ask the following inputs in EXACTLY this order, one per message:

### 1. ASIN

Ask:

**Please provide the ASIN for this listing.**

Wait.

### 2. ASIN Search Query Performance

Ask:

**Please provide the Search Query Performance data for this ASIN.**

Wait.

### 3. Brand Search Query Performance

Ask:

**Please provide the Brand-level Search Query Performance data for your brand.**

Wait.

### 4. Current Item Name

Ask:

**Please provide the current Item Name.**

Wait.

### 5. Current Product Description

Ask:

**Please provide the current Product Description.**

Wait.

### 6. Current Bullet Points

Ask:

**Please provide the current Bullet Points.**

Wait.

### 7. Current Generic Keywords

Ask:

**Please provide the current Generic Keywords.**

Wait.

### 8. Current Item Highlight

Ask:

**Please provide the current Item Highlight.**

Wait.

### 9. Main/First Image

Ask:

**Please upload the first/main image of the listing.**

Wait.

### 10. Additional Images

Ask:

**Please upload the remaining product/listing images.**

Wait.

If there are no additional images, the user may say so. Do not block the workflow unnecessarily.

Only after step 10 is complete should analysis begin.

---

# Amazon Analysis

Analyze all collected evidence together:

1. ASIN Search Query Performance.
2. Brand Search Query Performance.
3. Existing listing fields.
4. Main image.
5. Additional images.
6. Explicit product facts supplied by the seller.

## Keyword prioritization

Prioritize relevant keywords using a combination of:

- Product relevance and factual fit.
- ASIN-level performance.
- Brand-level performance.
- Search volume/demand.
- Impressions.
- ASIN impression share.
- Click share.
- Cart-add share.
- Purchase share.
- Brand impression/click/cart/purchase share.
- High-demand/low-visibility indicators.
- Converts-well-once-seen indicators.
- Natural placement in the correct Amazon field.

Do not treat search volume alone as a reason to use a keyword.

A keyword that performs well for the brand is valuable only when it is relevant to the current product.

## Product verification

Use the supplied product details and images to verify:

- Product type.
- Design.
- Shape.
- Color/finish.
- Visible quantity.
- Components.
- Chains.
- Threads.
- Tassels.
- Hooks/closures.
- Pearls.
- Stones.
- Beads.
- Coins.
- Charms.
- Motifs.
- Layers.
- Patterns.
- Other visible features.

Do not claim a material or construction detail solely from visual appearance when it cannot be established.

## Existing listing analysis

Compare the current listing against the performance data and product evidence.

Look for:

- Strong relevant keywords that are missing.
- Relevant brand-performing terms that can naturally be incorporated.
- Redundant keyword usage.
- Unsupported attributes.
- Missing product differentiators.
- Unclear or weak wording.
- Opportunities to improve relevance without keyword stuffing.

## Keywords to exclude

Examples of reasons for exclusion:

- Query says "set" but product is a single item.
- Query says "ghungroo" but no ghungroo is present.
- Query says "layered" but product is not layered.
- Query says "german silver" but material is not established.
- Query implies a different product type.
- Query implies a different quantity or configuration.
- Competitor brand.
- ASIN.
- Irrelevant search intent.
- Keyword creates a misleading customer expectation.

Do not silently discard important keywords. Present them to the seller before final generation.

---

# Amazon Final Output

After the exclusion approval checkpoint, generate exactly these sections:

## Updated Item Name

Provide the optimized customer-facing title.

## Updated Product Description

Provide the optimized paragraph description.

## Updated Bullet Points

Provide the optimized bullets.

## Updated Generic Keywords

Provide the optimized backend search terms.

## Updated Item Highlight

Provide the optimized short feature/benefit phrases.

## Optimization Notes

Briefly explain:

- Which keyword groups were prioritized.
- How ASIN-level and brand-level performance influenced the strategy.
- Major listing changes.
- Important exclusions and any seller-approved overrides.

Do not provide an overall score, ranking, or unsupported performance prediction.

---

# Generic Keyword Rules

Do not include:

- Competitor brand names.
- ASINs.
- Irrelevant search terms.
- Unsupported attributes.
- Misleading terms.
- Excessive repetition.
- Terms that describe a different product type.

Follow marketplace-specific limits and formatting rules from the relevant reference file.

---

# Meesho and Flipkart

When Meesho or Flipkart is selected:

1. Ask the platform-specific required inputs one at a time.
2. Do not use Amazon field names or rules unless the marketplace reference explicitly supports them.
3. Collect the main image and additional images separately.
4. Do not generate anything until all required inputs are collected.
5. Run the same mandatory exclusion approval checkpoint.
6. Generate only the fields appropriate to that marketplace.

Marketplace-specific requirements belong in the corresponding reference file.

---

# Quality Gate

Before final output, verify:

- Correct marketplace selected.
- Every required input received.
- No input was skipped.
- No multiple-input request was made.
- No early optimization was provided.
- Product claims are supported.
- Images were reviewed.
- Keyword strategy uses both performance evidence and product relevance.
- Important exclusions were shown to the seller.
- Seller overrides were considered.
- Final fields are complete.
- Generic keywords contain no competitor brands or ASINs.
- No unsupported attributes were introduced.## Mandatory workflow

This skill is a sequential intake workflow. **Ask exactly one question per message and wait for the answer.**

### First question

Ask only:

**Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?**

Do not include a checklist or any additional request.

### After platform selection

Ask the next required input as a single question. Do not list future inputs.

For Amazon, use this exact sequence:

1. **ASIN** — ask only for the ASIN.
2. **ASIN-level Search Query Performance data** — ask only for this data.
3. **Brand-level Search Query Performance data** — ask only for this data.
4. **Current Item Name** — ask only for the current Item Name.
5. **Current Product Description** — ask only for the current Product Description.
6. **Current Bullet Points** — ask only for the current Bullet Points.
7. **Current Generic Keywords** — ask only for the current Generic Keywords.
8. **Current Item Highlight** — ask only for the current Item Highlight.
9. **Main/first listing image** — ask only for the main image.
10. **Other listing/product images** — ask only for the remaining images. If there are none, accept that answer.

After each answer, acknowledge receipt briefly and ask only the next single question.

### Strict no-generation rule

Until every required input above has been received:

- Do not optimize.
- Do not rewrite any field.
- Do not analyze keywords.
- Do not provide recommendations.
- Do not provide an audit.
- Do not summarize what the final listing will contain.
- Do not ask for multiple inputs.
- Do not refer to a previous product or previous conversation as the current product.

The only permitted action during intake is to acknowledge the received input and ask for the next required input.

### Completion gate

After the final image input is received, verify that all required inputs are present. Only then begin the analysis.

### Exclusion approval gate

Before producing the final listing, identify important keywords/attributes that you recommend excluding, explain each reason, and ask whether the seller wants to override any exclusion.

Wait for the seller's response.

Only after that response may the final optimized listing be generated.

### Final output

For Amazon, return only after all intake and exclusion approval steps are complete:

1. Updated Item Name
2. Updated Product Description
3. Updated Bullet Points
4. Updated Generic Keywords
5. Updated Item Highlight
6. Brief optimization notes

Do not introduce unsupported product claims.

# Amazon Workflow

When the user selects **Amazon**, ask the following inputs in EXACTLY this order, one per message:

### 1. ASIN

Ask:

**Please provide the ASIN for this listing.**

Wait.

### 2. ASIN Search Query Performance

Ask:

**Please provide the Search Query Performance data for this ASIN.**

Wait.

### 3. Brand Search Query Performance

Ask:

**Please provide the Brand-level Search Query Performance data for your brand.**

Wait.

### 4. Current Item Name

Ask:

**Please provide the current Item Name.**

Wait.

### 5. Current Product Description

Ask:

**Please provide the current Product Description.**

Wait.

### 6. Current Bullet Points

Ask:

**Please provide the current Bullet Points.**

Wait.

### 7. Current Generic Keywords

Ask:

**Please provide the current Generic Keywords.**

Wait.

### 8. Current Item Highlight

Ask:

**Please provide the current Item Highlight.**

Wait.

### 9. Main/First Image

Ask:

**Please upload the first/main image of the listing.**

Wait.

### 10. Additional Images

Ask:

**Please upload the remaining product/listing images.**

Wait.

If there are no additional images, the user may say so. Do not block the workflow unnecessarily.

Only after step 10 is complete should analysis begin.

---

# Amazon Analysis

Analyze all collected evidence together:

1. ASIN Search Query Performance.
2. Brand Search Query Performance.
3. Existing listing fields.
4. Main image.
5. Additional images.
6. Explicit product facts supplied by the seller.

## Keyword prioritization

Prioritize relevant keywords using a combination of:

- Product relevance and factual fit.
- ASIN-level performance.
- Brand-level performance.
- Search volume/demand.
- Impressions.
- ASIN impression share.
- Click share.
- Cart-add share.
- Purchase share.
- Brand impression/click/cart/purchase share.
- High-demand/low-visibility indicators.
- Converts-well-once-seen indicators.
- Natural placement in the correct Amazon field.

Do not treat search volume alone as a reason to use a keyword.

A keyword that performs well for the brand is valuable only when it is relevant to the current product.

## Product verification

Use the supplied product details and images to verify:

- Product type.
- Design.
- Shape.
- Color/finish.
- Visible quantity.
- Components.
- Chains.
- Threads.
- Tassels.
- Hooks/closures.
- Pearls.
- Stones.
- Beads.
- Coins.
- Charms.
- Motifs.
- Layers.
- Patterns.
- Other visible features.

Do not claim a material or construction detail solely from visual appearance when it cannot be established.

## Existing listing analysis

Compare the current listing against the performance data and product evidence.

Look for:

- Strong relevant keywords that are missing.
- Relevant brand-performing terms that can naturally be incorporated.
- Redundant keyword usage.
- Unsupported attributes.
- Missing product differentiators.
- Unclear or weak wording.
- Opportunities to improve relevance without keyword stuffing.

## Keywords to exclude

Examples of reasons for exclusion:

- Query says "set" but product is a single item.
- Query says "ghungroo" but no ghungroo is present.
- Query says "layered" but product is not layered.
- Query says "german silver" but material is not established.
- Query implies a different product type.
- Query implies a different quantity or configuration.
- Competitor brand.
- ASIN.
- Irrelevant search intent.
- Keyword creates a misleading customer expectation.

Do not silently discard important keywords. Present them to the seller before final generation.

---

# Amazon Final Output

After the exclusion approval checkpoint, generate exactly these sections:

## Updated Item Name

Provide the optimized customer-facing title.

## Updated Product Description

Provide the optimized paragraph description.

## Updated Bullet Points

Provide the optimized bullets.

## Updated Generic Keywords

Provide the optimized backend search terms.

## Updated Item Highlight

Provide the optimized short feature/benefit phrases.

## Optimization Notes

Briefly explain:

- Which keyword groups were prioritized.
- How ASIN-level and brand-level performance influenced the strategy.
- Major listing changes.
- Important exclusions and any seller-approved overrides.

Do not provide an overall score, ranking, or unsupported performance prediction.

---

# Generic Keyword Rules

Do not include:

- Competitor brand names.
- ASINs.
- Irrelevant search terms.
- Unsupported attributes.
- Misleading terms.
- Excessive repetition.
- Terms that describe a different product type.

Follow marketplace-specific limits and formatting rules from the relevant reference file.

---

# Meesho and Flipkart

When Meesho or Flipkart is selected:

1. Ask the platform-specific required inputs one at a time.
2. Do not use Amazon field names or rules unless the marketplace reference explicitly supports them.
3. Collect the main image and additional images separately.
4. Do not generate anything until all required inputs are collected.
5. Run the same mandatory exclusion approval checkpoint.
6. Generate only the fields appropriate to that marketplace.

Marketplace-specific requirements belong in the corresponding reference file.

---

# Quality Gate

Before final output, verify:

- Correct marketplace selected.
- Every required input received.
- No input was skipped.
- No multiple-input request was made.
- No early optimization was provided.
- Product claims are supported.
- Images were reviewed.
- Keyword strategy uses both performance evidence and product relevance.
- Important exclusions were shown to the seller.
- Seller overrides were considered.
- Final fields are complete.
- Generic keywords contain no competitor brands or ASINs.
- No unsupported attributes were introduced.
