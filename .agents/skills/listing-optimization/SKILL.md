---
name: listing-optimization
description: Optimize e-commerce marketplace listings using marketplace-specific rules, search performance data, existing listing content, and product images. Ask for the marketplace first, collect required inputs one question at a time, do not generate final copy until all required inputs are received, and review proposed keyword exclusions with the seller before final output.
---

# Listing Optimization

## Mission

Produce accurate, marketplace-specific listing optimization based on the actual product, available search-performance evidence, existing listing content, and product images.

The seller remains in control. The skill should explain important exclusions before final generation and allow the seller to override them.

## Mandatory conversation workflow

### Rule 1: Ask platform first

At the beginning of every new optimization run, ask exactly one question:

> Which platform is this listing for? (Amazon, Meesho, Flipkart, or Other)

Do not request ASIN, listing fields, keywords, or images until the platform is known.

### Rule 2: One question at a time

Ask for only one information item at a time. Wait for the user's answer before asking for the next item.

Do not provide a checklist of all required inputs in one message.

### Rule 3: No premature optimization

Do not draft, rewrite, rank keywords, or provide final listing content while required inputs are still missing.

You may acknowledge receipt of information, but do not start the optimization output.

### Rule 4: Do not invent missing facts

Never assume a material, size, quantity, closure, set composition, feature, certification, or other product attribute from a keyword alone.

Use explicit user-provided information and visible image evidence. Clearly distinguish what is visible, stated, inferred, and unknown.

## Amazon input sequence

After the user selects Amazon, request these inputs in order, one at a time:

1. ASIN.
2. ASIN-level Search Query Performance data.
3. Brand-level Search Query Performance data.
4. Current Item Name.
5. Current Product Description.
6. Current Bullet Points.
7. Current Generic Keywords.
8. Current Item Highlight.
9. Main/first listing image.
10. Other listing/product images.

If a later input is absent or unusable, request that specific input and do not proceed to final optimization.

## Amazon analysis

Use the Amazon reference file for detailed marketplace rules.

Analyze:

- ASIN Search Query Performance.
- Brand Search Query Performance.
- Existing listing content.
- Main and secondary images.
- Product facts explicitly supplied by the seller.
- Search demand and performance signals.
- Keyword relevance and semantic fit.
- Existing listing coverage and repetition.

Prioritize keywords using a combination of relevance, search demand, ASIN performance, brand performance, and verified product fit. Do not treat high volume as sufficient evidence of suitability.

### Keyword signals

Consider, when available:

- Search Query.
- Search Query Score.
- Search Query Volume.
- Impressions.
- ASIN impression share.
- Click share.
- Cart-add share.
- Purchase share.
- Brand impression share.
- Brand click share.
- Brand cart-add share.
- Brand purchase share.
- Explicit opportunity flags such as high-demand/low-visibility or good-conversion signals.

Do not fabricate missing metrics.

## Image analysis

Review the first/main image and other listing images to verify or identify visible attributes, such as:

- Product type.
- Shape and design.
- Color/finish.
- Number of visible components.
- Chains, threads, tassels, hooks, clasps, or other closures.
- Pearls, stones, beads, coins, charms, or motifs.
- Layers.
- Pattern.
- Relative size where the image supports it.

Images are evidence, but image appearance alone should not be treated as definitive proof of composition or material when the claim requires information not visible in the image.

## Exclusion review: mandatory checkpoint

Before generating final listing content, identify meaningful keywords or attributes that you intend to exclude.

For every proposed exclusion, provide:

- Keyword/term.
- Reason for exclusion.
- Whether the concern is product mismatch, unverified attribute, misleading implication, duplication, or another concrete reason.

Then ask the seller whether they want to override any exclusion.

Example:

> Proposed exclusions:
> - german silver — material not confirmed.
> - ghungroo — no visible ghungroo feature.
> - choker set — product appears to be a single item.
>
> Do you want to use any of these despite the recommendation?

Do not generate the final optimized listing until the seller has had an opportunity to respond to this checkpoint.

If the seller overrides an exclusion, use it only where it can be incorporated without making a false product claim, unless the seller also provides the missing fact that establishes the attribute.

## Final Amazon output

After all inputs are received and the exclusion checkpoint is resolved, return:

1. **Updated Item Name**
2. **Updated Product Description**
3. **Updated Bullet Points**
4. **Updated Generic Keywords**
5. **Updated Item Highlight**

Also include a compact rationale covering the main keyword strategy and important changes.

Do not produce prohibited or unsupported product claims.

## Generic keyword handling

Generic keywords should contain relevant customer-search terms without unnecessary repetition.

Do not use:

- Competitor brand names.
- ASINs.
- Irrelevant keywords.
- Unsupported product attributes.
- Repetitive variants solely to inflate term count.
- Misleading terms that imply a different product type, material, quantity, or configuration.

Marketplace-specific search-term limits and formatting rules belong in the marketplace reference file.

## Extension to additional marketplaces

For Meesho, Flipkart, and future marketplaces:

1. Keep the same core rules for platform-first selection, one-question-at-a-time intake, no premature generation, factual verification, image review, and exclusion approval.
2. Use the marketplace-specific reference file for required inputs, fields, terminology, character limits, and other rules.
3. Never import Amazon-specific field rules into another marketplace unless the relevant reference explicitly says to do so.

## Quality gate before final output

Before finalizing, verify:

- All required inputs were received.
- The selected marketplace is correct.
- Product claims match supplied facts and images.
- Important exclusions were presented to the seller.
- Any seller overrides were respected where factually supportable.
- Keywords are relevant and naturally integrated.
- Required output fields are all present.
- No competitor brand names or ASINs appear in generic keywords.
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

## Amazon analysis

Use the Amazon reference file for detailed marketplace rules.

Analyze:

- ASIN Search Query Performance.
- Brand Search Query Performance.
- Existing listing content.
- Main and secondary images.
- Product facts explicitly supplied by the seller.
- Search demand and performance signals.
- Keyword relevance and semantic fit.
- Existing listing coverage and repetition.

Prioritize keywords using a combination of relevance, search demand, ASIN performance, brand performance, and verified product fit. Do not treat high volume as sufficient evidence of suitability.

### Keyword signals

Consider, when available:

- Search Query.
- Search Query Score.
- Search Query Volume.
- Impressions.
- ASIN impression share.
- Click share.
- Cart-add share.
- Purchase share.
- Brand impression share.
- Brand click share.
- Brand cart-add share.
- Brand purchase share.
- Explicit opportunity flags such as high-demand/low-visibility or good-conversion signals.

Do not fabricate missing metrics.

## Image analysis

Review the first/main image and other listing images to verify or identify visible attributes, such as:

- Product type.
- Shape and design.
- Color/finish.
- Number of visible components.
- Chains, threads, tassels, hooks, clasps, or other closures.
- Pearls, stones, beads, coins, charms, or motifs.
- Layers.
- Pattern.
- Relative size where the image supports it.

Images are evidence, but image appearance alone should not be treated as definitive proof of composition or material when the claim requires information not visible in the image.

## Exclusion review: mandatory checkpoint

Before generating final listing content, identify meaningful keywords or attributes that you intend to exclude.

For every proposed exclusion, provide:

- Keyword/term.
- Reason for exclusion.
- Whether the concern is product mismatch, unverified attribute, misleading implication, duplication, or another concrete reason.

Then ask the seller whether they want to override any exclusion.

Example:

> Proposed exclusions:
> - german silver — material not confirmed.
> - ghungroo — no visible ghungroo feature.
> - choker set — product appears to be a single item.
>
> Do you want to use any of these despite the recommendation?

Do not generate the final optimized listing until the seller has had an opportunity to respond to this checkpoint.

If the seller overrides an exclusion, use it only where it can be incorporated without making a false product claim, unless the seller also provides the missing fact that establishes the attribute.

## Final Amazon output

After all inputs are received and the exclusion checkpoint is resolved, return:

1. **Updated Item Name**
2. **Updated Product Description**
3. **Updated Bullet Points**
4. **Updated Generic Keywords**
5. **Updated Item Highlight**

Also include a compact rationale covering the main keyword strategy and important changes.

Do not produce prohibited or unsupported product claims.

## Generic keyword handling

Generic keywords should contain relevant customer-search terms without unnecessary repetition.

Do not use:

- Competitor brand names.
- ASINs.
- Irrelevant keywords.
- Unsupported product attributes.
- Repetitive variants solely to inflate term count.
- Misleading terms that imply a different product type, material, quantity, or configuration.

Marketplace-specific search-term limits and formatting rules belong in the marketplace reference file.

## Extension to additional marketplaces

For Meesho, Flipkart, and future marketplaces:

1. Keep the same core rules for platform-first selection, one-question-at-a-time intake, no premature generation, factual verification, image review, and exclusion approval.
2. Use the marketplace-specific reference file for required inputs, fields, terminology, character limits, and other rules.
3. Never import Amazon-specific field rules into another marketplace unless the relevant reference explicitly says to do so.

## Quality gate before final output

Before finalizing, verify:

- All required inputs were received.
- The selected marketplace is correct.
- Product claims match supplied facts and images.
- Important exclusions were presented to the seller.
- Any seller overrides were respected where factually supportable.
- Keywords are relevant and naturally integrated.
- Required output fields are all present.
- No competitor brand names or ASINs appear in generic keywords.
- No unsupported attributes were introduced.
