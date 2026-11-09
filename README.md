# Reforge

**Give your coding agent a practical design process for better landing pages and mobile onboarding.**

Reforge is a reusable set of instructions for your AI coding agent. It helps the agent audit your existing UI, improve the design in your project, and check the result. It focuses on clear messaging, thoughtful layouts, readable typography, and usable interactions while preserving your brand by default.

[Quick start](#quick-start) · [Examples](#example-prompts) · [Before & after](#before-and-after) · [How it works](#how-it-works) · [FAQ](#faq) · [Contributing](#contributing)

## Quick start

### 1. Install in your project

From your project's terminal, run:

```bash
npx skills add gurshaan17/reforge --skill reforge
```

Choose your coding agent when prompted. You need Node.js and an agent supported by the [skills CLI](https://github.com/vercel-labs/skills).

### 2. Open your agent and give it a target

```text
/reforge redesign the landing page in src/app/page.tsx.
Make the product and primary action clearer, improve the layout on mobile,
and preserve our existing colors, fonts, logo, and images.
```

Replace the file path with your page or flow. You can also provide screenshots or a URL your agent can access. If your agent uses a different skill invocation syntax, use its equivalent of `/reforge`.

### 3. Review the result

The agent should explain what changed, why, and what it checked. When rendering tools are available, it should inspect desktop and mobile layouts and provide comparable before-and-after screenshots.

<details>
<summary><strong>More installation options</strong></summary>

Install across projects:

```bash
npx skills add gurshaan17/reforge --skill reforge -g
```

Preview the available skill before installing:

```bash
npx skills add gurshaan17/reforge --list
```

For manual installation, clone this repository and copy the entire `skills/reforge` folder into your agent's documented skills directory. Keep its `SKILL.md`, `agents/`, and `references/` together. Reload your agent's skill list if needed.

See the [skills.sh documentation](https://skills.sh/docs) for installation help and supported agents. Reforge needs no separate service or API key; it uses the tools available to your coding agent.

</details>

## When to use Reforge

| You want to… | Ask Reforge to… |
| --- | --- |
| Improve a landing page | Clarify the message, strengthen hierarchy, and improve composition. |
| Polish an existing design | Refine spacing, typography, imagery, and responsive layouts. |
| Improve mobile onboarding | Clarify each step, reduce confusion, and inspect recovery states. |
| Get feedback before changing code | Critique the page and provide recommendations only. |

Reforge works within your existing stack and components. Its focus is landing pages and onboarding; it does not provide a general backend development workflow.

## Example prompts

### Redesign a landing page

```text
/reforge audit and redesign the landing page in src/app/page.tsx.
Our audience is independent designers. The primary action is starting
a free trial. Keep our palette, fonts, logo, and product screenshots.
Implement the changes and check desktop and mobile layouts.
```

### Polish one page

```text
/reforge improve the pricing page's typography, spacing, and hierarchy.
Preserve the pricing, content, images, and checkout behavior.
Keep the scope to this page and use the existing components.
```

### Improve onboarding

```text
/reforge improve our mobile onboarding screens. The first useful outcome
is creating a workspace. Preserve navigation and business logic, clarify
each step, and check keyboard behavior and permission-denial states.
```

### Get a critique without code changes

```text
/reforge critique this landing page screenshot. Identify the highest-impact
improvements to message, hierarchy, typography, and composition.
Provide recommendations only. Do not change code.
```

**For better results, include:** the target page or files, who it is for, the action visitors should take, and any constraints. For example: “Keep the checkout flow unchanged” or “Only update the hero.”

## Before and after

A Metaverse landing-page redesign:

| Before | After |
| --- | --- |
| ![Before: dark Metaverse landing page with a virtual HQ headline and game screenshot](assets/metaverse-before.png) | ![After: light Metaverse landing page with expressive typography and an illustrated virtual workspace](assets/metaverse-after.png) |

[View full-size before](assets/metaverse-before.png) · [View full-size after](assets/metaverse-after.png)

This example changes the logo, palette, theme, and product imagery. Changes of this scope require explicit rebranding and asset-replacement authorization. **Reforge preserves your existing brand and imagery by default.**

## How it works

1. **Audit the existing UI.** Identify the audience, main action, strengths, and biggest obstacles.
2. **Set concrete targets.** Choose observable improvements, such as making a product screenshot readable on mobile or making the primary action easier to find.
3. **Implement the design.** Improve composition, typography, spacing, and image framing within the requested scope.
4. **Inspect and refine.** Check the rendered result and relevant interactions when tools permit. Fix specific problems and recheck the affected areas.
5. **Explain the result.** Summarize changes, design decisions, checks, and anything that could not be verified.

The agent reads supporting guidance when relevant:

| Guide | What it covers |
| --- | --- |
| [Composition](skills/reforge/references/composition.md) | Layout selection, section rhythm, image scale, and mobile reading order. |
| [Background treatments](skills/reforge/references/backgrounds.md) | Choosing among 22 treatments, combining effects, and keeping content readable when assets fail to load. |
| [Mobile onboarding](skills/reforge/references/onboarding.md) | Step purpose, required inputs, permissions, recovery, saved state, and keyboard behavior. |

## FAQ

### Will it change my branding?

It preserves existing colors, fonts, logos, imagery, and voice by default. Explicitly describe any rebranding or asset changes you want to authorize.

### Does it work with my framework?

The instructions are framework-independent. Your coding agent works with your existing architecture and tools; Reforge does not require a particular component library, browser plugin, or image generator.

### Will it change code or just give advice?

That depends on your request. Ask for a redesign to get implementation, or request a critique for recommendations only. You can also ask for alternative directions.

### What if my agent cannot open a browser?

It can work from accessible source files and supplied screenshots. It should state which visual, browser, or device checks it could not perform. A code review alone does not verify the rendered design.

### Does it publish my site?

Publishing or deployment requires a separate request.

### Does it guarantee better conversions?

No. Reforge guides design improvements; conversion and performance claims require measurements. Testimonials, metrics, pricing, and other factual content must come from supplied evidence.

### The skill is installed, but my agent cannot find it. What should I check?

Confirm that you installed it for the correct agent and project, then reload the agent's skill list or session. Use your agent's supported invocation syntax. For a manual installation, confirm that the complete `reforge` folder is in its documented skills location.

## Repository guide

```text
reforge/
├── README.md
├── assets/                     # README screenshots
└── skills/
    └── reforge/
        ├── SKILL.md             # Main agent instructions
        ├── agents/
        │   └── openai.yaml      # Interface metadata for compatible agents
        └── references/
            ├── backgrounds.md
            ├── composition.md
            └── onboarding.md
```

Start with [SKILL.md](skills/reforge/SKILL.md) to understand or modify the workflow. The complete installable skill lives under `skills/reforge/`; the repository's screenshot assets are for this README.

## Contributing

[Open an issue](https://github.com/gurshaan17/reforge/issues) to report a problem or suggest an improvement. Include your prompt, relevant context, expected behavior, and actual result. Remove private project data before sharing.

For a pull request:

- Edit the skill files under `skills/reforge/` and update usage documentation when needed.
- Keep valid `name` and `description` frontmatter in `SKILL.md`, and check that local reference links resolve.
- Explain the observed problem, your change, and how you evaluated it.

<details>
<summary><strong>How to evaluate a change to the skill</strong></summary>

Compare the previous and proposed versions on several different projects, such as a product landing page, a content-heavy page, and a mobile onboarding flow. Use the same prompt, starting assets, permissions, and available tools for each comparison. Keep generated results outside the skill package.

Compare task clarity, brand and image preservation, responsive composition, interaction correctness, and visual quality using screenshots and observed behavior. Record concrete failures and owner feedback. Distinguish a preference specific to one brand from a recurring problem before adding a new instruction.

Packaging checks confirm that the skill can be discovered and its references loaded. Real-project comparisons are needed to establish whether its design output improves.

</details>
