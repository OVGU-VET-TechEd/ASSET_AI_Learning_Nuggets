<!--
author:   Hannes Tegelbeckers · OVGU Magdeburg · ASSET project (UNESCO-UNEVOC Network)
email:    hannes.tegelbeckers@ovgu.de
version:  2026.1.0
language: en
narrator: UK English Female
license:  CC BY-SA 4.0
comment:  ASSET AI starter course 2026, Nugget 3 of 5 (Tools): tool families, four areas of use in TVET, data routes, a five-question tool check. Acquire level.

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

# Nugget 3 · AI Tools for Teaching

--{{0}}--
Welcome to nugget three. Today we look at AI tools for everyday teaching, and at how to choose them wisely.

<div class="hero">
<div class="hero__kicker">ASSET · AI for Skills, Sustainability and Training · Starter course 2026 · Nugget 3 of 5</div>
<div class="hero__title">AI Tools for Teaching: <em>what, where, and who thinks</em></div>
<div class="hero__sub">An overview of tool types, four areas of use in TVET, and a five-question check before you use a tool.</div>
<div class="chips">
<span class="chip chip--level">Level: Acquire</span>
<span class="chip">⏱ about 30 minutes</span>
<span class="chip">UNESCO AI CFT: AI foundations and applications · AI pedagogy</span>
<span class="chip">🌐 works offline</span>
</div>
</div>

**After this nugget you can …**

1. name the main families of AI tools and give a teaching example for each;
2. give examples of AI use in preparation, in class, in assessment and in administration;
3. explain where your text goes when you use a tool, and what that means for learners' data;
4. check a tool with five questions before using it;
5. decide whether an AI use helps learners think — or does the thinking for them.

@steps(0)

<div class="partners">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNESCO-UNEVOC logo">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET project logo">
<span>A UNESCO-UNEVOC Network Coaction Initiative · CC BY-SA 4.0</span>
</div>

# ① Start: Anjali has 40 minutes

@steps(1)

--{{0}}--
Our case today comes from a culinary arts training centre in Mauritius.

<div class="persona">
<div class="persona__avatar">🍲</div>
<div>
<div class="persona__name">Anjali · culinary arts trainer, hospitality training centre, Mauritius</div>

Tomorrow Anjali teaches **food safety and safe cooling of cooked food** to a new
group. Some learners read fluently in English, some prefer French or Mauritian
Creole, and two have reading difficulties. Anjali has 40 minutes to prepare.

A colleague says: *"Just let the AI do it — worksheet, quiz, translation, done in
five minutes."* Another colleague says: *"Never put anything about our learners
into those tools."*

</div>
</div>

<div class="box box--case">
<div class="box__label">Your view</div>

Which parts of Anjali's preparation would you give to an AI tool, and which not?

</div>

[[draft]] Drafting a worksheet on safe cooling
[[translate]] Translating the worksheet into French
[[simplify]] Creating a simpler version for learners with reading difficulties
[[quiz]] Writing quiz questions
[[classlist]] Uploading the class list to create personalised tasks
[[factcheck]] Checking that the temperatures and times are correct

<details>
<summary><strong>A first hint</strong></summary>

There is no single right answer — this is about your first judgement. By the end
of the nugget you will have a checklist to decide. Two points in advance:
uploading a class list sends **personal data** to a tool, and **checking**
food-safety values is exactly the part that must stay with the expert.

</details>

# ② Understand: Families of AI tools

@steps(2)

--{{0}}--
There are thousands of AI tools, but most of them belong to a few families.

Tool names change every few months — the families stay. Learn the families,
then look at the tools available in your institution.

<div class="cards">
<div class="card"><div class="card__title">💬 Chat assistants</div>General-purpose: explain, draft, summarise, brainstorm, translate. <br><em>Examples (2026): ChatGPT, Claude, Gemini, Microsoft Copilot, Le Chat; open models you can run locally.</em></div>
<div class="card card--green"><div class="card__title">🖼 Media creation</div>Images, diagrams, slides, audio (text-to-speech), video, subtitles. Useful for accessible materials.</div>
<div class="card card--amber"><div class="card__title">🌍 Language tools</div>Translation, simplified language, reading aloud, speech-to-text. Important for multilingual groups.</div>
<div class="card card--violet"><div class="card__title">📝 Assessment helpers</div>Quiz generators, rubric drafts, feedback suggestions. Always teacher-checked.</div>
<div class="card card--teal"><div class="card__title">🛠 TVET-specific systems</div>Simulators, virtual and augmented reality, diagnostic and inspection systems, often built into machines.</div>
<div class="card card--indigo"><div class="card__title">🔗 Built-in AI</div>AI features inside tools you already use: office software, learning platforms, search engines, phones.</div>
</div>

<div class="box">
<div class="box__label">Good news for low-resource settings</div>

Many useful things work on a basic smartphone, and some open models can run on
an ordinary laptop **without internet**. You do not need the newest tool to use AI
well — you need clear goals and a good checking routine.

</div>

## Four areas of use in TVET

--{{0}}--
Teachers use AI in four areas. The benefit and the risk are different in each.

| Area | Useful for … | Watch out for … |
| --- | --- | --- |
| **Preparation** | first drafts of worksheets, examples, case stories, differentiated versions, translations, quiz ideas | factual errors in technical and safety content; generic content that ignores local standards |
| **In class** | explaining a concept in other words, role-play partners (e.g. a difficult customer), language support, feedback on drafts | learners skipping the effortful part; unequal access to devices and accounts |
| **Assessment** | question banks, rubric drafts, feedback suggestions for the teacher to review | grades decided by AI; unreliable "AI detectors"; results that cannot be reproduced |
| **Administration** | emails, schedules, meeting notes, reports | personal data of learners and colleagues in external tools |

<div class="box box--warn">
<div class="box__label">Two firm rules for beginners</div>

1. **No personal data** of learners (names, grades, health, photos) in tools your
   institution has not approved.
2. **No grade, admission or safety decision** is made by an AI tool alone.

</div>

## Where does my text go?

--{{0}}--
When you type into an AI tool, your text is processed somewhere. Where exactly makes a big difference.

```ascii
                         your prompt
                              |
        +---------------------+----------------------+
        |                     |                      |
        v                     v                      v
 +--------------+    +------------------+    +-------------------+
 | YOUR DEVICE  |    | YOUR INSTITUTION |    | EXTERNAL PROVIDER |
 | local model  |    | approved server  |    | public web tool   |
 +--------------+    +------------------+    +-------------------+
   text stays          contract and           text leaves; terms
   with you            rules apply            of the provider apply
```

- **Your device:** most private; needs a capable computer; results may be weaker.
- **Your institution:** a tool licensed by your school or company, with a data
  protection agreement. Usually the best choice for work with learners.
- **External provider:** convenient and powerful; read the terms. Free versions
  may use your input to improve their products.

<details>
<summary><strong>Read more: rules and laws</strong></summary>

Data protection law applies everywhere personal data is processed — for
example the GDPR in the European Union, or national data protection acts in
Sri Lanka and Mauritius. In the EU, the **AI Act** also requires organisations
that use AI to ensure their staff have sufficient **AI literacy** (Article 4,
applicable since February 2025), prohibits AI that recognises emotions in
education institutions, and treats AI that evaluates learning outcomes or
decides on admission as **high-risk**. Outside the EU, check your national rules
and your institution's AI policy. Nugget 5 returns to these questions.

</details>

## Who does the thinking?

--{{0}}--
The most important pedagogical question about any AI use is: who does the thinking?

Learning in a trade needs **practice**: making the diagnosis, planning the steps,
writing the justification. When AI does these parts, learners hand in finished
work **without having learned** the skill — and it shows later, at the machine or
in the exam.

<div class="cards">
<div class="card card--red"><div class="card__title">AI replaces thinking</div>"Write my report on the pump repair." <br>"Solve this calculation." <br>"Tell me what the fault is."</div>
<div class="card card--green"><div class="card__title">AI supports thinking</div>"Ask me questions that help me find the fault myself." <br>"Check my calculation steps and tell me where the first error is — but not the answer." <br>"Play a customer who complains about the repair."</div>
</div>

A study of an AI tutor in physics found **higher learning gains** than in active
classroom learning — but the tutor was *designed* to guide students through their
own steps, with checked solutions in the background (Kestin et al., 2025).
Unguided chatbot use tends to have the opposite effect. **The design decides.**

## The five-question tool check

--{{0}}--
Before you use a tool with learners, ask five questions. This takes two minutes.

<div class="cards">
<div class="card"><div class="card__title">1 · Purpose</div>What learning or work problem does it solve? Would a simpler solution do?</div>
<div class="card card--amber"><div class="card__title">2 · Data</div>What goes in, where is it processed, and is the tool approved for that data?</div>
<div class="card card--green"><div class="card__title">3 · Access</div>Can all learners use it — cost, device, bandwidth, language, disability?</div>
<div class="card card--violet"><div class="card__title">4 · Quality</div>How will I check the output? Who is responsible if it is wrong?</div>
<div class="card card--teal"><div class="card__title">5 · Learning</div>Who does the thinking — the learner or the tool?</div>
</div>

If you cannot answer one of the questions, **do not use the tool with learners
yet** — try it for your own preparation first, or ask your institution.

# ③ Try: Prepare Anjali's lesson

@steps(3)

--{{0}}--
Now help Anjali. The task takes about ten minutes.

<div class="box box--try">
<div class="box__label">Task · 10 minutes</div>

1. Ask a chat assistant for a **one-page worksheet** for your own trade, or use
   Anjali's topic:
   > *Create a one-page worksheet for first-year culinary learners on safe cooling
   > of cooked food. Include three short questions. Use simple English.*
2. Ask for a **simpler version** for learners with reading difficulties.
3. Mark every **fact, number and rule** in the result that you would have to check.
4. Run the **five-question check** below for the tool you used.

</div>

<details>
<summary><strong>No AI access? Example worksheet extract</strong></summary>

> **Safe cooling of cooked food**
> Bacteria grow fastest between 5 °C and 60 °C (the "danger zone").
> Cool cooked food from 60 °C to 21 °C within 2 hours, and to 5 °C within the next 4 hours.
> Divide large amounts into shallow containers. Do not leave food out overnight to cool.
>
> 1. What is the "danger zone"? 2. Why use shallow containers? 3. …

*Expert view:* The structure is useful and the language is clear. **But:** the
temperature limits and times differ between countries and food-safety
standards; the figures shown follow one common rule, not necessarily the one
Anjali's learners will be assessed on. These values must be checked against the
**local regulation or HACCP plan** before use.

</details>

**My five-question check for the tool I used:**

1 · Purpose — what did it help me with?

[[___]]

2 · Data — what did I enter, and where was it processed?

[[___]]

3 · Access — could all my learners use it?

[[___]]

4 · Quality — what did I have to check, and how?

[[___]]

5 · Learning — if learners used it, who would do the thinking?

[[___]]

# ④ Check

@steps(4)

--{{0}}--
Five questions. Read the explanation after each one.

**1. Anjali wants to create personalised exercises. Which approach respects learners' data?**

[( )] Upload the class list with names and grades to a free chat assistant
[(X)] Describe the group in general terms ("three learners need simpler language") without names
[( )] Paste each learner's last test into a public tool
************************************************
You can get differentiated material without any personal data. Describe needs,
not people.
************************************************

**2. Match the area of use.** Which area does each activity belong to?

[(Preparation) (In class) (Assessment) (Administration)]
[ (X) ( ) ( ) ( ) ] Drafting a differentiated worksheet
[ ( ) (X) ( ) ( ) ] Learners practise a customer conversation with an AI role-play
[ ( ) ( ) (X) ( ) ] Generating a question bank for a written test
[ ( ) ( ) ( ) (X) ] Summarising the minutes of a team meeting

**3. Which prompt supports the learner's own thinking?**

[( )] "Write the repair report for this pump."
[(X)] "Ask me three questions that help me find the cause of the fault myself."
[( )] "Give me the correct answer to question 4."
************************************************
Tools that *ask* rather than *answer* keep the effortful part with the learner.
************************************************

**4. Which statements about where text is processed are correct? (choose all that apply)**

[[X]] A local model on your own device keeps the text on that device
[[X]] A tool approved by your institution usually comes with a data protection agreement
[[ ]] Free public tools never store or use what you type
[[X]] Terms of use of external providers decide what happens with your input
************************************************
Always check the terms. Free versions often allow the provider to use inputs.
************************************************

**5. According to the five-question check, what should you do if you cannot answer one of the questions?**

[( )] Use the tool anyway, but carefully
[(X)] Not use it with learners yet: try it yourself first or ask your institution
[( )] Ask the AI tool to answer the question
************************************************
The check is a stop sign, not a formality.
************************************************

# ⑤ Reflect and transfer

@steps(5)

--{{0}}--
Let us bring the ideas back to your own teaching.

<div class="box box--class">
<div class="box__label">In your classroom · "Tool detectives" (20 minutes)</div>

Give small groups one AI tool each (or a screenshot of it). Each group applies
the **five-question check** and presents a one-minute verdict: *use it / use it
with conditions / do not use it*. Learners practise the same critical judgement
they will need at work — and you learn which tools they already use.

</div>

**Learning journal**

Anjali's colleague said: *"Just let the AI do it."* The other said: *"Never put anything into those tools."* Write your own position in two or three sentences.

[[___ ___ ___]]

One task in my next teaching week where an AI tool could **support** my learners' thinking:

[[___ ___]]

# ⑥ Look ahead

@steps(6)

--{{0}}--
Here is the summary of this nugget and a look at what comes next.

<div class="takeaways">

**Take-aways**

- Learn tool **families**, not tool names: chat, media, language, assessment, TVET-specific, built-in.
- Four areas of use — preparation, in class, assessment, administration — each with its own risks.
- Know **where your text goes**: your device, your institution, or an external provider.
- Two firm rules: no learners' personal data in unapproved tools; no grade, admission or safety decision by AI alone.
- Ask before every use: **who does the thinking?**
- The **five-question check**: purpose · data · access · quality · learning.

</div>

<div class="box box--ahead">
<div class="box__label">Next: Nugget 4 · Prompting</div>

The worksheet was useful but generic. How do you ask so that you get what you
actually need — for your trade, your learners, your local rules? The next nugget
is about prompting, and it gives you an outlook on how prompting is developing
into AI agents.

</div>

## Sources and further reading

- Kestin, G., Miller, K., Klales, A., Milbourne, T., & Ponti, G. (2025). AI tutoring
  outperforms in-class active learning: an RCT introducing a novel research-based
  design in an authentic educational setting. *Scientific Reports*, 15.
  https://doi.org/10.1038/s41598-025-97652-6
- UNESCO (2023). *Guidance for generative AI in education and research.*
  https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research
- European Union (2024). *Regulation (EU) 2024/1689 (AI Act)*, Article 4 (AI literacy),
  Article 5 and Annex III. https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- ASSET deeper nugget on this aspect: *LO 4.1.1 AI Pedagogy — Exploring AI-Assisted Teaching Approaches.*

*CC BY-SA 4.0 · ASSET project · contact: hannes.tegelbeckers@ovgu.de*
