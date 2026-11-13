# design-loop

**A universal, evidence-based design loop for AI coding agents.**

`design-loop` is an agent skill that turns any AI coding agent into a real designer-engineer. Instead of generating code and calling it done, the agent inspects the actual running application, captures real browser evidence, evaluates visual and functional quality, identifies the highest-impact problem, fixes it, verifies the result, and iterates — until the product reaches an explicit quality target.

Designed primarily for **web** work: websites, landing pages, web apps, marketing pages, presentation slides rendered in browsers, component libraries, design systems, dashboards, and any visual product that runs in a browser.

---

## Why this exists

AI agents are good at writing code. They are bad at knowing whether the result actually looks and works well.

The standard agent pattern is:

```
User asks → Agent generates code → Agent says "done"
```

`design-loop` replaces that with:

```
Understand → Inspect → Plan → Implement → Run → Browse
→ Capture → Evaluate → Prioritize → Fix → Verify
→ Regression Check → Accept or Iterate
```

The agent must look at the real running product, compare it against a quality bar, and prove improvement before accepting an iteration.

---

## What it covers

| Domain | Supported |
|---|---|
| Websites & Landing Pages | ✅ |
| Web Apps & Dashboards | ✅ |
| Marketing & Promo Pages | ✅ |
| Browser-rendered Slides | ✅ |
| Design Systems & Components | ✅ |
| E-commerce Frontends | ✅ |
| 2D Animated Websites | ✅ |
| 3D WebGL Websites | ✅ |
| Mobile Apps | ❌ (use a native mobile skill) |
| Backend / APIs | ❌ (use a backend skill) |

---

## File Map

```
design-loop/
├── SKILL.md                  ← Entry point. Load this first.
├── WORKFLOW.md               ← Full step-by-step execution order
├── MODES.md                  ← CREATE / REBUILD / REFINE / FIX / AUDIT / RESUME
├── DESIGN_CONSTITUTION.md    ← Visual language template for every project
├── REQUIREMENTS.md           ← Functional + UX + visual + technical requirements
├── AGENCY_QUALITY_STANDARD.md← The quality bar the agent must reach
├── GAUNTLET_PROTOCOL.md      ← Adversarial quality-control engine
├── CRITIC_PROTOCOL.md        ← Independent critique instructions
├── COUNCIL_PROTOCOL.md       ← Multi-perspective design decisions
├── RESEARCH_PROTOCOL.md      ← How to research references and competitors
├── DECOMPOSITION_PROTOCOL.md ← How to break work into parallel-safe units
├── GRAPHIFY_PROTOCOL.md      ← Knowledge graph sync after accepted changes
├── DECISIONS.md              ← Persistent record of design decisions
├── PROGRESS.md               ← Iteration progress log
├── ISSUES.json               ← Structured issue tracker (P0–P3)
├── STATE.json                ← Current project phase and iteration state
├── SESSION.json              ← Per-session context
├── DESIGN_RUBRIC.json        ← Scoring rubric for visual evaluation
├── QUALITY_BAR.json          ← Configured quality target
├── REFERENCE_ATLAS.json      ← Reference website registry
├── SECTION_LIBRARY.json      ← Section-level design pattern library
└── SKILL_REGISTRY.json       ← Available specialist skills registry
```

---

## How to Install

### Option 1 — Drop into any project

Copy the entire `design-loop/` folder into your project root or into a skills/agents configuration directory your agent supports.

```bash
# Example: clone this repo into your project's .agents folder
git clone https://github.com/your-username/design-loop .agents/design-loop
```

### Option 2 — Global agent skills directory

If your AI coding environment supports a global skills directory (e.g. `~/.gemini/config/skills/`), place `design-loop/` there so it is available across all projects.

```bash
git clone https://github.com/your-username/design-loop ~/.gemini/config/skills/design-loop
```

### Option 3 — Copy manually

Download or copy the folder and place it wherever your agent looks for skill files. No build step, no dependencies — these are plain Markdown and JSON files.

---

## How to Use

### Basic invocation

Tell your agent to load and use the design loop. Most agents supporting SKILL.md-based skills will activate on a direct instruction:

```
Use design-loop to build a landing page for [product].
```

```
Load design-loop and rebuild the UI of this website.
```

```
Run a design audit on the current application using design-loop.
```

### Modes

| Mode | When to use | Example prompt |
|---|---|---|
| **CREATE** | Building something new from scratch | `"Build me a portfolio website."` |
| **REBUILD** | Existing product needs a new visual direction | `"I hate the current design. Rebuild the UI."` |
| **REFINE** | Polish / hierarchy / spacing / premium improvements | `"Make the hero more premium."` |
| **FIX** | Something is visually broken or not working | `"The navbar breaks on mobile."` |
| **AUDIT** | Score and identify problems without changing code | `"Tell me what's wrong with this design."` |
| **RESEARCH** | Competitive analysis and reference gathering | `"Find design references for this product."` |
| **RESUME** | Continue after a session was interrupted | `"Continue where you stopped."` |

---

## How to Use in AI Agents & Identity Harnesses

### Claude Code

Place `design-loop/` in your project root or reference it via `CLAUDE.md`:

```markdown
# CLAUDE.md

## Skills
- design-loop: available at ./design-loop/SKILL.md
  Load this skill when the user asks to build, rebuild, refine, fix, audit,
  or visually improve any web product.
```

Then invoke:

```
Use the design-loop skill to create a premium SaaS landing page.
```

---

### Gemini / Antigravity (.agents/ or global skills)

Place `design-loop/` inside your `.agents/skills/` directory or your global `~/.gemini/config/skills/` directory.

The agent will discover it automatically and activate it when the task matches.

For explicit invocation in a system prompt or agent config:

```markdown
## Available Skills
- design-loop (./design-loop/SKILL.md): Use when building, rebuilding,
  refining, or auditing any website or web application.
```

---

### Custom Agent Harness (any LLM)

Inject the skill into your system prompt or agent context:

```python
import pathlib

skill_text = pathlib.Path("design-loop/SKILL.md").read_text()
workflow_text = pathlib.Path("design-loop/WORKFLOW.md").read_text()

system_prompt = f"""
You are a senior design-engineer agent.

You have access to the Universal Design Loop skill. Follow its instructions
precisely when designing or improving web products.

--- SKILL ---
{skill_text}

--- WORKFLOW ---
{workflow_text}
"""
```

At runtime, the agent will load additional protocol files (GAUNTLET_PROTOCOL.md,
DESIGN_CONSTITUTION.md, etc.) as the task progresses.

---

### MCP / Tool-calling Agents

Expose a `read_file` tool to the agent and instruct it to load the skill files in sequence.
The WORKFLOW.md defines the exact load order. Example tool description:

```json
{
  "name": "read_design_loop_file",
  "description": "Read a file from the design-loop skill directory.",
  "parameters": {
    "filename": { "type": "string" }
  }
}
```

---

## Full Example — Premium SaaS Landing Page

**User prompt:**

> Build me a premium SaaS landing page for a project management tool called "Stackflow". Dark theme. Research competitors first.

**What the agent does with design-loop active:**

1. **INITIALIZE** — Reads `SKILL.md`, `DESIGN_CONSTITUTION.md`, `STATE.json`, `REQUIREMENTS.md`
2. **DETECT MODE** → `CREATE`
3. **RESEARCH** — Opens competitor sites (Linear, Notion, Height, Asana), scores them section by section using `DESIGN_RUBRIC.json`, records the strongest patterns in `REFERENCE_ATLAS.json`
4. **DESIGN SYNTHESIS** — Selects the strongest hero pattern, the strongest feature showcase, the strongest CTA. Updates `DESIGN_CONSTITUTION.md` with Stackflow's specific visual language: dark slate, accent violet, editorial typography (Syne + DM Sans), asymmetric composition
5. **COUNCIL REVIEW** — Invokes Council to challenge the direction: "Does this risk looking like a generic SaaS site?"
6. **DECOMPOSE** — Splits sections into independent work units: hero, nav, feature grid, pricing, testimonials, footer
7. **IMPLEMENT** — Builds the page, following the constitution
8. **BROWSER VERIFY** — Opens the running app, checks at 1440px / 768px / 390px, inspects console for errors, captures screenshots
9. **GAUNTLET** — Independent critic compares current hero against the Linear.app hero. Finds: "Heading hierarchy is weak. Value proposition unclear." → P1 issue created
10. **FIX** — Increases heading scale, rewrites headline to lead with outcome, improves hero spacing
11. **REGRESSION CHECK** — Verifies the fix didn't break mobile
12. **REPEAT** — Next largest gap: feature grid is too generic. Switches to an editorial asymmetric layout
13. **SCORE** — Visual: 93 / UX: 91 / Responsive: 90 / Technical: 97 / Overall: 92.6
14. **ITERATE** — One more pass to push over 95
15. **FINALIZE** — Updates `STATE.json`, `PROGRESS.md`, runs Graphify sync

**Result:** A dark, editorial, non-generic SaaS landing page that has been browser-verified at three viewports, evaluated by an independent critic, and scored against a quality bar — not just code that was written and assumed to be good.

---

## Quality System

### Issue Priority

| Level | Meaning | Examples |
|---|---|---|
| **P0** | Critical — product is broken | Page doesn't load, runtime crash |
| **P1** | Major — significant problem | Broken mobile layout, weak hero hierarchy |
| **P2** | Moderate | Inconsistent spacing, typography mismatch |
| **P3** | Polish | Minor alignment, subtle refinement |

### Scoring

```
Visual Quality:      30%
UX:                  20%
Responsive Quality:  15%
Technical Quality:   15%
Performance:         10%
Accessibility:       10%
```

**Default target: 95 / 100**

The loop runs until the target is reached or the user explicitly stops it.

### Gauntlet

The Gauntlet Quality Engine is the adversarial layer. After every major milestone:

- A **fresh critic** (new context, no builder bias) evaluates the output
- The result is compared A/B against the strongest reference
- The **largest remaining gap** is identified
- The gap is fixed
- Repeat until no material gaps remain

This prevents the builder from grading its own work.

---

## Supported Agent Platforms

Tested and documented for use with:

- **Claude Code** (Anthropic)
- **Antigravity** (Google)
- **Gemini CLI** (Google)
- **Codex** (OpenAI)
- **Cursor / Windsurf** (via system prompt injection)
- Any LLM agent with file read access and browser/terminal tools

The skill is platform-independent. The agent uses whatever tools are available (file operations, browser, terminal, screenshots).

---

## Tips

- **Always let the agent read `DESIGN_CONSTITUTION.md` before implementing.** It prevents design drift across long sessions.
- **Use RESUME mode** after context limits or session interruptions. The agent picks up exactly where it left off.
- **Reference websites speed up research significantly.** Give the agent 2–3 URLs of sites you like and it will extract patterns immediately.
- **The Gauntlet works best with a real quality bar.** Instead of asking for "a nice website," give a competitor URL and say "I want to match or beat this."
- **P0 and P1 issues block acceptance.** The agent will not mark the project complete while high-severity issues remain unresolved.

---

## Contributing

PRs are welcome. This is a plain-text skill — no build pipeline, no dependencies.

If you add a new protocol file, register it in `SKILL.md` under the appropriate section so agents discover it.

If you improve an existing protocol, keep the section-numbered structure so agents can reference specific rules by number.

---

## License

MIT — see [LICENSE](./LICENSE)

---

*Built for web. Verified in the browser. Improved through evidence.*
