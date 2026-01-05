---
name: Recursive First Principles
description: Automatically executes multiple rounds of recursive questioning, applying first principles thinking to challenge each conclusion layer by layer until converging on fundamental truths or proving the problem doesn't exist. Like a Socratic dialogue that doesn't stop at the first answer.
version: 1.0.0
---

# Recursive First Principles

## ⚡ Quick Start: The Core 3 Rules

**New to this? Start here** - Master these 3 rules in 5 minutes:

### 1. 🔍 Sample Size Check (n=?)

**Question:** "How many examples support this conclusion?"  
**Red Flag:** n=1 (single case), n=0 (zero evidence), "always/never" claims  
**Example:** "Users hate this feature" → n=? → n=2 complaints → Insufficient

### 2. 🚩 Assumption Detector ("should/need/must")

**Question:** "What assumptions am I treating as facts?"  
**Red Flags:** "should", "need to", "must", "obviously", "clearly"  
**Example:** "We need Redis for caching" → Why? → "For scale" → Current scale? → 100 users → Assumption: scale problem exists (false)

### 3. 🔄 Falsification Test (What would prove me wrong?)

**Question:** "What evidence would disprove this?"  
**Red Flag:** "Nothing can change my mind" → You're not analyzing, you're justifying  
**Example:** "This code is slow" → What would disprove? → Benchmark showing <100ms → Run benchmark → 45ms → Disproved

**That's it.** These 3 rules cover 80% of what you need. The rest of this document explains the automation process.

---

A meta-reasoning tool that recursively applies first principles thinking to its own conclusions, diving deeper through multiple rounds of questioning until reaching irreducible truths or discovering the problem is illusory.

## When to Use This Skill

### ✅ Perfect For

**Technical architecture decisions with long-term impact:**

- Choosing tech stack for new projects (React vs Vue, microservices vs monolith)
- Evaluating major refactoring decisions (rewrite vs incremental)
- Database technology choices (PostgreSQL vs MongoDB vs DynamoDB)
- Challenging "always done it this way" assumptions in legacy systems

**When you feel cognitive dissonance:**

- "Solution seems right, but feels wrong"
- "Everyone says yes, but I'm uncertain"
- "Conventional wisdom conflicts with context"

### ⚠️ OK, But Not Ideal

**Moderately complex decisions:**

- API design patterns (REST vs GraphQL)
- Library choices for specific features
- Code organization debates

**Why not ideal:** May be overkill; simpler methods (pros/cons list) might suffice.

### ❌ Don't Use For

**Simple/time-sensitive tasks:**

- Bug fixes with clear root cause
- Feature additions with proven patterns
- Urgent production issues (no time for 3-5 rounds)

**Trivial decisions:**

- Naming variables
- Code formatting preferences
- Minor optimizations

> **⚠️ Cost Warning:** This skill runs 3-5 rounds of deep analysis (15-60 minutes). Reserve it for decisions that matter.

---

### 🆚 When to Use THIS vs Other Methods

| Method                         | Best For                                        | Time      | Depth        |
| ------------------------------ | ----------------------------------------------- | --------- | ------------ |
| **Recursive First Principles** | Technical architecture, challenging assumptions | 30-60 min | Very deep    |
| **5-Whys**                     | Root cause analysis, debugging failures         | 10-15 min | Medium       |
| **Six Thinking Hats**          | Team decisions, exploring perspectives          | 20-40 min | Breadth      |
| **Pre-mortem**                 | Risk analysis, failure prevention               | 15-30 min | Future focus |
| **Pros/Cons List**             | Simple trade-offs, quick decisions              | 5-10 min  | Shallow      |

**Key difference:** This tool recursively questions its own conclusions until convergence. Others stop after 1-2 passes.

---

## Core Concept

**Traditional First Principles:** Analyze once, get a conclusion  
**Recursive First Principles:** Analyze → Question the analysis → Question the questioning → Continue until convergence

**Example from real usage:**

```
Round 1: "This skill needs 8 improvements"
Round 2: "Wait, are those improvements based on real evidence?"
Round 3: "My Round 2 critique itself might be too harsh"
Round 4: "Actually, Round 2 was right - no evidence exists"
→ Converged: Original improvements were premature
```

---

## Core Process

### Round 1: Initial First Principles Analysis

Apply standard first principles to the problem:

1. Identify problem essence
2. Challenge assumptions
3. Establish ground truths
4. Build reasoning chain
5. Reach initial conclusion

**Output:** Initial analysis with proposed solution/approach

---

### Round 2: Meta-Analysis (Question the Analysis)

Apply first principles **to the Round 1 analysis itself:**

**Key Questions:**

- **Ground Truth Verification:** Are your "ground truths" actually assumptions disguised?
  - Red flag: Contains "should", "need", "better" → It's a preference, not truth
  - Test: Can you prove it's false? If not provable → assumption
- **Reasoning Chain Audit:** Are there logical leaps?
  - Check each step: Does B actually follow from A?
  - Look for hidden assumptions in the arrows
- **Evidence Quality:** What's the sample size?
  - n=1: Extremely weak
  - n=5: Weak pattern
  - n=20+: Reasonable evidence
  - Personal opinion: Not evidence
- **Problem Existence:** Do you have proof the problem exists?
  - User complaints? Metrics? Incidents?
  - Or just "I think this could be better"?

**Output:** Critique of Round 1, identifying flaws in reasoning

---

### Round 3: Meta-Meta-Analysis (Question the Questioning)

Apply first principles **to the Round 2 critique:**

**Key Questions:**

- **Overcorrection Check:** Did Round 2 swing too far in the opposite direction?
- **New Assumptions:** What new assumptions did the critique introduce?
- **Evidence for Critique:** Is the critique itself well-supported?
- **Net Progress:** Are we closer to truth than Round 1?

**Output:** Refined analysis that incorporates valid critiques

---

### Round N: Continue Recursion

Keep applying first principles to each new conclusion until hitting a **convergence condition**.

---

## Convergence Conditions (When to Stop)

Stop recursion when you hit **any** of these:

### 1. ✅ Stable Conclusion

**Condition:** Last 2 rounds reach the same conclusion  
**Signal:** "Round N confirms Round N-1"  
**Example:**

- Round 4: "Don't optimize, no evidence"
- Round 5: "Confirmed, don't optimize"
- → Converged

### 2. ✅ Irreducible Truth Reached

**Condition:** Hit a physics/math law that cannot be decomposed further  
**Examples:**

- "Memory is finite" (hardware constraint)
- "Network calls have latency" (physics)
- "Humans can process 7±2 items" (cognitive science)

### 3. ✅ Problem Proven Non-Existent

**Condition:** Discovered the problem was based on false assumptions  
**Example:**

- Round 1: "Need to optimize for scale"
- Round 3: "No evidence of scale problem"
- → Converged: Problem doesn't exist

### 4. ✅ Cost Exceeds Benefit

**Condition:** Next round of questioning costs more than value of answer  
**Signal:** "Further analysis won't change the decision"

### 5. ⚠️ Max Depth Reached

**Condition:** Hit 5 rounds (safety limit to prevent infinite recursion)  
**Action:** Force convergence with current best answer

---

## 🛑 Stop Signals (Behavioral Circuit Breakers)

**Even if convergence conditions aren't met, STOP if you hit these warning signals:**

### 🔴 Red Signal 1: Sunk Cost Spiral

**Symptom:** "I've invested 3+ hours, I need to finish this analysis"  
**Reality:** You're justifying past time investment, not optimizing future decisions  
**Action:** Stop NOW. Ask: "If I started fresh today, would I spend 3 hours on this?"

**Example:**

- 2 hours into analysis: "This refactoring decision needs more rounds"
- Reality check: Decision impact = saves 1 hour/week
- Math: 2 hours cost > 2 weeks benefit → STOP

### 🟡 Red Signal 2: Analysis Enjoyment (Procrastination)

**Symptom:** "This is intellectually stimulating, let's go deeper"  
**Reality:** You're avoiding actual implementation work  
**Action:** Ask: "Am I analyzing because I need clarity, or because I'm avoiding action?"

**Example:**

- Round 5: "Let's question the meta-meta-meta assumptions"
- Truth: You already have 80% confidence to decide
- Math: 80% confidence is enough → ACT, don't analyze

### 🟠 Red Signal 3: Diminishing Returns

**Symptom:** Last 2-3 rounds repeat the same insights  
**Reality:** You've extracted all useful signal, now just adding noise  
**Action:** If Round N = Round N-2, you've converged (even if conclusions differ slightly)

**Example:**

- Round 3: "Need more data, sample size = 1"
- Round 4: "Need more data, sample size = 1"
- Round 5: "Need more data, sample size = 1"
- → STOP. Go collect data, don't analyze further.

### 🟣 Red Signal 4: Loss Aversion Paralysis

**Symptom:** "I can't decide until I'm 100% certain"  
**Reality:** You're over-weighting potential losses vs potential gains (loss aversion bias)  
**Action:** Ask: "What's the cost of being wrong? What's the cost of not deciding?"

**Example:**

- Analysis paralysis: "Need to analyze 5 more rounds to be sure"
- Reality: Wrong decision cost = 2 days rework
- Opportunity cost of delay = 1 week blocked work
- Math: 2 days < 1 week → DECIDE NOW with current info

---

**Meta-Rule:** If you're reading this section multiple times during one analysis, you've hit a stop signal. Stop analyzing. Start acting.

---

## Output Format

For each round, output:

```markdown
## Round N: [Focus of This Round]

### What We're Questioning

[Describe what this round challenges from the previous round]

### Key Discoveries

1. **[Discovery Category]:** [Finding]
2. **[Discovery Category]:** [Finding]

### Revised Conclusion

[What we now believe to be true]

### Convergence Check

- [ ] Stable conclusion (matches previous round)
- [ ] Irreducible truth reached
- [ ] Problem proven non-existent
- [ ] Cost exceeds benefit
- [ ] Max depth (5 rounds)

**Decision:** [✅ CONVERGED / 🔄 CONTINUE TO ROUND N+1]
**Reason:** [Brief explanation]
```

---

## Final Output

After convergence, provide:

```markdown
# Recursive Analysis Complete

## Convergence Summary

**Stopped at:** Round N
**Reason:** [Convergence condition met]

## Evolution of Understanding

Round 1: [Initial belief]
Round 2: [First correction]
Round 3: [Second correction]
...
Round N: [Final truth]

## Key Insights from Recursion

1. **[Major insight]** - [What the recursion revealed]
2. **[Pattern discovered]** - [What kept appearing]
3. **[Avoided mistake]** - [What would have happened without recursion]

## Final Recommendation

[Actionable conclusion based on converged understanding]

## Confidence Level

[Low/Medium/High] - [Justification]
```

---

## Common Patterns

### Pattern: The Assumption Pyramid

**Symptom:** Each round discovers the previous round's "truths" were assumptions

**Example:**

```
Round 1: Build on Assumption A
Round 2: A is based on Assumption B
Round 3: B is based on Assumption C
Round 4: C is false
→ Entire pyramid collapses
```

### Pattern: The Pendulum Swing

**Symptom:** Conclusions swing back and forth

**Example:**

```
Round 1: Extreme position
Round 2: Overcorrect to opposite extreme
Round 3: Settle in balanced middle
→ Converged
```

**How to detect:** If Round N contradicts Round N-2, you might be swinging

### Pattern: The Premature Convergence

**Symptom:** Two rounds agree, but both are wrong

**Detection:** Check if the "agreement" is based on shared assumptions

**Solution:** Force one more round questioning the shared assumptions

### Pattern: The Infinite Descent

**Symptom:** Can keep questioning forever, no natural stopping point

**Example:** "Why do we exist?" type questions

**Solution:** Apply "Cost Exceeds Benefit" convergence condition

---

## Anti-Patterns (What to Avoid)

### ❌ Analysis Paralysis

**Symptom:** Using recursion to avoid making decisions  
**Fix:** Set a deadline - "We recurse until Friday, then decide"

### ❌ Weaponized Skepticism

**Symptom:** Questioning everything to prove nothing works  
**Fix:** Require each critique to propose something better

### ❌ Sample Size = 1 Generalization

**Symptom:** Building universal theories from one experience  
**Example:** "I had this problem once, so everyone will"  
**Fix:** Explicitly check sample size in every round

### ❌ Ignoring Convergence Signals

**Symptom:** Continuing to recurse when already converged  
**Fix:** Strictly apply convergence conditions

---

## Integration with Other Skills

| When to Use                         | Which Skill                  |
| ----------------------------------- | ---------------------------- |
| Single deep analysis needed         | `first-principles`           |
| Need to validate/challenge analysis | `recursive-first-principles` |
| Tracing historical decisions        | `5-whys`                     |
| Code quality review                 | `code-review-excellence`     |

**Tip:** You can call `first-principles` in Round 1, then use this skill to recurse

---

## Practical Tips

### Tip 1: Start with Strong Opinions

Recursion works best when you start with a clear position to challenge. Wishy-washy starting points lead to wishy-washy conclusions.

### Tip 2: Look for Sample Size

In every round, ask: "How many data points support this?" Sample size = 1 is the most common flaw.

### Tip 3: Watch for "Should" and "Need"

These words often disguise preferences as truths:

- "Users need X" → Is that proven or assumed?
- "We should use Y" → Based on what evidence?

### Tip 4: Set a Time Budget

Recursion can take hours. Decide upfront: "We'll recurse for 2 hours max."

### Tip 5: Document the Journey

The value isn't just the final answer - it's seeing how your understanding evolved through rounds.

---

## Example: Full Recursive Analysis

See `examples/skill-optimization-case.md` for a real-world example based on actual usage of this skill.

---

## Meta-Note

This skill description was itself created through recursive first principles:

- Round 1: Designed "optimize-or-not" skill
- Round 2: Questioned whether that skill had value
- Round 3: Discovered the real value was the recursion process
- Round 4: Designed this skill
- → Converged: Recursion is the valuable pattern

**Recursion works.** 🔄

---

## Quick Reference

**The Recursive Checklist:**

Before each round:

- [ ] What am I questioning this round?
- [ ] What evidence do I have?
- [ ] What's my sample size?
- [ ] Are my "truths" actually assumptions?
- [ ] Check convergence conditions
- [ ] Should I stop or continue?

**Stop when:**

- ✅ Last 2 rounds agree
- ✅ Hit physics/math law
- ✅ Problem proven fake
- ✅ Further analysis unhelpful
- ⚠️ Hit 5 rounds
