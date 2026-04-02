<p align="right">
  <a href="README-zh.md">中文</a> | <strong>English</strong>
</p>

<p align="center">
  <img src="assets/banner.svg" alt="metacog banner" width="100%">
</p>

<p align="center">
  <em>Upgrade AI from answer-generator to cognitive operating system</em>
</p>

---

## What is metacog?

**metacog** is a single Claude Code skill that packs 8 metacognitive capabilities into one `/metacog` command. Instead of just answering your questions, it helps you **think better about thinking itself**.

Most AI interactions follow: *User asks → AI answers*. The real bottleneck is rarely "what's the answer" — it's **"am I even asking the right question?"** metacog flips the script: it analyzes the thinking process itself.

<p align="center">
  <img src="assets/architecture.svg" alt="architecture" width="100%">
</p>

---

## Installation

```bash
# Personal (all your projects)
mkdir -p ~/.claude/skills/metacog
cp SKILL.md ~/.claude/skills/metacog/

# Or project-level (this project only)
mkdir -p .claude/skills/metacog
cp SKILL.md .claude/skills/metacog/
```

Restart Claude Code after installation.

---

## The 8 Skills

| Keyword | Skill | What it does | Theory |
|---------|-------|-------------|--------|
| `cognition` | Metacognition | Diagnoses thinking errors, biases, logic gaps | Flavell, Dunning-Kruger |
| `learning` | Meta-Learning | Designs learning paths, finds the critical 20% | Feynman, Pareto, Ericsson |
| `decision` | Meta-Decision | Analyzes trade-offs, runs pre-mortems | Kahneman, prospect theory |
| `structure` | Meta-Structure | Builds MECE logical skeletons | Minto Pyramid, McKinsey |
| `feedback` | Meta-Feedback | Traces behavior→mechanism→outcome chains | Nelson & Narens |
| `review` | Meta-Review | Extracts SOPs from past events via 5 Whys | Reflexion, Argyris |
| `emotion` | Meta-Emotion | Separates emotional signal from noise | Gottman, Gross, Slovic |
| `communication` | Meta-Communication | Decodes meta-messages, fixes intent-impact gaps | Bateson, Watzlawick, NVC |

---

## Usage

### Auto-routing — describe your situation naturally
```
/metacog I study 8 hours a day but my exam scores are terrible
→ Routing → learning
→ (identifies fluency illusion, designs active recall path)
```

### Explicit keyword — pick the skill yourself
```
/metacog decision Should I quit my job to start a business?
→ (decision principles, trade-off matrix, pre-mortem, fallback plan)
```

### All mode — multi-skill pipeline for complex problems
```
/metacog all I keep procrastinating and feel terrible about it
→ Runs emotion + cognition + feedback → Synthesizes insights
```

---

## Output Contract

Every skill output always includes these 5 guarantees:

<p align="center">
  <img src="assets/output-contract.svg" alt="output contract" width="100%">
</p>

---

## Theoretical Foundations

Every skill is grounded in peer-reviewed academic frameworks, not vibes.

<p align="center">
  <img src="assets/theory-map.svg" alt="theory map" width="100%">
</p>

<details>
<summary><strong>Nelson & Narens Monitor-Control (1990)</strong> — The operating backbone</summary>

Two cognitive levels interact:
- **Monitor**: meta-level observes the object-level (*"How am I doing?"*)
- **Control**: meta-level modifies the object-level (*"Switch strategy"*)

Every metacog skill follows this: first monitor the user's thinking, then provide control actions.
</details>

<details>
<summary><strong>Kahneman Dual Process (2011)</strong> — Why we need metacognition</summary>

- **System 1**: Fast, automatic, intuitive, error-prone
- **System 2**: Slow, deliberate, rational, energy-consuming

Metacognition = using System 2 to audit System 1.
</details>

<details>
<summary><strong>Gottman Meta-Emotion (1996)</strong> — Emotions about emotions</summary>

- **Emotion-Coaching**: recognize → name → understand
- **Emotion-Dismissing**: deny → suppress → avoid

The `emotion` skill implements the coaching approach: emotions as data, not noise.
</details>

<details>
<summary><strong>Argyris Double-Loop Learning (1978)</strong> — Question the model</summary>

- **Single-loop**: action failed → fix the action
- **Double-loop**: action failed → question the assumption → fix the mental model

The `review` skill asks not just "what went wrong" but "what belief was wrong."
</details>

---

## Design Decisions

| Decision | Why |
|----------|-----|
| **Single file** | Users remember one command: `/metacog`. Router handles complexity. |
| **Bilingual headers** | English for LLM precision; Chinese for intuitive understanding. |
| **Confidence 1-10** | Combats Dunning-Kruger for both AI and user. |
| **Anti-flattery** | Every output must survive: "Delete all compliments — what's left?" |
| **Reusable principles** | Each interaction extracts one transferable insight. |

### Skill Differentiation

| | cognition | emotion |
|---|---|---|
| Target | Thinking errors | Emotional distortion |
| Core Q | "Is my reasoning valid?" | "What am I feeling? How does it bend judgment?" |
| Anti-pattern | "You're right" (flattery) | "Don't overthink it" (denial) |

| | structure | communication |
|---|---|---|
| Target | Information architecture | Interpersonal dynamics |
| Core Q | "Is this organized clearly?" | "What is really being said?" |
| Anti-pattern | "Everything matters" (flat) | "Just be honest" (naive) |

---

## Anti-Patterns

These outputs are **explicitly forbidden**:

| Pattern | Bad | Good |
|---------|-----|------|
| Flattery | "Great question!" | Jump to analysis |
| Chicken soup | "Believe in yourself!" | Concrete steps |
| Hedging | "It depends" | List variables + conditionals |
| Emotion denial | "Don't overthink it" | Name the emotion, trace effects |
| Naive advice | "Just be honest" | Analyze dynamics, give phrasing |
| Flattening | "All equally important" | Priority ranking |
| Hallucination | Fabricating answers | State what's missing, ask |

---

## References

**Core**: Flavell (1979), Schraw & Dennison MAI (1994), Nelson & Narens (1990), Kahneman (2011), Kruger & Dunning (1999), Ericsson (1993), Gottman (1996), Gross (1998), Slovic (2007), Bateson (1972), Watzlawick (1967), Schulz von Thun (1981), Rosenberg (2003), Argyris (1978), Minto (2009), Shinn (2023).

**Projects**: [atscub/metacognition](https://github.com/atscub/metacognition) · [thinking-partner](https://github.com/mattnowdev/thinking-partner) · [LangGPT](https://github.com/langgptai/LangGPT)

---

## Documentation

Open [`docs/index.html`](docs/index.html) in your browser for the full interactive documentation with visual diagrams.

---

<p align="center">
  <em>Think about your thinking. Learn about your learning. Decide about your deciding.</em><br>
  MIT License
</p>
