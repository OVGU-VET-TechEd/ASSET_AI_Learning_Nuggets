<!--
author:   Hannes Tegelbeckers · OVGU Magdeburg · ASSET project (UNESCO-UNEVOC Network)
email:    hannes.tegelbeckers@ovgu.de
version:  2026.1.0
language: en
narrator: UK English Female
license:  CC BY-SA 4.0
comment:  ASSET AI starter course 2026, Nugget 2 of 5 (AI Basics): learning from data, bias, how chat assistants produce answers, five key terms. Acquire level.

@style
/* ASSET 2026 design system v1 — keep this block identical in all 2026 nuggets */
:root {
  --a-ink: #1f2933;
  --a-muted: #52606d;
  --a-blue: #0b5394;
  --a-blue-soft: #eaf2fb;
  --a-amber: #b45309;
  --a-amber-soft: #fff5e6;
  --a-green: #2f7d4f;
  --a-green-soft: #edf7f0;
  --a-violet: #6b46c1;
  --a-violet-soft: #f4f0fc;
  --a-teal: #0f766e;
  --a-teal-soft: #e8f6f4;
  --a-red: #b42318;
  --a-red-soft: #fdf0ef;
  --a-indigo: #3730a3;
  --a-indigo-soft: #eef0fb;
  --a-line: #d9e2ec;
}

.hero {
  background: linear-gradient(120deg, #eaf2fb 0%, #f1f5fa 55%, #eef7f4 100%);
  border-bottom: 3px solid var(--a-blue);
  border-radius: 12px;
  padding: 1.6rem 1.4rem;
  color: var(--a-ink);
  margin-bottom: 1.2rem;
}
.hero__kicker { color: var(--a-muted); font-size: .85em; letter-spacing: .04em; text-transform: uppercase; }
.hero__title { color: var(--a-blue); font-size: 2em; font-weight: 700; line-height: 1.15; margin: .4rem 0 .3rem; }
.hero__title em { color: var(--a-teal); font-style: normal; }
.hero__sub { color: var(--a-muted); font-size: 1.05em; }

.chips { display: flex; flex-wrap: wrap; gap: .4rem; margin-top: .9rem; }
.chip {
  display: inline-block; background: #fff; color: var(--a-ink);
  border: 1px solid var(--a-line); border-radius: 999px;
  padding: .15rem .7rem; font-size: .85em;
}
.chip--level { background: var(--a-blue); border-color: var(--a-blue); color: #fff; }

/* phase stepper: @steps(n) highlights step n */
.steps { display: flex; flex-wrap: wrap; gap: .3rem; margin: .2rem 0 1rem; }
.step {
  flex: 1 1 5.5rem; text-align: center; font-size: .78em; padding: .3rem .2rem;
  border-radius: 6px; background: #f1f4f8; color: var(--a-muted); border: 1px solid var(--a-line);
}
.steps--1 .step:nth-child(1) { background: var(--a-amber);  color: #fff; border-color: var(--a-amber); }
.steps--2 .step:nth-child(2) { background: var(--a-blue);   color: #fff; border-color: var(--a-blue); }
.steps--3 .step:nth-child(3) { background: var(--a-green);  color: #fff; border-color: var(--a-green); }
.steps--4 .step:nth-child(4) { background: var(--a-violet); color: #fff; border-color: var(--a-violet); }
.steps--5 .step:nth-child(5) { background: var(--a-teal);   color: #fff; border-color: var(--a-teal); }
.steps--6 .step:nth-child(6) { background: var(--a-indigo); color: #fff; border-color: var(--a-indigo); }

.box {
  border: 1px solid var(--a-line); border-left: 5px solid var(--a-blue);
  border-radius: 0 10px 10px 0; background: var(--a-blue-soft); color: var(--a-ink);
  padding: .8rem 1rem; margin: 1rem 0;
}
.box__label { font-weight: 700; font-size: .78em; letter-spacing: .05em; text-transform: uppercase; margin-bottom: .3rem; color: var(--a-blue); }
.box--case   { border-left-color: var(--a-amber);  background: var(--a-amber-soft); }
.box--case   .box__label { color: var(--a-amber); }
.box--try    { border-left-color: var(--a-green);  background: var(--a-green-soft); }
.box--try    .box__label { color: var(--a-green); }
.box--check  { border-left-color: var(--a-violet); background: var(--a-violet-soft); }
.box--check  .box__label { color: var(--a-violet); }
.box--class  { border-left-color: var(--a-teal);   background: var(--a-teal-soft); }
.box--class  .box__label { color: var(--a-teal); }
.box--warn   { border-left-color: var(--a-red);    background: var(--a-red-soft); }
.box--warn   .box__label { color: var(--a-red); }
.box--ahead  { border-left-color: var(--a-indigo); background: var(--a-indigo-soft); }
.box--ahead  .box__label { color: var(--a-indigo); }

.cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: .8rem; margin: 1rem 0; }
.card {
  background: #fff; color: var(--a-ink); border: 1px solid var(--a-line);
  border-top: 4px solid var(--a-blue); border-radius: 10px; padding: .8rem 1rem;
}
.card__title { font-weight: 700; color: var(--a-blue); margin-bottom: .3rem; }
.card--amber  { border-top-color: var(--a-amber); }  .card--amber  .card__title { color: var(--a-amber); }
.card--green  { border-top-color: var(--a-green); }  .card--green  .card__title { color: var(--a-green); }
.card--violet { border-top-color: var(--a-violet); } .card--violet .card__title { color: var(--a-violet); }
.card--teal   { border-top-color: var(--a-teal); }   .card--teal   .card__title { color: var(--a-teal); }
.card--red    { border-top-color: var(--a-red); }    .card--red    .card__title { color: var(--a-red); }
.card--indigo { border-top-color: var(--a-indigo); } .card--indigo .card__title { color: var(--a-indigo); }

.persona {
  display: flex; gap: .9rem; align-items: flex-start;
  background: #fff; color: var(--a-ink); border: 1px solid var(--a-line);
  border-radius: 12px; padding: .9rem 1rem; margin: 1rem 0;
}
.persona__avatar {
  flex: 0 0 3rem; height: 3rem; border-radius: 50%; background: var(--a-amber-soft);
  color: var(--a-amber); font-size: 1.5em; display: flex; align-items: center; justify-content: center;
}
.persona__name { font-weight: 700; color: var(--a-amber); }

.takeaways { background: #fff; color: var(--a-ink); border: 2px solid var(--a-indigo); border-radius: 12px; padding: .8rem 1.2rem; margin: 1rem 0; }

.partners { display: flex; flex-wrap: wrap; gap: 1.4rem; align-items: center; margin-top: 1.2rem; color: var(--a-muted); font-size: .85em; }
.partners img { height: 52px; width: auto; border-radius: 8px; }

.fw { display: grid; grid-template-columns: 1.3fr repeat(3, 1fr); gap: 3px; font-size: .82em; margin: 1rem 0; }
.fw div { padding: .45rem .5rem; background: #f1f4f8; color: var(--a-ink); border-radius: 4px; }
.fw .fw__head { background: var(--a-blue); color: #fff; font-weight: 700; }
.fw .fw__row  { background: #e3eaf3; font-weight: 700; }
.fw .fw__here { background: var(--a-teal); color: #fff; font-weight: 700; }
@end

@steps: <div class="steps steps--@0"><span class="step">① Start</span><span class="step">② Understand</span><span class="step">③ Try</span><span class="step">④ Check</span><span class="step">⑤ Reflect</span><span class="step">⑥ Look ahead</span></div>
-->

# Nugget 2 · How AI Works

--{{0}}--
Welcome to nugget two. We open the box and look at how AI works, without any mathematics.

<div class="hero">
<div class="hero__kicker">ASSET · AI for Skills, Sustainability and Training · Starter course 2026 · Nugget 2 of 5</div>
<div class="hero__title">How AI Works: <em>data, patterns, predictions</em></div>
<div class="hero__sub">The technical basics every teacher needs, explained with examples from the workshop. No maths, no programming.</div>
<div class="chips">
<span class="chip chip--level">Level: Acquire</span>
<span class="chip">⏱ about 30 minutes</span>
<span class="chip">UNESCO AI CFT: AI foundations and applications</span>
<span class="chip">🌐 works offline</span>
</div>
</div>

**After this nugget you can …**

1. explain how a machine "learns" from examples, using a case from your trade;
2. explain why the quality of data decides the quality of an AI system;
3. describe how a chat assistant produces an answer — and why it can be wrong while sounding certain;
4. use five key terms correctly: *token, training vs. use, context window, hallucination, grounding*.

@steps(0)

<div class="partners">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNESCO-UNEVOC logo">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET project logo">
<span>A UNESCO-UNEVOC Network Coaction Initiative · CC BY-SA 4.0</span>
</div>

# ① Start: Two kinds of AI in Nuwan's workshop

@steps(1)

--{{0}}--
Our case today comes from an automotive workshop in Sri Lanka.

<div class="persona">
<div class="persona__avatar">🔧</div>
<div>
<div class="persona__name">Nuwan · automotive mechatronics instructor, vocational training institute, Sri Lanka</div>

Nuwan's workshop received a **diagnostic tester** that predicts brake wear from
sensor data. It is right most of the time. At the same time, Nuwan's learners
use a **chat assistant** on their phones to explain fault codes.

Last week both got something wrong. The tester flagged a new brake disc as
"worn". The chat assistant explained a fault code confidently — for a different
car manufacturer.

</div>
</div>

<div class="box box--case">
<div class="box__label">Your guess</div>

Why do you think each system made its mistake? Write a first guess — you will
check it at the end.

</div>

[[___ ___]]

# ② Understand: Learning from examples

@steps(2)

--{{0}}--
The central idea of today's AI is simple: it learns from examples instead of following written rules.

Traditional software follows **rules** that a person wrote:
*"If the pad thickness is below 3 mm, show a warning."*

**Machine learning** works the other way round. People collect many
**examples** with the right answer, and the computer finds the pattern itself:

```ascii
  EXAMPLES (training data)          TRAINING              MODEL                 USE
 +---------------------------+                    +-----------------+
 | 5,000 brake measurements  |                    |  learned        |   new car  -->  "worn: 87 %"
 | each labelled by experts  | ---> finds    ---> |  pattern        |
 | "worn" / "not worn"       |      patterns      |  (fixed after   |
 +---------------------------+                    |   training)     |
                                                  +-----------------+
```

- **Training data** — the examples the system learns from.
- **Model** — the learned pattern, stored as many numbers. After training it is fixed.
- **Prediction** — the model's output for a new case, often with a probability.

<div class="box">
<div class="box__label">Key idea</div>

A model can only be as good as its examples. Nuwan's tester had learned from
discs of one supplier. A new disc from another supplier has a different surface
— **a case it had never seen**. It was not "stupid"; it was *out of its experience*.

</div>

## Data decides

--{{0}}--
Because AI learns from data, problems in the data become problems in the AI.

| If the data … | then the AI … | TVET example |
| --- | --- | --- |
| covers only some cases | fails on unfamiliar cases | a weld-inspection camera trained only on steel misjudges aluminium |
| reflects old habits or unfair patterns | repeats them (**bias**) | a career-advice tool trained on past records steers women away from technical trades |
| is mostly in one language or culture | works worse for others | a speech tool understands standard English well but not local accents |
| contains personal information | may reveal or misuse it | learner records uploaded to a public tool |

<div class="box box--warn">
<div class="box__label">Remember</div>

"The computer said so" is not a reason. Ask: **what data was it trained on, and
does my situation fit that data?**

</div>

## From idea to working system

--{{0}}--
Every AI system goes through a life cycle. People make decisions at every step.

```ascii
  1 Define the     2 Collect and     3 Train the     4 Test with      5 Use in       6 Monitor
    problem   --->   prepare data --->  model    ---> new cases  ---> practice ---> and improve
       ^                                                                               |
       +-------------------------------------------------------------------------------+
```

Teachers are involved more often than they think: when an institution **chooses**
a system (step 1 and 4), when learners' data is **collected** (step 2), and when
someone notices that the system gets things wrong in practice (step 6).

## How a chat assistant writes

--{{0}}--
Chat assistants are built on so-called large language models. Here is what they actually do.

A chat assistant is built on a **large language model (LLM)**. It was trained
on huge amounts of text with one simple task: **predict the next piece of text**.

```text
  "Before working on a circuit, always switch off the ..."

   next piece?      power   ██████████████████  62 %
                    supply  ██████             18 %
                    machine ███                 7 %
                    light   █                   2 %
```

It picks a likely continuation, adds it, and repeats — piece by piece — until
the answer is complete. These pieces are called **tokens** (a word or part of a
word).

<div class="cards">
<div class="card"><div class="card__title">Probable ≠ true</div>The model produces what <em>sounds</em> likely. Usually that is also correct — but the model cannot tell the difference.</div>
<div class="card"><div class="card__title">No look-up</div>A plain model does not search a book or the internet. Some assistants add a search step; then check which sources were used.</div>
<div class="card"><div class="card__title">Varies each time</div>Ask the same question twice and you may get two different answers. There is some randomness in the choice.</div>
</div>

## Five terms that prevent mistakes

--{{0}}--
Five terms help you avoid the most common misunderstandings.

| Term | What it means | The mistake it prevents |
| --- | --- | --- |
| **Token** | the piece of text a model works with; about ¾ of an English word, often more pieces for other languages | assuming all languages work equally well — many languages need more tokens and get weaker results |
| **Training vs. use** | the model is fixed after training; your chat does **not** change it | believing that correcting the AI once "teaches" it for next time |
| **Context window** | the maximum amount of text the model can consider at once | pasting a 90-page document and assuming the answer covers all of it |
| **Hallucination** | fluent output that is not supported by any source | taking a well-written answer as a checked fact |
| **Grounding** | giving the model the source text and asking it to use only that | expecting correct local rules the model never saw |

<div class="box">
<div class="box__label">Back to Nuwan</div>

The chat assistant had never been given the manual for the learners' car. It
produced the most *probable* explanation of the fault code — from the texts it
was trained on, which were mostly about other manufacturers. That is a
**hallucination**. Pasting the relevant page of the right manual (**grounding**)
would have helped.

</div>

<details>
<summary><strong>Read more: "But the assistant remembered what I said last week!"</strong></summary>

Some assistants have a *memory* feature. The model itself still does not change:
the software stores notes about you and **pastes them back into the input** of
every new conversation. Everything an assistant seems to "know" about you or your
documents is text that software around the model puts into the input. This
matters for privacy: what is stored can be read again. Nugget 4 comes back to this
idea, because it is the basis of today's AI agents.

</details>

# ③ Try: Three small experiments

@steps(3)

--{{0}}--
Three experiments of about three minutes each. Each one shows one of the terms from the table.

<div class="box box--try">
<div class="box__label">Experiment A · Same question, different answers</div>

Ask a chat assistant the same question **three times in new chats**, for example:
*"Give me one example of a common mistake apprentices make in [your trade]."*
Compare the answers.

</div>

<div class="box box--try">
<div class="box__label">Experiment B · Ask for sources</div>

Ask: *"Name two books or official documents about safety in [your trade], with
author and year."* Then check whether they exist (library catalogue, publisher
website, search engine).

</div>

<div class="box box--try">
<div class="box__label">Experiment C · Grounding</div>

Copy a short paragraph from a document you know well (a work instruction, a
curriculum text). Ask a question about it **once without** and **once with** the
paragraph pasted in, adding: *"Answer only from the text above."* Compare.

</div>

<details>
<summary><strong>No AI access? Typical results</strong></summary>

- **A:** The three answers name different mistakes and use different wording.
  Useful for ideas — not reliable when you need the *same* result twice, for
  example when you mark work.
- **B:** Often one reference is real and one is invented, or author and year do
  not match. Invented references look completely normal.
- **C:** Without the text, the answer is general and may contradict your
  document. With the text and the instruction, it usually sticks to the
  document — but still check it.

</details>

**Which experiment surprised you most?**

[(A)] A · different answers each time
[(B)] B · invented or wrong sources
[(C)] C · the effect of grounding
[(D)] None — I expected all of it

# ④ Check

@steps(4)

--{{0}}--
Five questions to check your understanding.

**1. What does "training data" mean?**

[( )] The rules a programmer writes for the AI
[(X)] The examples an AI system learns its patterns from
[( )] The data a teacher enters in a chat
[( )] The test the AI has to pass before it is sold
************************************************
Training data are the examples. The model is the pattern learned from them.
************************************************

**2. A weld-inspection camera was trained only with pictures of steel welds. What is most likely to happen with aluminium welds?**

[( )] It works equally well, because a weld is a weld
[(X)] It makes more mistakes, because aluminium welds were not in its training data
[( )] It refuses to work
************************************************
AI systems are weakest where their situation differs from their training data.
************************************************

**3. You corrected a chat assistant's wrong answer yesterday. Today, in a new chat, it makes the same mistake. Why?**

[( )] The assistant is broken
[(X)] The model is fixed after training; a correction in a chat does not change it
[( )] Someone else changed the model overnight
************************************************
Using a model does not train it. If you want a rule to be followed every time,
you have to give it again — or store it as a standing instruction (see Nugget 4).
************************************************

**4. Fill the gap:** Fluent AI output that is not supported by any source is called a [[hallucination]].
[[?]] It begins with "h".
************************************************
The model does not lie — it has no idea of truth. It produces probable text.
************************************************

**5. Which measures reduce the risk of wrong answers? (choose all that apply)**

[[X]] Giving the AI the relevant source text and asking it to use only that
[[X]] Checking important facts against a reliable source
[[ ]] Asking the AI whether it is sure
[[X]] Asking an expert colleague
************************************************
Asking the AI "Are you sure?" is not an independent check: models tend to agree
with the user and may simply change their answer. Use sources and people.
************************************************

# ⑤ Reflect and transfer

@steps(5)

--{{0}}--
How do you explain all this to your learners? Here is an activity that works without any technology.

<div class="box box--class">
<div class="box__label">In your classroom · "Be the model" (unplugged, 15 minutes)</div>

1. Write the beginning of a sentence from your trade on the board, for example
   *"Before you start the lathe, always …"*.
2. Each learner writes the **most likely next word** on a card. Collect and count.
3. Continue with the most frequent word — and repeat three or four times.
4. Discuss: *Is the resulting sentence correct? Would a different group have
   written the same? What would happen if nobody in the group knew the rule?*

Learners experience that a text can be **probable without being checked** —
which is exactly how a language model works.

</div>

**Learning journal**

Look at your guess from the start. What would you now say caused each of the two mistakes in Nuwan's workshop?

[[___ ___ ___]]

Which one term from this nugget would you most like your learners to understand, and why?

[[___ ___]]

# ⑥ Look ahead

@steps(6)

--{{0}}--
Here is the summary of this nugget and a look at what comes next.

<div class="takeaways">

**Take-aways**

- Machine learning means finding patterns in **examples** — the model is only as good as its data.
- Bias, gaps and personal information in the data become problems in the AI.
- A chat assistant predicts **probable** text piece by piece; probable is not the same as true.
- The model does not learn from your chat. What seems like memory is text put back into the input.
- **Grounding** — giving the source and asking to use only it — makes answers more reliable, but not perfect.

</div>

<div class="box box--ahead">
<div class="box__label">Next: Nugget 3 · AI Tools for Teaching</div>

Now that you know how the systems work, the next nugget looks at the tools
themselves: what they are good for in preparation, in class, in assessment and
in administration — and where your data goes when you use them.

</div>

## Sources and further reading

- UNESCO (2024). *AI competency framework for teachers*, aspect "AI foundations and applications".
  https://www.unesco.org/en/articles/ai-competency-framework-teachers
- Elements of AI — free online course by the University of Helsinki and MinnaLearn,
  available in many languages. https://www.elementsofai.com
- UNESCO (2023). *Guidance for generative AI in education and research.*
  https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research
- ASSET deeper nugget on this aspect: *LO 3.1.1 AI Foundations and Applications.*

*CC BY-SA 4.0 · ASSET project · contact: hannes.tegelbeckers@ovgu.de*
