# Documentation Style

Audience: me. Write like I'm picking this up six months from now and need to reconstruct the thinking, not just the conclusion. AND FOR THE LOVE OF GOD, NO EM-DASH.

---

## The Core Principle

Every technical claim needs its mechanism explained. Not just *what* is true but also *why* it is true, and *what breaks* if you ignore it.

Bad:
> K-Means fails on hard instances.

Good:
> K-Means fails on hard instances because it is a distance-based heuristic with no awareness of combinatorial thresholds. If a cluster of students collectively takes ≥ T unique external exams, that sub-exam forms an infeasible clique, variance reduction does not prevent this.

The explanation should be tight enough that a reader can reconstruct the reasoning independently. If a sentence contains a claim that could be wrong, the explanation is what lets you verify it later.

---

## Structure

**Start with why the problem is hard, before proposing solutions.**
Document the failure mode of the naive or previous approach first. This makes the design decision legible — you understand what constraint the solution is satisfying.

```
1. What the problem is and why it's non-trivial
2. What was tried / why the obvious approach fails (mechanism, not just result)
3. Key insight(s) that reframe the problem
4. The solution and its justification
5. Known limitations / open questions
```

This is not a strict template. Match the structure to the content. But the *reasoning arc*: failure → insight → solution should almost always be present.

---

## Math

LaTeX for formal expressions. Always follow with a plain English sentence that says what it means in domain terms.

```markdown
$$K_i = \{ u \in V \mid X_u = X_v \text{ for all } v \in K_i \}$$

Students in the same equivalence class take the exact same 
set of external exams. Grouping them creates zero conflict inflation — 
to the CP solver, they are structurally interchangeable.
```

Never leave a formula to speak for itself. The formula is precise; the sentence is what makes it retrievable later.

Notation should be defined on first use and consistent throughout. If $T$ means number of timeslots, it means that for the whole document.

---

## Two Doc Types

### Synthesis / Reasoning Docs

Written after working through a problem: reading, experimenting, or thinking. The goal is to crystallize *why something works the way it does*, not just document that it works.

- Include the chronology of understanding if it matters. "We first tried X. It failed because Y. This revealed that the real structure is Z."
- Be explicit about what you didn't know at the start.
- Note which parts are still uncertain or empirical.
- LaTeX appears naturally where precision is needed.

### Implementation Docs

Written to explain existing code: variables, constraints, objective terms, pipeline stages.

- Table for decision variables (name, type, scope, what it represents).
- Each constraint gets a code reference (`main.py:111–113`) and a plain-English description alongside the formula.
- For the objective, include a table: term | weight | which requirement it covers | what it penalizes.
- Known Issues section is mandatory. Document structural fragilities even if they haven't caused problems yet. Include: status, problem description, impact, potential fix.
- Non-implemented items get their own note, don't imply the code does something it doesn't.


### What to Avoid

| Avoid | Why |
|---|---|
| em-dash, in any context, for any reason | BANNED. always a comma, parenthesis, or line break instead. no exceptions, ever |
| "it's not X, it's Y" | Performative contrast formula. Instead: "it is not X but rather / more about Y" |
| variants: "it is not X. it is Y." / "it is not just X, it is [insert profound thing]" | Same formula, same problem |
| Filler transitions ("Furthermore," "In conclusion," "It is worth noting") | Wrong register entirely |
| Uniform medium-length sentences throughout | Kills the rhythm |
| Excessive italics or bold | Emphatic everywhere = emphatic nowhere |

---

## Part II: Academic Specific

- **Rhythm and sentence variety.** Short sentences still land. Long ones still build. Uniform medium-length sentences are still boring.
- **Specificity over generality.** Name the exact method, the exact metric, the exact term.
- **Clarity over complexity.** The right word at my vocabulary level, not an inflated synonym. If a simpler term conveys the same meaning precisely, use it. In academic mode, the goal is to communicate one point clearly, not to hold tension or complicate the thesis. Take a position, defend it, acknowledge genuine limitations, move on. If the ideas are strong; the language would not need to cosplay at a higher level. Prioritize: correct usage of domain-specific terms (which can be technical), plain language for everything else.

---

### What "at my level" means

- Correct technical terminology for the domain (CP-SAT, decomposition, feasibility, branching, etc.), these are precise and stay precise
- Plain English for everything that is *not* technical, no padding, no "it is worth noting that," no "herein"
- Direct active constructions: "we propose," "the model encodes," "this constraint ensures", not "it was proposed that" or "the aforementioned model"
- One idea per sentence. One idea per paragraph. Cut the sentence that repeats the previous one in slightly different words.