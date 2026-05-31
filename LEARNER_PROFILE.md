# Learner Profile — ML/DS Tutorial

Generated from session observations. Use this to design new classes.

---

## Background

- **Primary expertise:** Software engineering (Node.js, TypeScript, cloud infrastructure)
- **ML/DS level:** Beginner — no prior ML background
- **Relatable domains:** AWS costs, EC2, databases, API latency, server metrics, DevOps telemetry
- **Motivation:** Transitioning from engineering into ML/DS — wants to understand the *why*, not just memorize syntax

---

## Learning Style

### ✅ What works

| Pattern | Evidence from session |
|---------|----------------------|
| **Analogy first, then math** | "flour/salt" for feature scaling, "blindfolded on a hill" for gradient descent — both landed immediately |
| **Experience before explanation** | GD tab was confusing until experiments came before the formula. "Play first, read theory second" |
| **Before/After tables** | Asked for before/after on Stage 3 (correlation) and Stage 2 (log transform). Visual diffs make abstract steps concrete |
| **Short plain-English hook at top** | Green callout boxes with one-sentence summaries before any detail. Requested implicitly across multiple tabs |
| **Connecting new concepts to prior ones** | "The ball simulator is this exact loop" — linking GD formula to W1 training made it click |
| **Concrete numbers in examples** | `28×0.2 + 52000×0.5` for the dot product. Abstract notation alone doesn't stick |
| **Interactive > static** | Built games for every concept; plain docs were not requested |
| **Color-coded feedback** | Green = good, red = bad, yellow = warning. Used consistently throughout |
| **Progress persistence** | Immediately noticed when progress was lost on refresh — memory matters |

### ❌ What doesn't work

| Pattern | Evidence |
|---------|----------|
| **Walls of text** | Matrix tab became overwhelming at 6 dense cards. Was called out as "hard to understand" |
| **Math notation before intuition** | Greek letters (η, ∇) shown before experiencing gradient descent confused rather than clarified |
| **Jargon without parachute** | Terms like "multicollinearity", "vectorized", "imputation" caused follow-up questions until plain-English was added inline |
| **Code labels on UI buttons** | Pandas steps labeled `df.isna().sum()` instead of "Find missing values" — too technical for a newbie |
| **Theory → Practice ordering** | Original GD tab: formula first, experiments last. Reversed after feedback |
| **"What am I doing?" ambiguity** | Week 2 game had no explanation of the goal until it was explicitly added |

---

## Question Patterns

These are the types of questions asked — design new classes to pre-empt them.

### "What is X?" questions
Asked about nearly every new term before engaging:
- "What is Matrix Dimension Matcher?"
- "What is W1 (4×3)?"
- "What is Gradient Descent Simulator?"
- "What is Standardized Mode?"
- "What does correlation do?"

**Design implication:** Every new concept needs a `💡 In plain English:` callout *before* any detail. Never introduce a term without a one-sentence definition in everyday language.

### "Why do we need this?" questions
- "Why are there Raw Mode and Standardized Mode?"
- "I don't see the before and after" (on correlation)

**Design implication:** Every stage needs a "why does this matter?" section that appears *before* the technical implementation. The payoff must be visible before the work.

### "How does X get defined / work internally?" questions
- "How does W1 get defined?"
- "How does it calculate the median values for the gaps?"

**Design implication:** Don't stop at "here's the formula." Trace through one concrete example end-to-end with real numbers. Show the internal mechanics at least once.

---

## Content Structure That Works

Use this template for every new concept:

```
1. 💡 Plain-English hook (1–2 sentences, green callout box)
   "In plain English: [analogy that maps to engineering experience]"

2. The Problem (what breaks without this concept)
   - Show a concrete failure case
   - Numbers, not abstractions

3. Play/Experience (interactive element BEFORE theory)
   - Button, slider, or step to click through
   - Let them feel it before reading about it

4. Before / After (visual diff)
   - Side-by-side table or histogram
   - Label what changed and why it matters

5. The Explanation (now that they've seen it)
   - Plain English first, then formula
   - Connect to something they already know

6. Code (optional, last)
   - One-liner Python showing the operation
   - Only after concept is understood
```

---

## Analogy Bank — What Resonated

| Concept | Analogy that worked |
|---------|---------------------|
| Gradient descent | Blindfolded on a hill, always step downhill |
| Feature scaling | Flour in tons + salt in pinches — can't use the same scale |
| NumPy vectorization | Python loop = carrying boxes one at a time; NumPy = forklift |
| Multicollinearity | Two GPS apps shouting the same directions |
| W1 weight matrix | Connection strengths between inputs and neurons |
| Training loop | Random guess → measure error → step downhill → repeat |
| Matrix | A spreadsheet / table of numbers |
| Loss | "How wrong the model is" |

---

## Visual Preferences

- **Dark theme** — comfortable; never requested light mode
- **Color coding:** green = correct/good, red = wrong/bad, yellow = warning, blue = informational, purple = advanced
- **Tables over prose** for comparisons — side-by-side before/after is the preferred format
- **Canvas visualizations** — gradient descent ball, loss landscape contour map, histograms — all engaged with
- **Progress indicators** — XP bars, level pills, step counters — liked having visible progress
- **Short stat pills** — small `background:#21262d` boxes showing a single metric (e.g. "Skewness: 4.2") preferred over inline text

---

## Pacing Preferences

- Prefers **one concept per page/tab** — not multiple topics mixed together
- Wants **step-by-step unlocking** — Level 1 → Level 2 → Level 3, not everything at once
- Short sessions — questions came in bursts; each session focused on one confusion point
- **Memory across sessions is important** — asked for localStorage persistence when progress was lost

---

## Engineering Analogies That Map Well

Since the learner is a software engineer, use these framings:

| ML Concept | Engineering Frame |
|------------|-------------------|
| Loss function | Error rate / p95 latency — "how wrong is the system" |
| Gradient descent | Binary search / load balancer auto-tuning |
| Feature scaling | Normalizing API response times for fair comparison |
| Overfitting | Caching too aggressively — perfect on training data, fails on new data |
| Batch size | Pagination / chunk size in data processing |
| Epoch | One full pass through the job queue |
| Weights (W1, W2) | Config values the system tunes automatically |
| Neural network layer | A middleware transform — takes input, produces output |

---

## Class Generation Checklist

When building a new class for this learner:

- [ ] Plain-English hook at the very top (1–2 sentences, coloured callout)
- [ ] "Why do I need this?" before any implementation
- [ ] Interactive element before theory (slider, button, game mechanic)
- [ ] Before/After visual diff for any data transformation
- [ ] Every new term defined in plain English on first use
- [ ] At least one analogy from engineering domain (AWS, APIs, servers)
- [ ] Concrete numbers in at least one worked example
- [ ] Connect new concept to a previously learned concept
- [ ] Code shown last, not first
- [ ] Progress saved to localStorage if there are quiz/answer states
- [ ] No wall-of-text cards — max 4 sentences per paragraph
- [ ] "Reset progress" option if state is persisted
