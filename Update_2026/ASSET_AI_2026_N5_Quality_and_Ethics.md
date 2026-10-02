<!--
author:   Hannes Tegelbeckers · OVGU Magdeburg · ASSET project (UNESCO-UNEVOC Network)
email:    hannes.tegelbeckers@ovgu.de
version:  2026.1.0
language: en
narrator: UK English Female
license:  CC BY-SA 4.0
comment:  ASSET AI starter course 2026, Nugget 5 of 5 (Quality and Ethics): failure modes, the F-A-C-T-S check, four ethical lenses, AI detectors, class rules, next steps. Acquire level.

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

# Nugget 5 · Quality and Ethics

--{{0}}--
Welcome to the last nugget of the starter course. Today is about using AI responsibly: checking what it produces, protecting learners, and deciding well.

<div class="hero">
<div class="hero__kicker">ASSET · AI for Skills, Sustainability and Training · Starter course 2026 · Nugget 5 of 5</div>
<div class="hero__title">Quality and Ethics: <em>check, protect, decide</em></div>
<div class="hero__sub">A checking routine for AI output, four ethical lenses for TVET, fair rules for learners — and your personal next steps.</div>
<div class="chips">
<span class="chip chip--level">Level: Acquire</span>
<span class="chip">⏱ about 35 minutes</span>
<span class="chip">UNESCO AI CFT: ethics of AI · human-centred mindset · professional development</span>
<span class="chip">🌐 works offline</span>
</div>
</div>

**After this nugget you can …**

1. name typical ways in which AI output fails, including those you cannot see in a single answer;
2. check AI-generated teaching material with the **F·A·C·T·S** routine;
3. analyse an AI use in TVET through four ethical lenses;
4. explain why AI detectors must not be used as evidence against learners;
5. agree on clear, fair AI rules with your learners and plan your next steps.

@steps(0)

<div class="partners">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNESCO-UNEVOC logo">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET project logo">
<span>A UNESCO-UNEVOC Network Coaction Initiative · CC BY-SA 4.0</span>
</div>

# ① Start: Two uncomfortable moments

@steps(1)

--{{0}}--
Two situations from the training centres we already know.

<div class="cards">
<div class="card card--amber"><div class="card__title">Jonas, Germany</div>A colleague gives Jonas an AI-generated worksheet on angle grinder safety: "Looks great, just print it." Jonas reads it the evening before class and finds a rule that could cause a serious accident.</div>
<div class="card card--amber"><div class="card__title">Anjali, Mauritius</div>An online "AI detector" says a learner's written assignment is "87 % AI-generated". The learner, who writes in English as a third language, says: "I wrote it myself." The head of department asks Anjali to fail the assignment.</div>
</div>

<div class="box box--case">
<div class="box__label">Your first reaction</div>

What should Anjali do?

</div>

[(1)] Fail the assignment — the detector is clear
[(2)] Ask the learner to talk about the assignment and show drafts or notes
[(3)] Run the text through a second detector
[(4)] Accept the assignment without further questions
[(5)] I don't know yet

# ② Understand: How AI output fails

@steps(2)

--{{0}}--
Some AI errors are easy to spot. Others are invisible in a single answer and only show up over time.

Some failures can be found by **checking one answer** against a source. Others
**do not show in a single answer** — they affect the person using the AI, or a
whole group of learners.

| Failure | In one sentence | Visible in one answer? |
| --- | --- | --- |
| **Fabrication** | plausible but false facts, numbers or sources | yes — check against a source |
| **Local mismatch** | correct somewhere, but not under your country's rules or your workplace's standards | yes — if you know the local rules |
| **Bias and stereotypes** | who appears as the expert, the worker, the customer — and who does not | often only across many texts |
| **Agreeing with you** | the AI confirms what you suggest, even when you are wrong | no |
| **Checking fatigue** | after many good answers, people stop checking carefully | no |
| **Sameness** | thirty learners' texts share the same structure and examples | only across a set |
| **Learning stall** | the effortful part is skipped; the gap shows later, at the machine | no — visible later |

<div class="box box--warn">
<div class="box__label">In TVET, errors can hurt people</div>

In workshops, kitchens, construction sites and care settings, a wrong rule is
not just a wrong answer: it can cause **injury**. Safety-critical content from AI
must always be checked against the official regulation, standard or
manufacturer's manual.

</div>

## The F·A·C·T·S routine

--{{0}}--
Here is a simple routine to check any AI-generated teaching material before you use it.

Before you use AI-generated material, check the **F·A·C·T·S**:

<div class="cards">
<div class="card"><div class="card__title">F · Facts and figures</div>Every number, value, name and rule checked against a reliable source.</div>
<div class="card card--green"><div class="card__title">A · Audience fit</div>Right level, language and examples for <em>these</em> learners?</div>
<div class="card card--amber"><div class="card__title">C · Complete and current</div>Are important steps missing? Does it follow <em>current, local</em> regulations?</div>
<div class="card card--violet"><div class="card__title">T · Tone and fairness</div>Inclusive language? Who is shown as competent? Any stereotypes?</div>
<div class="card card--red"><div class="card__title">S · Safety and sources</div>Safety steps correct and complete? Do the cited sources exist and say this?</div>
</div>

The routine takes a few minutes. It also protects **you**: you remain responsible
for every material you hand out, whoever drafted it.

## Four ethical lenses

--{{0}}--
Ethical questions about AI in TVET can be examined through four lenses.

Look at any AI use in your institution through four lenses:

<div class="cards">
<div class="card card--teal"><div class="card__title">👤 Human agency</div>Do teachers and learners keep control? Can decisions be explained and contested?</div>
<div class="card card--teal"><div class="card__title">🔒 Privacy</div>What data is collected, why, for how long, and who can see it? Were learners informed?</div>
<div class="card card--teal"><div class="card__title">🦺 Safety and security</div>Is the system reliable enough for this purpose? What happens when it fails?</div>
<div class="card card--teal"><div class="card__title">🌍 Fairness and cultural relevance</div>Does it work equally well for all learners — languages, cultures, genders, disabilities?</div>
</div>

<div class="box box--case">
<div class="box__label">Example: a skills-assessment camera</div>

A training centre uses a camera system to assess learners' precision in CNC
machining. It turns out that the system rates learners with a hand tremor as
"less skilled", even when their finished parts are within tolerance, and that
learners feel watched and stop trying new approaches.

- **Human agency:** instructors feel pressured to accept the scores.
- **Privacy:** constant video recording of learners.
- **Safety:** unclear how reliable the scores are.
- **Fairness:** learners with a medical condition are disadvantaged.

</div>

## Honest and fair rules

--{{0}}--
Now to Anjali's situation: AI detectors, transparency, and fair rules.

**AI detectors are not evidence.** Studies show that tools claiming to detect
AI-written text are unreliable, can be tricked easily, and misjudge texts by
people writing in a second or third language more often than texts by native
speakers. A detector score **must never be the only reason** for an accusation or
a grade.

What works better:

- **Talk to the learner** about the content: *"Explain this paragraph to me."*
- Ask for **drafts, notes or the process**, not only the product.
- Design assessment so that the key competence is shown **in practice or orally**.
- Agree on **clear rules in advance**, so learners know what is allowed.

<div class="cards">
<div class="card card--green"><div class="card__title">🟢 Allowed</div>e.g. checking spelling, translating instructions, getting ideas for a topic</div>
<div class="card card--amber"><div class="card__title">🟠 Allowed if stated</div>e.g. improving the structure of a text, getting feedback on a draft — say how you used it</div>
<div class="card card--red"><div class="card__title">🔴 Not allowed</div>e.g. letting AI write the technical justification that is being assessed</div>
</div>

**Be transparent yourself.** If you use AI to prepare materials or feedback,
say so. Learners learn honest AI use from your example.

<details>
<summary><strong>Read more: laws, policies and sustainability</strong></summary>

- **Institutional policy first.** Check whether your school or company has an AI
  policy and a list of approved tools.
- **Data protection law** applies whenever personal data is processed.
- **In the EU**, the AI Act requires AI literacy of staff who use AI (Article 4),
  prohibits emotion recognition in education institutions (Article 5), and
  classifies AI used for admission, for evaluating learning outcomes and for
  monitoring learners during tests as **high-risk** (Annex III), with strict
  obligations for providers and users. The rules apply in phases; check the
  current state.
- **Sustainability.** Running AI uses electricity and water in data centres. A
  single text request uses little, but images, video and very frequent use add
  up. Use AI where it adds real value — this fits the ASSET idea of *skills for
  sustainability*.

</details>

# ③ Try: Check a worksheet

@steps(3)

--{{0}}--
This task needs no AI tool. Check the worksheet with the F·A·C·T·S routine.

<div class="box box--try">
<div class="box__label">Task · 10 minutes — no AI tool needed</div>

This is the worksheet Jonas received. It was generated by AI. Check it with
**F·A·C·T·S** and find **four problems**. Even if you do not work with metal,
you will find at least three.

</div>

<div style="background:#fff;color:#1f2933;border:1px dashed #9aa5b1;border-radius:8px;padding:1rem 1.2rem;margin:1rem 0;">

**Worksheet: Working safely with an angle grinder**

1. Always wear safety glasses or a face shield and hearing protection.
2. Unplug the grinder or remove the battery before changing a disc.
3. Check that the maximum speed printed on the disc is **lower** than the speed of the grinder.
4. When cutting thick material, **remove the guard** for better visibility.
5. According to ISO 12100:2019, section 4.7, apprentices under 18 may not use angle grinders.
6. Let the disc stop completely before putting the grinder down.
7. Every apprentice should ask his supervisor if he is unsure.

</div>

**Which numbered points are problematic?** (choose all that apply)

[[ ]] 1
[[ ]] 2
[[X]] 3
[[X]] 4
[[X]] 5
[[ ]] 6
[[X]] 7
************************************************
- **3 — Facts (dangerous):** the reverse is correct. The maximum speed of the disc
  must be **equal to or higher** than the speed of the grinder, otherwise the disc
  can burst.
- **4 — Safety (dangerous):** the guard must **never** be removed. It protects
  against disc fragments.
- **5 — Sources (fabrication):** ISO 12100 is a general standard on machine safety
  and risk assessment; it contains no such age rule, and the cited section is
  invented. Rules for young workers come from national law and workplace risk
  assessments.
- **7 — Tone and fairness:** "his … he" presents apprentices as male. Better:
  *"Ask your supervisor if you are unsure."*

Points 1, 2 and 6 are correct. Notice that the dangerous errors sound just as
confident as the correct rules.
************************************************

## Judge the situations

--{{0}}--
Now judge five situations. Use the four ethical lenses.

Decide for each situation: **acceptable**, **acceptable with conditions**, or **not acceptable**.

[(acceptable) (with conditions) (not acceptable)]
[ ( ) (X) ( ) ] A teacher uses a chat assistant to draft quiz questions and checks them before use.
[ ( ) ( ) (X) ] A camera system detects learners' emotions to measure their motivation in class.
[ ( ) (X) ( ) ] Learners use a translation tool to understand instructions in a second language.
[ ( ) ( ) (X) ] A learner is failed because an AI detector scored the text as "AI-written".
[ ( ) (X) ( ) ] An AI tool suggests feedback on anonymised learner texts; the teacher edits and signs it.
************************************************
- **Quiz drafts:** fine — with the F·A·C·T·S check.
- **Emotion detection:** a serious intrusion into privacy and dignity, scientifically
  doubtful, and prohibited in education institutions in the EU.
- **Translation:** supports inclusion — with a check of technical terms, and not in
  an assessment of language skills.
- **Detector as evidence:** unreliable and unfair, especially for multilingual learners.
- **Feedback suggestions:** fine if the data is anonymised, the tool is approved and
  the teacher decides.
************************************************

# ④ Check

@steps(4)

--{{0}}--
Five final questions.

**1. Which failure can you NOT detect by checking a single AI answer?**

[( )] An invented source
[( )] A wrong number
[(X)] Your own checking becoming less careful after many good answers
************************************************
Checking fatigue is about the person, not the answer. Countermeasures are
procedures: checklists, a second reader, sources outside the conversation.
************************************************

**2. What does the "C" in F·A·C·T·S stand for?**

[( )] Creative and clear
[(X)] Complete and current
[( )] Copyright and cost
************************************************
Complete (no missing steps) and current (the valid, local version of a rule).
************************************************

**3. An AI detector says a text is "90 % AI-generated". What is the appropriate response?**

[( )] Fail the assignment
[(X)] Treat it as, at most, a reason for a conversation about the content and the process
[( )] Use a second detector to confirm
************************************************
Detectors are unreliable and biased against second-language writers. Evidence
comes from talking with the learner and from the work process.
************************************************

**4. Which of these belong to the four ethical lenses in this nugget? (choose all that apply)**

[[X]] Human agency
[[X]] Privacy
[[ ]] Speed
[[X]] Safety and security
[[X]] Fairness and cultural relevance
************************************************
Speed may be a benefit, but it is not an ethical lens.
************************************************

**5. Who is responsible for a worksheet that was drafted by AI and handed out by a teacher?**

[( )] The AI provider
[( )] Nobody, if the AI made the error
[(X)] The teacher who handed it out
************************************************
AI can draft; the person who uses the material is responsible for it.
************************************************

# ⑤ Reflect and plan

@steps(5)

--{{0}}--
You have reached the end of the starter course. Let us turn what you learned into action.

<div class="box box--class">
<div class="box__label">In your classroom · "Our AI agreement" (30 minutes)</div>

Create your class's AI rules **together with your learners**, using the three
colours: 🟢 allowed, 🟠 allowed if stated, 🔴 not allowed. Start from real tasks
of the course. Write the agreement on one page, hang it up, and review it after
a few weeks. Learners who help make the rules understand — and keep — them better.

</div>

**Learning journal**

Back to Anjali: what would you now advise, and why?

[[___ ___ ___]]

**My next 30 days** — three small, concrete steps (for example: *"Build a prompt library with five prompts for my module"*, *"Discuss an AI agreement with my class"*, *"Ask which AI tools my institution has approved"*):

Step 1

[[___]]

Step 2

[[___]]

Step 3

[[___]]

With whom will I share what I learned? (a colleague, my team, a network)

[[___]]

# ⑥ Look ahead: What's next

@steps(6)

--{{0}}--
Congratulations on completing the starter course. Here is a summary and your options for going further.

<div class="takeaways">

**Take-aways**

- Some AI failures show in one answer (fabrication, local mismatch); others only over time (bias, agreeing with you, checking fatigue, learning stall).
- Check every AI-generated material with **F·A·C·T·S** — especially safety-critical content.
- Look at AI uses through four lenses: **human agency, privacy, safety and security, fairness**.
- AI detectors are **not evidence**. Talk with learners, look at the process, design assessment for visible competence.
- Agree on clear rules with learners, and be transparent about your own AI use.
- You remain responsible for what you use and hand out.

</div>

<div class="box box--ahead">
<div class="box__label">You completed the ASSET starter course 🎉</div>

You worked on the **Acquire** level in all five aspects of the UNESCO AI
Competency Framework for Teachers. To go further (**Deepen**):

- the ASSET learning objectives **LO 1.1.1 – LO 5.1.1** — one deeper nugget per aspect;
- the GitHub and LiaScript nuggets of the ASSET series — to create and share your own open learning materials;
- *AI in Teaching: Tools, Strategies and Reflection* — the five stages of prompting, with lab exercises.

</div>

**How useful was this starter course for your work?**

[(1)] Not useful
[(2)] A little useful
[(3)] Useful
[(4)] Very useful

**What should we improve?**

[[___ ___]]

## Sources and further reading

- UNESCO (2024). *AI competency framework for teachers*, aspect "Ethics of AI".
  https://www.unesco.org/en/articles/ai-competency-framework-teachers
- UNESCO (2021). *Recommendation on the Ethics of Artificial Intelligence.*
  https://www.unesco.org/en/artificial-intelligence/recommendation-ethics
- Weber-Wulff, D. et al. (2023). Testing of detection tools for AI-generated text.
  *International Journal for Educational Integrity*, 19, 26.
  https://doi.org/10.1007/s40979-023-00146-z
- Liang, W., Yuksekgonul, M., Mao, Y., Wu, E., & Zou, J. (2023). GPT detectors are
  biased against non-native English writers. *Patterns*, 4(7).
  https://doi.org/10.1016/j.patter.2023.100779
- European Union (2024). *Regulation (EU) 2024/1689 (AI Act).*
  https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- ASSET deeper nuggets: *LO 2.1.1 Ethics of AI in TVET* · *LO 5.1.1 AI for Professional Development.*

**Contact:** Hannes Tegelbeckers, Otto von Guericke University Magdeburg ·
hannes.tegelbeckers@ovgu.de

*This course is licensed under CC BY-SA 4.0. You may adapt and translate it for
your context; please name the ASSET project.*
