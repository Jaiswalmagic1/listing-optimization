# Listing Optimization

An AI-powered, marketplace-aware skill for optimizing e-commerce product listings using search-performance data, existing listing content, and product images.

**Repository:** https://github.com/Jaiswalmagic1/listing-optimization

The project is designed around the **Agent Skills** format so the same core skill can be used across compatible AI agents, with platform-specific installation instructions for **ChatGPT, Gemini, and Claude**.

## What It Does

**Listing Optimization** collects the information needed to understand a product and its marketplace search performance, then produces an optimized listing for the selected marketplace.

The workflow is intentionally controlled:

1. Select the marketplace.
2. Collect the SKU, when available, for chat identification.
3. Collect required listing and performance data one question at a time.
4. Analyze the product images.
5. Analyze marketplace search-query performance.
6. Identify relevant keywords and attributes.
7. Identify keywords or attributes that should be excluded.
8. Ask the seller to review important exclusions and provide overrides.
9. Generate the final optimized listing only after the required information and exclusion review are complete.

The skill does **not** optimize during intake and does not invent product facts.

## Cross-LLM / Agent Skills Design

The skill uses a `SKILL.md` plus optional reference files. Agent Skills are an open standard designed to package reusable instructions, workflows, scripts, and resources for AI agents.

The repository keeps the marketplace workflow in:

```text
skills/listing-optimization/
├── SKILL.md
└── references/
    ├── amazon.md
    ├── meesho.md
    ├── flipkart.md
    └── README.md
```

The repository also contains an interoperable `.agents/skills/` copy for agent environments that discover skills from that location.

**GitHub is the source of truth.** The downloadable release ZIP is generated from the canonical `skills/listing-optimization/` directory.

## Using the Skill with ChatGPT

ChatGPT supports reusable Skills for eligible workspaces/products. OpenAI documents Skill installation through **Plugins → Skills → Create → Upload from your computer** where Skills are available.

Official documentation:
https://help.openai.com/en/articles/20001066-skills-in-chatgpt

### Installation

1. Download the latest release:
   https://github.com/Jaiswalmagic1/listing-optimization/releases/latest/download/listing-optimization.zip
2. In ChatGPT, open **Plugins**.
3. Open the **Skills** tab.
4. Select **Create → Upload from your computer**.
5. Upload the downloaded ZIP.
6. Install/enable the skill.
7. Start a new chat and use the skill for a marketplace listing.

The exact ChatGPT UI and eligibility can vary by account, workspace, and product surface.

### Expected behavior

When the skill is active, a new listing-optimization run starts with:

> Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?

The workflow then proceeds one question at a time.

For Amazon, the current order is:

1. Platform
2. SKU
3. ASIN
4. ASIN-level Search Query Performance
5. Brand-level Search Query Performance
6. Item Name
7. Item Highlight
8. Occasion
9. Product Description
10. Bullet Points
11. Generic Keywords
12. Set Name
13. Holiday Type
14. Pendant Description, when applicable
15. Main/first image
16. Additional images

The final output is not generated until the required intake is complete and the seller has reviewed the proposed keyword/attribute exclusions.

## Using the Skill with Gemini

### Gemini CLI

Gemini CLI supports Agent Skills and discovers skills from locations including `.agents/skills/` and `.gemini/skills/`.

Official documentation:
https://github.com/google-gemini/gemini-cli/blob/main/docs/cli/using-agent-skills.md

You can install the skill directly from this repository:

```bash
gemini skills install https://github.com/Jaiswalmagic1/listing-optimization.git --path skills/listing-optimization
```

Then verify it:

```bash
gemini skills list
```

Inside a Gemini CLI session, you can also use:

```text
/skills list
```

If the skill was added or changed locally, reload skills with:

```text
/skills reload
```

Gemini CLI also supports the interoperable `.agents/skills/` location.

### Gemini Apps / Gemini web surfaces

Where the Gemini product surface provides custom Skill/Agent Skill upload or import, use the packaged `SKILL.md` skill directory or compatible ZIP package.

Because Gemini product surfaces can differ from Gemini CLI, use the current Google/Gemini UI instructions for the account you are using.

**Important:** Gemini CLI and Gemini web/app interfaces are separate environments. A skill installed in Gemini CLI does not automatically mean it is installed in the Gemini web application.

## Using the Skill with Claude

Claude supports the Agent Skills format across Claude apps, Claude Code, and the Claude API.

Official documentation:
https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview

### Claude.ai

Where custom Skills are available:

1. Download the latest release ZIP.
2. Open Claude's Skill settings/features area.
3. Upload the Skill ZIP.
4. Enable/use the Skill.
5. Start a new conversation and request marketplace listing optimization.

Claude's available Skill features and plan requirements can change, so follow the current Claude UI documentation for the account being used.

### Claude Code

Claude Code supports custom Skills as filesystem-based directories.

For a project-local installation, the expected structure is:

```text
your-project/
└── .claude/
    └── skills/
        └── listing-optimization/
            ├── SKILL.md
            └── references/
                ├── amazon.md
                ├── meesho.md
                └── flipkart.md
```

You can copy the contents of `skills/listing-optimization/` from this repository into that directory.

For a personal/user-level installation, place the skill under:

```text
~/.claude/skills/listing-optimization/
```

Claude Code can then discover the Skill and use it when the task matches, or it can be invoked directly when supported.

Claude's official announcement describes Skills as portable across Claude apps, Claude Code, and the API:
https://claude.com/blog/skills

## Portable Installation Summary

| AI platform | Recommended method | Source |
|---|---|---|
| ChatGPT | Upload the latest Skill ZIP through Skills | GitHub release ZIP |
| Gemini CLI | `gemini skills install` from GitHub | GitHub repository |
| Gemini web/app | Use the Skill/Agent Skill upload/import available in that product surface | GitHub release ZIP |
| Claude.ai | Upload the Skill ZIP where custom Skills are available | GitHub release ZIP |
| Claude Code | Copy/link the Skill into `.claude/skills/` | GitHub repository |
| Other Agent Skills-compatible agents | Use the `skills/listing-optimization/` directory or compatible package format | GitHub repository |

Not every AI product exposes the same installation UI. The **SKILL.md + references** are the portable core; installation is platform-specific.

## Amazon Optimization Methodology

Amazon optimization uses multiple sources of information rather than relying only on keyword volume.

### ASIN Search Query Performance

The skill can analyze:

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

### Brand Search Query Performance

Brand-level search performance is used to identify relevant search terms where the seller's brand already receives meaningful visibility, clicks, carts, or purchases.

Brand-level performance is **not** used blindly. A keyword must still be factually relevant to the product.

### Existing Listing

The current listing fields are reviewed before creating replacements.

### Product Images

Images are used as evidence for clearly visible characteristics such as:

* Design
* Shape
* Color/finish
* Visible components
* Patterns
* Closures
* Chains
* Threads
* Stones
* Pearls
* Layers
* Other visible characteristics

Appearance alone is not treated as definitive proof of material/composition.

## Image Recommendation Rule

The skill does **not** recommend changing product images just to make the listing look different.

An image change is suggested only when there is a specific evidence-based reason, such as:

* A clear marketplace requirement or compliance issue.
* An objectively identifiable product-presentation problem.
* Relevant performance data supporting an image-related hypothesis, such as weak click-through relative to relevant search exposure.

The skill must distinguish **observed facts** from **hypotheses**.

If the existing images satisfy the requirements and there is no meaningful evidence that an image change is needed, the correct recommendation is:

> Keep the existing images unchanged.

This rule is intentionally strict to prevent random or speculative image recommendations.

## Keyword Strategy

The skill prioritizes keywords using:

* Search demand
* ASIN-level performance
* Brand-level performance
* Impressions
* Click/cart/purchase signals
* Product relevance
* Existing listing coverage
* Product-image verification
* Marketplace-specific rules

High search volume alone does not automatically make a keyword suitable.

Terms such as `ghungroo`, `layered`, `german silver`, or `set` should not be used merely because they have search volume. The product must support the corresponding attribute.

## Keyword Exclusion Review

Before generating the final listing, the skill identifies important keywords or attributes that should be excluded.

Reasons may include:

* Product mismatch
* Unsupported attribute
* Unconfirmed material
* Different product type
* Different quantity/configuration
* Competitor brand or ASIN
* Misleading product expectation
* Unnecessary duplication

The seller is explicitly asked whether any exclusion should be overridden.

The final listing is generated only after this review.

## Amazon Field Rules

Current Amazon-specific rules include:

* **Item Name:** maximum 75 characters.
* **Item Highlight:** one field, maximum 125 characters.
* **Occasion:** specific event or celebration for which the jewelry item is designed or appropriate to wear.
* **Product Description:** marketplace-specific description.
* **Bullet Points:** marketplace-specific feature/value bullets.
* **Generic Keywords:** relevant search terms without competitor brands, ASINs, or unsupported claims.
* **Set Name:** use the manufacturer's official name when supplied; otherwise describe the factual set type and number of components. Never invent an official manufacturer name.
* **Holiday Type:** holiday/holidays the item is intended for or associated with; holidays are culturally recognized collective celebrations.
* **Pendant Description:** maximum 100 characters when applicable.

## Supported Marketplaces

### Amazon

Detailed workflow currently supported.

### Meesho

Marketplace-specific structure is present and can be expanded with verified marketplace rules.

### Flipkart

Marketplace-specific structure is present and can be expanded with verified marketplace rules.

Do not assume or invent marketplace rules. New rules should be verified before being added to the corresponding reference file.

## Design Principles

### Accuracy over keyword stuffing

Keywords should describe the actual product.

### Search performance over assumptions

Available marketplace search data should be used whenever possible.

### Relevance over raw volume

A lower-volume keyword that closely matches the product may be more useful than a high-volume keyword describing a different product.

### Images are evidence

Images can verify visible characteristics but should not be used to invent material/composition claims.

### Seller remains in control

The skill identifies recommendations and exclusions, but the seller reviews important exclusions before final output.

## Repository Structure

```text
listing-optimization/
├── skills/
│   └── listing-optimization/
│       ├── SKILL.md
│       └── references/
│           ├── amazon.md
│           ├── meesho.md
│           ├── flipkart.md
│           └── README.md
├── .agents/
│   └── skills/
│       └── listing-optimization/
│           ├── SKILL.md
│           └── references/
├── .github/
│   └── workflows/
│       └── publish-latest-skill.yml
├── LICENSE
└── README.md
```

## Extending the Skill

A new marketplace should generally contain:

* Marketplace-specific fields
* Title rules
* Description rules
* Bullet/feature rules
* Search-term rules
* Character limits
* Restricted terminology
* Required attributes
* Image requirements
* Output format

Keep marketplace-specific rules in the relevant reference file.

## Contributing

Marketplace rules and search behavior change over time.

Contributions that improve marketplace-specific rules, keyword analysis, listing quality checks, product attribute validation, search-performance interpretation, or evidence-based image verification are welcome.

When adding marketplace rules, verify them against current marketplace documentation or reliable marketplace evidence before committing them.

## License

This project is released under the **MIT License**.

The MIT License permits reuse, modification, distribution, and commercial use, subject to the conditions in the LICENSE file.

The license applies to the repository's original code, documentation, and skill materials unless a file states otherwise.

Third-party trademarks, marketplace names, logos, and platform documentation remain the property of their respective owners.

## Download the Latest Skill

The repository automatically publishes the latest portable skill whenever the `main` branch is updated.

**Latest ZIP:**
https://github.com/Jaiswalmagic1/listing-optimization/releases/latest/download/listing-optimization.zip

After future updates, download the latest release rather than using an older ZIP.

## Testing the Skill

Use a **fresh conversation/session** when testing so previous instructions do not affect the result.

### Basic test

Start with:

> Optimize a listing for me.

Expected first response:

> Which platform is this listing for — Amazon, Meesho, Flipkart, or Other?

### Amazon test

After selecting Amazon, the skill should ask for the SKU first, then continue one input at a time.

It should **not**:

* Produce listing copy during intake.
* Ask for all remaining inputs in one message.
* Invent product facts.
* Add keywords solely because they have high search volume.
* Recommend changing images without evidence.
* Skip the exclusion-review checkpoint.

### Final-stage test

Before final listing output, verify that the skill:

1. Shows important proposed exclusions and reasons.
2. Asks:
   **Do you want to override any of these exclusions?**
3. Waits for the seller's response.
4. Generates the final listing only after the response.

## Versioning

Use Git history and GitHub releases to track changes.

When marketplace rules change, update the relevant reference file and test the workflow before publishing a new release.

---

**Current primary marketplace:** Amazon

**Planned expansion:** Meesho, Flipkart, and additional marketplaces
