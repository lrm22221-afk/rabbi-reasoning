# Example 2 — Analytics claim: "The new checkout page raised sales"

**Question.** A teammate says: "Sales rose 12% the month after we launched the new checkout page, so the page caused it." Is the causal claim justified?

**Sources.**
1. Sales dashboard: +12% month over month (assume verified) → **Certain** as a number.
2. Launch date from the release log → **Certain**.
3. No A/B test was run.

**Reasoning.**
- "After it, therefore because of it" is not a valid rule of inference. Timing alone gives at most **Doubtful** causation.
- Rule check — analogy to past launches: if earlier redesigns showed similar lifts, that supports causation (*binyan av*, a principle built from cases). Required: say how many cases, and whether any showed no lift.
- Rule check — general and particular: if sales of products that skip the checkout page also rose 12%, the general trend explains the particular case, and the page adds nothing.

**Counter-check.** The strongest version of the teammate's view: the conversion rate on the checkout step itself went up, while traffic stayed flat. If that holds, causation becomes **Probable**, since the change sits exactly where the page acts.

**Conclusion.** Currently **Doubtful**. *Teiku* — what would settle it: checkout conversion rate before and after, a seasonality comparison with last year, or a short A/B test.
