# Recursive First Principles

> Recursively apply first principles thinking until converging on fundamental truths or discovering problems don't exist.

## What is This?

A thinking tool that doesn't stop at the first answer. Instead, it:

1. Analyzes the problem (Round 1)
2. Questions the analysis itself (Round 2)
3. Questions the questioning (Round 3)
4. Continues until reaching stable truth

**Like a Socratic dialogue that doesn't accept "good enough" answers.**

---

## 5-Minute Quick Start

**Don't read the full guide yet.** Try this minimal workflow first:

### Step 1: Ask the 3 Core Questions

For ANY decision, ask:

1. **🔍 n=?** → How many examples support this? (Watch for n=1, n=0)
2. **🚩 Assumptions?** → What am I assuming is true? (Watch for "should/must/need")
3. **🔄 Falsifiable?** → What evidence would prove me wrong?

### Step 2: Trigger the Skill

Say to Claude:

- "Recursively analyze [your decision]"
- "Apply recursive first principles to [problem]"

### Step 3: Let It Run

Claude will execute 3-5 rounds, each questioning the previous round. You just watch.

### Step 4: Act on the Result

The final round gives you either:

- ✅ **Strong conclusion** (backed by evidence)
- ⚠️ **Weak conclusion** (needs more data)
- ❌ **Problem doesn't exist** (based on false assumptions)

**That's it.** You've learned 80% of what matters. Read below for details.

---

---

## Why Use This?

**Problem:** Single-pass analysis often misses:

- Assumptions disguised as truths
- Logical leaps in reasoning
- Sample size = 1 generalizations
- Solutions looking for problems

**Solution:** Each recursion round catches what the previous round missed.

---

## Quick Start

**Trigger phrases:**

- "Recursively analyze [problem]"
- "Apply recursive first principles to [decision]"
- "层层质疑 [问题]"
- "递归分析"

**What happens:**
Claude will execute 3-5 rounds of questioning, each challenging the previous round, until converging on a stable conclusion.

---

## When to Use

✅ **Use for:**

- Major architectural decisions
- Challenging core assumptions
- Evaluating whether to refactor critical systems
- Analyzing your own analysis (meta-reasoning)

❌ **Don't use for:**

- Simple bugs or features
- Time-sensitive decisions
- Well-understood problems

> **⚠️ Cost:** This runs 3-5 rounds of deep analysis. Reserve for important decisions.

---

## Example Output

```
Round 1: "Need to add 8 new features to this skill"
    ↓
Round 2: "Wait, what evidence supports these features?"
    ↓
Round 3: "No evidence exists. Sample size = 0"
    ↓
Round 4: "Confirmed. Don't add features."
    ↓
CONVERGED: Original plan was premature optimization
```

**Real case:** Prevented 5+ hours of unnecessary work. See `examples/skill-optimization-case.md`

---

## How It Works

### Convergence Conditions (When It Stops)

Recursion stops when hitting **any** of these:

1. ✅ Last 2 rounds reach same conclusion
2. ✅ Hit irreducible truth (physics/math law)
3. ✅ Problem proven non-existent
4. ✅ Further analysis costs more than value
5. ⚠️ Max depth reached (5 rounds - safety limit)

---

## Common Patterns

**The Assumption Pyramid:**

```
Round 1: Build on Assumption A
Round 2: A is based on Assumption B
Round 3: B is based on Assumption C
Round 4: C is false
→ Entire pyramid collapses
```

**The Pendulum:**

```
Round 1: Extreme position
Round 2: Overcorrect to opposite extreme
Round 3: Settle in balanced middle
→ Converged
```

**Question Dissolution:**

```
Round 1: How to solve Problem X?
Round 2: Does Problem X exist?
Round 3: No evidence X exists
→ Question dissolves
```

---

## Files

- **`SKILL.md`** - Complete documentation
- **`examples/skill-optimization-case.md`** - Real case from actual usage
- **`references/theoretical-foundation.md`** - Why recursion works (cognitive science, philosophy)

---

## Relationship to Other Skills

| Skill                        | Purpose                    | When to Use                 |
| ---------------------------- | -------------------------- | --------------------------- |
| `first-principles`           | Single deep analysis       | Straightforward problems    |
| `recursive-first-principles` | Multi-round validation     | Complex/ambiguous decisions |
| `5-whys`                     | Trace historical causality | "Why did this happen?"      |

**Tip:** Can use `first-principles` for Round 1, then this skill to recurse.

---

## Anti-Patterns to Avoid

❌ **Analysis Paralysis** - Using recursion to avoid deciding  
❌ **Weaponized Skepticism** - Tearing everything down without building up  
❌ **Sample Size = 1** - Generalizing from one experience  
❌ **Ignoring Convergence** - Continuing when already converged

---

## Meta-Note

**This skill was created through recursive first principles:**

```
Round 1: Analyzed content-research-writer skill
Round 2: Questioned the analysis (found it was premature)
Round 3: Analyzed first-principles skill
Round 4: Questioned those optimizations (3/4 were invalid)
Round 5: Proposed "optimize-or-not" skill
Round 6: Questioned that skill's value (user feedback)
    ↓
CONVERGED: The recursion process itself is the valuable pattern
    ↓
Created this skill to capture that pattern
```

**The skill's existence validates its own method.** 🔄

---

## Version

**1.0.0** - Initial release based on real-world usage

## Author Note

Created from actual experience making (and catching) premature optimization mistakes through recursive questioning. The documented examples are not hypothetical - they're the actual conversation that led to this skill's creation.

**Recursion works.**
