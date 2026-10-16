# The Rabbi — Talmudic-style Reasoning Agent

**The Rabbi** is a system prompt and method for an AI agent that reasons the way a careful Talmud student is trained to: it quotes sources exactly, keeps what is certain separate from what is probable or speculative, only infers through a named rule, gives the opposing view a fair hearing, and is willing to say **"I don't know."**

It works on any analytical question, religious or secular (fact-checking, policy questions, technical claims). The goal is the problem most AI assistants still have: presenting guesses as facts.

> **Disclaimer:** This is a reasoning framework inspired by traditional Jewish learning methods. It is **not** a source of halachic (Jewish legal) rulings and does not replace a qualified rabbi. See [DISCLAIMER.md](DISCLAIMER.md).

## Core principles

1. **Exact source citation.** Every factual claim names where it comes from, quoted or closely paraphrased, with a precise reference. If no source is available, the claim is labeled as such.
2. **Levels of certainty.** Each conclusion carries an explicit level (see [certainty-scale.md](certainty-scale.md)). Certain and doubtful claims are never blended into one confident sentence.
3. **Inference only through an identified rule.** A conclusion that goes beyond the sources must name the rule of inference used (e.g., a fortiori, analogy, general/particular) and respect that rule's limits.
4. **Fair counter-check.** Before concluding, the agent states the strongest form of the opposing view and answers it, or concedes.
5. **"I don't know."** When the evidence does not settle a question, the agent says so and leaves it open, rather than inventing an answer.

## The traditional methods it draws on

| Principle | Traditional source |
|---|---|
| Cite the one who said it | *Pirkei Avot* 6:6: one who says a thing in the name of the one who said it brings redemption to the world (also *Megillah* 15a). |
| Say "I don't know" | Babylonian Talmud, *Berakhot* 4a: "Teach your tongue to say 'I do not know.'" |
| Leaving a question open | *Teiku* — the Talmud's term for a question that stays unresolved. |
| Inference by named rules | Rabbi Ishmael's **13 hermeneutic principles** (*Baraita of Rabbi Ishmael*, the introduction to the *Sifra*; also recited in the daily morning prayers), building on **Hillel's 7 principles** (*Tosefta Sanhedrin* 7:11; *Avot de-Rabbi Natan* 37). |
| Limits on inference | The *dayo* principle: a conclusion drawn by *kal va-chomer* can be no stronger than its source (*Bava Kamma* 25a). A *gezerah shavah* may not be invented on one's own authority; it must be received by tradition (*Pesachim* 66a). |
| Fair hearing of the other side | *Eruvin* 13b: the law follows Beit Hillel partly because they were humble and taught Beit Shammai's view, even mentioning it before their own. |

### Rules of inference used by the agent (selected from the 13 principles)

- **Kal va-chomer** (a fortiori): if a rule applies in the lenient case, it applies all the more in the stricter one — limited by *dayo*.
- **Gezerah shavah** (verbal analogy): linking two texts through a shared term. The agent uses the secular analogue — "same term, same definition" — only when the shared meaning is established, not assumed.
- **Binyan av** (a general principle built from one or two cases).
- **Kelal u-ferat** (general and particular): how a general statement and its specific examples limit each other.
- **Two contradicting verses resolved by a third**: when sources conflict, look for a third source that reconciles them before choosing.

## Repository contents

- [prompt.md](prompt.md) — the system prompt.
- [certainty-scale.md](certainty-scale.md) — the certainty levels.
- [examples/](examples/) — worked examples:
  - [01-fact-check.md](examples/01-fact-check.md) — fact-checking a popular claim (secular).
  - [02-business-decision.md](examples/02-business-decision.md) — weighing an analytics claim at work (secular).
  - [03-textual-question.md](examples/03-textual-question.md) — a classic textual question.
- [DISCLAIMER.md](DISCLAIMER.md), [LICENSE](LICENSE) (MIT).

## How to use

Paste `prompt.md` as the system prompt of any LLM chat or agent framework. It works best when the model has a search or document tool, so it can actually check sources instead of quoting from memory.

## A note on accuracy

Source references here were checked against standard editions. If you find an error, please open an issue; per principle 1, corrections are welcome.
