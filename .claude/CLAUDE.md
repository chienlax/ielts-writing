# Writing Style

This document consolidates the writing guidelines, rules, and registers for this workspace.

---

## Core Banned Patterns (Global Rules)

### 1. Performative Contrast (Strictly Banned)
**Performative contrast** is the habit of stating what something is *not* before stating what it *is*, to make a point sound weightier than it needs to be. The positive claim (`Y`) almost always stands on its own. The negation (`X`) is scaffolding that must be cut.

#### Banned Patterns:
*   `"This is not X. It is Y."`
*   `"The problem is not X. The problem is Y."`
*   `"Not X, but Y."` (as a standalone move)
*   `"It is not just X, it is Y."` (the profundity setup)
*   `"It is X, not Y."` (the reversal setup)
*   `"X is not the case, Y is."` (the formal setup)
*   `"The problem is X, not Y."` (the diagnostic setup)
*   *Any variant that stages the contrast as a dramatic reveal rather than stating the claim directly.*

#### Examples and Fixes:
*   [Bad] *The minimal experiment is not a shortcut. Its purpose is logical.*
    [Fixed] *The minimal experiment serves a logical purpose.*
*   [Bad] *Science is not just about discovery. It is an act of persuasion.*
    [Fixed] *Science is as much an act of persuasion as it is an act of discovery.*
*   [Bad] *The most difficult writing skill to develop is not clarity, not structure, and not precision. It is the ability to read your own work as a hostile reviewer would.*
    [Fixed] *The most difficult writing skill to develop is reading your own work as a hostile reviewer would.*

#### The One-Sentence Test:
Remove the negation sentence/clause. If the meaning is preserved, the negation was doing nothing. **Cut it.**

#### Legitimate Exceptions (Factual, Not Rhetorical):
1.  **Correcting a Widespread/Documented Error:** Correcting a documented misconception the reader is likely to hold, with specific evidence (e.g., *"Prior work assumed X; this is incorrect because..."*).
2.  **Defining Scope Boundaries:** Stating what the work does or does not cover (e.g., *"This paper does not address Y"* or *"the method does not apply to Z"*). Keep these brief.

#### Acceptable Alternatives (Integrated Negation):
If negation is genuinely necessary to qualify, keep it integrated and minimal within a single sentence:
*   **"rather than"** (e.g., *"deployed as a substitute for clarity rather than a complement to it"*)
*   **"not X but rather Y"** (use sparingly and only when genuinely informative)
*   **"more about X than Y"** / **"X, though/while Y"** (subordinates the qualification inside the main claim)

---

### 2. Em-Dash Ban (Strictly Banned)
**The em-dash (`—` or `--`) is banned globally.** There are no exceptions, no edge cases, and no contexts where an em-dash is allowed.
*   **Alternatives:** Use a comma, parentheses, a line break, a semicolon, or a new sentence.

---

### 3. Styling & Structural Trashing
*   **Excessive Bold/Italics:** Emphatic everywhere = emphatic nowhere. Avoid overuse.
*   **Filler Transitions:** Banned in formal contexts (e.g., *"Furthermore,"* *"In conclusion,"* *"It is worth noting,"* *"Herein,"* *"The aforementioned"*).
*   **Uniform Medium-Length Sentences:** Banned. They kill the rhythm. Vary sentence lengths (short, long, alternating).

---

## Academic & IELTS Register

### 1. Tone and Vocabulary Standard
*   **Target Level:** Clear, precise, well-structured, but not artificially elevated. Write at a natural, precise level without "cosplaying" at a higher level with inflated synonyms.
*   **Clarity Over Complexity:** If a simpler term conveys the same meaning precisely, use it. Prioritize correct usage of domain-specific technical terms, but keep all non-technical phrasing in plain, direct English.
*   **Grammar & Formatting:** Capitalize normally. No profanity. No lowercase aesthetic. No parenthetical aside comedy or footnoting for deflection. No sentimental register.
*   **Direct, Active Constructions:** Prefer active voice (e.g., *"we propose,"* *"the model encodes,"* *"this constraint ensures"*) over passive, bloated phrasing (e.g., *"it was proposed that"*).
*   **Density:** One idea per sentence. One idea per paragraph. Cut sentences that repeat previous ideas in slightly different words.

### 2. Grammatical Diversity Toolkit
Vary sentence structures using the following toolkit (especially key for IELTS writing):
*   **Inversion:** Fronting a negative or restrictive adverbial (e.g., *"Seldom have we observed..."*).
*   **Inverted Conditionals:** Replace "if" with an inverted auxiliary (using *were*, *had*, or *should* as the lead):
    *   *“Were the constraints relaxed, the search space would collapse.”*
    *   *“Had the decomposition failed, the entire pipeline would have stalled.”*
    *   *“Should this assumption not hold, the bound becomes loose.”*
*   **Mixed Conditionals:** For differing condition and consequence time frames.
*   **Cleft Sentences:** To redirect emphasis onto a specific element.
*   **Fronting / Topicalization:** Moving a non-subject element to the front for thematic continuity.
*   **Participle and Absolute Clauses:** Compressing background information into a modifier.
*   **Concessive Constructions.**

### 3. Hedging Register
Confidence must match the strength of the evidence. Definitions, mathematical identities, and empirically verified results do not require hedging. Interpretations, generalizations, comparisons, and causal claims **must be hedged**:
*   **Modal Verbs:** *may, might, could, would tend to*
*   **Epistemic Adverbs:** *arguably, presumably, apparently, seemingly*
*   **Qualifying Verbs:** *appears to, seems to, tends to, suggests that*
*   **Scoped Claims:** *in most cases, under these conditions, for the instances tested, within this framework*
*   **Attribution Hedges:** *the evidence suggests, the results indicate, this may imply, one possible interpretation is*

---

## Technical & Documentation Style (OR Papers / Specs)

### 1. Explaining the Mechanism
Every technical claim needs its mechanism explained: not just *what* is true, but *why* it is true, and *what breaks* if you ignore it.
*   [Bad] *K-Means fails on hard instances.*
*   [Good] *K-Means fails on hard instances because it is a distance-based heuristic with no awareness of combinatorial thresholds. If a cluster of students collectively takes ≥ T unique external exams, that sub-exam forms an infeasible clique, variance reduction does not prevent this.*

### 2. Math & Formulas
*   Use LaTeX for formal expressions.
*   **Never leave a formula to speak for itself.** Always follow it with a plain English sentence explaining what it means in domain terms.
*   Notation must be defined on first use and consistent throughout (e.g., if $T$ represents timeslots, it remains timeslots).

### 3. Core Structural Arc
Start with why the problem is hard before proposing solutions. Document the failure modes of naive approaches first so design decisions are legible:
1.  What the problem is and why it is non-trivial.
2.  What was tried / why the obvious approach fails (mechanism, not just result).
3.  Key insight(s) that reframe the problem.
4.  The solution and its justification.
5.  Known limitations / open questions.

### 4. Document Types
*   **Synthesis/Reasoning Docs:** Focused on *why something works*. Include the chronology of understanding (e.g., *"We first tried X..."*), be explicit about initial unknowns, and note parts that remain empirical.
*   **Implementation Docs:** Focused on code explanation. Must include:
    *   Table for decision variables (name, type, scope, representation).
    *   Code references alongside plain-English descriptions for each constraint.
    *   Objective table detailing: `term | weight | requirement covered | what it penalizes`.
    *   Mandatory **Known Issues** section detailing structural fragilities (status, problem description, impact, potential fix).
    *   Clear notes on non-implemented items (do not imply code does something it does not).

---

## Personal & Casual Register

### 1. Voice and Rhythm
*   **Aesthetic:** Lowercase, conversational, first-person. Conversational flow marked by contractions (*gonna, kinda*), conversational pivots (*well, i mean, like*), and functional (non-decorative) profanity.
*   **Punctuation & Flow:** Comma-heavy to mark natural pauses in thought progression. 
*   **Transitions:** "well" buffers self-corrections or soft pivots; "i mean" for approximation.

### 2. Humor and Deflection
*   **Register Drop:** Build anticipation or seriousness, then undercut it with a mundane anticlimax (e.g., *"gross / cant stand someone, well i cant stand myself either, i'm a hypocrite"*).
*   Never explain the joke. Sarcasm is dry, self-aware, and directed inward first.

### 3. Emotion and Sentimentality
*   **Concrete Detail:** Lean on specific physical or sensory details over declared general emotions (e.g., *"i want to hear his voice"* rather than *"i miss him"*).
*   **Sentimental Structure:** Earnest statement followed by its own softer, slightly varied echo (e.g., *"i think i will be fine. i have to be."* or *"i think so. i think so. i thought so."*).
*   **Progression:** Spiral → exhaust → quiet declarative.
