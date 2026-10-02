<!--
author:   Hannes Tegelbeckers · OVGU Magdeburg · ASSET project (UNESCO-UNEVOC Network)
email:    hannes.tegelbeckers@ovgu.de
version:  2026.1.0
language: en
narrator: UK English Female
license:  CC BY-SA 4.0
comment:  ASSET AI starter course 2026, Nugget 1 of 5 (Orientation): what AI is, a human-centred mindset, and the UNESCO AI Competency Framework for Teachers. Acquire level.

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

# Nugget 1 · AI and Me

--{{0}}--
Welcome to the first nugget of the ASSET starter course on artificial intelligence
in technical and vocational education and training. In about twenty-five minutes
you will find your own starting point.

<div class="hero">
<div class="hero__kicker">ASSET · AI for Skills, Sustainability and Training · Starter course 2026 · Nugget 1 of 5</div>
<div class="hero__title">AI and Me: <em>a human-centred start</em></div>
<div class="hero__sub">Orientation for TVET teachers, trainers and in-company instructors. No technical background needed.</div>
<div class="chips">
<span class="chip chip--level">Level: Acquire</span>
<span class="chip">⏱ about 25 minutes</span>
<span class="chip">UNESCO AI CFT: human-centred mindset · professional learning</span>
<span class="chip">🌐 works offline</span>
</div>
</div>

**After this nugget you can …**

1. describe in your own words what AI is, and name three places where it already appears in your trade;
2. explain what a *human-centred* approach to AI means for a teacher;
3. locate yourself in the UNESCO AI Competency Framework for Teachers;
4. set one personal goal for this starter course.

<div class="partners">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNESCO-UNEVOC logo">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET project logo">
<span>A UNESCO-UNEVOC Network Coaction Initiative · HWK OWL Bielefeld · UNEVOC Centres Magdeburg, Sri Lanka and Mauritius · CC BY-SA 4.0</span>
</div>

## How this course works

--{{0}}--
Every nugget follows the same six steps, so you always know where you are.

The starter course has **five nuggets**. Each one takes 25–35 minutes and can be
done on its own, on a phone, and offline.

| Nugget | Topic | Key question |
| --- | --- | --- |
| **1 · AI and Me** | orientation, human-centred mindset | *What does AI mean for me as a teacher?* |
| 2 · How AI Works | basics, data, generative AI | *What happens inside the box?* |
| 3 · AI Tools for Teaching | tools, data routes, tool choice | *Which tool, for what, and at what price?* |
| 4 · Prompting | talking to AI with purpose; outlook to agents | *How do I get useful results?* |
| 5 · Quality and Ethics | checking, protecting, deciding | *How do I use AI responsibly?* |

Every nugget follows the same **six steps**:

@steps(0)

<div class="cards">
<div class="card card--amber"><div class="card__title">① Start</div>A short case from a TVET workplace and a question to you.</div>
<div class="card"><div class="card__title">② Understand</div>The core ideas, in plain language and with examples from trades.</div>
<div class="card card--green"><div class="card__title">③ Try</div>A hands-on task. If you have no AI tool at hand, use the example result.</div>
<div class="card card--violet"><div class="card__title">④ Check</div>A short quiz with explanations. Mistakes are part of learning.</div>
<div class="card card--teal"><div class="card__title">⑤ Reflect</div>Notes for your learning journal, and ideas for your own classroom.</div>
<div class="card card--indigo"><div class="card__title">⑥ Look ahead</div>Summary, and where the topic goes next.</div>
</div>

<div class="box box--class">
<div class="box__label">Two levels at once</div>

This course is built so that you experience the methods you can later use with
your own learners: a case to start, trying things out, a quiz with feedback,
reflection. Look out for the boxes marked **In your classroom**.

</div>

**Tips:** Click the 🔊 speaker symbol to listen to a slide. Use the **Textbook**
view (the glasses symbol at the top) if you prefer to read. Your answers in the
text fields are saved in your own browser only.

# ① Start: Jonas and the perfect reports

@steps(1)

--{{0}}--
We start with a situation that many trainers know.

<div class="persona">
<div class="persona__avatar">⚡</div>
<div>
<div class="persona__name">Jonas · master electrician, training centre of a Chamber of Skilled Crafts, Germany</div>

Jonas trains second-year apprentices in electrical installation. This week, the
written reports on a switchboard installation look different: perfect grammar,
tidy headings, correct technical terms. One apprentice who usually struggles with
writing handed in the best report in the group.

In the workshop the next day, the same apprentice cannot explain why a residual
current device (RCD) was placed where it is.

</div>
</div>

<div class="box box--case">
<div class="box__label">Your first thoughts</div>

What would you do in Jonas's place? There is no right or wrong answer here.

</div>

[(1)] Ban AI tools for all written work.
[(2)] Ignore it: the report is fine.
[(3)] Talk to the apprentice and find out how the report was made.
[(4)] Change the task so that the thinking has to happen visibly.
[(5)] I am not sure yet.

--{{1}}--
Keep your choice in mind. We will come back to Jonas at the end of this nugget.

{{1}}
> We will come back to Jonas at the end of this nugget. Keep your choice in mind.

## Where do you stand today?

--{{0}}--
A short self-check helps you see your starting point. Nobody else sees your answers.

**How often do you use AI tools such as chat assistants, translation or image tools?**

[(1)] Never, or I am not sure
[(2)] Sometimes, for private things
[(3)] Sometimes, for work
[(4)] Regularly, for teaching

**How do you feel about AI in vocational education right now?** (choose all that fit)

[[curious]] Curious
[[worried]] Worried
[[overwhelmed]] Overwhelmed
[[excited]] Excited
[[sceptical]] Sceptical
[[indifferent]] Indifferent

**One question about AI I would really like answered in this course:**

[[___ ___]]

# ② Understand: What is AI?

@steps(2)

--{{0}}--
Let us clarify what we mean when we say artificial intelligence.

<div class="box">
<div class="box__label">A working definition</div>

**Artificial intelligence (AI)** is a family of computer systems that produce
outputs such as **predictions, recommendations, decisions or content** (text,
images, speech) from the input they receive — in ways that were not written
down step by step by a programmer, but **learned from large amounts of data**.

</div>

Three points matter for teachers:

1. **AI is not one thing.** A navigation app, a spam filter, a machine that
   detects faulty welds, and a chat assistant are all called "AI". They work
   differently and have different risks.
2. **AI finds patterns, it does not understand.** It can be very useful and
   still be wrong in ways a human expert would never be.
3. **AI is made by people.** People choose the data, the purpose, and how it is
   used. That means people are responsible — including you, when you use it.

## AI is already in your trade

--{{0}}--
Many learners will meet AI at work long before they meet it at school.

<div class="cards">
<div class="card"><div class="card__title">🚗 Automotive</div>Diagnostic systems suggest likely faults from sensor data; predictive maintenance warns before parts fail.</div>
<div class="card card--green"><div class="card__title">🏗 Construction</div>Planning software checks building models for clashes; drones and image analysis measure progress.</div>
<div class="card card--amber"><div class="card__title">🍳 Hospitality</div>Booking systems forecast demand; translation tools help with international guests.</div>
<div class="card card--teal"><div class="card__title">🩺 Health and care</div>Systems flag unusual values; speech recognition helps with documentation.</div>
<div class="card card--violet"><div class="card__title">🏭 Manufacturing</div>Cameras detect surface defects; robots adapt their movements.</div>
<div class="card card--indigo"><div class="card__title">🗂 Office and admin</div>Assistants draft letters, summarise meetings and sort emails.</div>
</div>

Since the end of 2022, **generative AI** — systems that *produce* text, images,
audio or code on request — has been available to everyone with a phone. This is
why AI suddenly became a topic in every classroom, and it is the focus of this
course.

## A human-centred mindset

--{{0}}--
UNESCO asks teachers to take a human-centred view of AI. Here is what that means in practice.

UNESCO describes a **human-centred mindset** as the starting point for all work
with AI in education. In plain words:

<div class="cards">
<div class="card card--teal"><div class="card__title">People decide</div>AI can suggest. Decisions about learners — grades, admission, safety — stay with people who can explain and take responsibility for them.</div>
<div class="card card--teal"><div class="card__title">Learning comes first</div>The question is not "Can AI do this?" but "Does this help my learners build real competence?"</div>
<div class="card card--teal"><div class="card__title">Rights are protected</div>Privacy, fairness and inclusion matter more than convenience.</div>
<div class="card card--teal"><div class="card__title">Skills are kept</div>AI should support professional skills, not quietly replace the practice learners need.</div>
</div>

<div class="box">
<div class="box__label">Key idea</div>

**Human agency** means that people remain in control: they understand enough to
question the AI, they can say no, and they can explain their decision.
In a workshop, this is familiar: a good tradesperson uses power tools,
but knows how the job is done and checks the result.

</div>

## Where you are: the UNESCO framework

--{{0}}--
This course is based on the UNESCO AI Competency Framework for Teachers, published in 2024.

The **UNESCO AI Competency Framework for Teachers** (2024) describes
**15 competencies** in **five aspects** and **three levels**: *Acquire*,
*Deepen* and *Create*. This starter course works on the **Acquire** level in all
five aspects.

<div class="fw">
<div class="fw__head">Aspect</div><div class="fw__head">Acquire</div><div class="fw__head">Deepen</div><div class="fw__head">Create</div>
<div class="fw__row">1 · Human-centred mindset</div><div class="fw__here">Nugget 1</div><div>…</div><div>…</div>
<div class="fw__row">2 · Ethics of AI</div><div class="fw__here">Nugget 5</div><div>…</div><div>…</div>
<div class="fw__row">3 · AI foundations and applications</div><div class="fw__here">Nuggets 2 · 3 · 4</div><div>…</div><div>…</div>
<div class="fw__row">4 · AI pedagogy</div><div class="fw__here">Nuggets 3 · 4</div><div>…</div><div>…</div>
<div class="fw__row">5 · AI for professional development</div><div class="fw__here">Nuggets 1 · 5</div><div>…</div><div>…</div>
</div>

The assignment of nuggets to aspects is this course's own; the aspect and level
names are UNESCO's. After the starter course, the ASSET learning objectives
LO 1.1.1 to LO 5.1.1 go deeper into each aspect.

# ③ Try: Ask an AI about your trade

@steps(3)

--{{0}}--
Now it is your turn. This task takes about five minutes.

<div class="box box--try">
<div class="box__label">Task · 5 minutes</div>

1. Open any AI chat assistant you have access to (for example the one offered by
   your institution, or a free one on your phone).
2. Type this question and replace the part in brackets with your trade:
   > *What are the three most important safety rules for a beginner in [your trade]?*
3. Read the answer as an **expert**, not as a learner. Mark in your head what is
   correct, what is missing, and what is doubtful.

**No AI access?** Open the example below and assess it instead.

</div>

<details>
<summary><strong>Example answer (for "electrical installation")</strong></summary>

> 1. **Always switch off and isolate the power** before working on a circuit, and
>    make sure it cannot be switched on again.
> 2. **Wear appropriate personal protective equipment**, such as insulated gloves
>    and safety glasses.
> 3. **Never work alone** on electrical systems.

*An expert's view:* Rule 1 is good but incomplete: it misses *verifying* that the
circuit is dead with a tester, which is a core step of the recognised safe
isolation procedure. Rule 3 sounds plausible but is not a general rule
everywhere. Nothing is said about local regulations. The answer is **fluent,
confident and partly incomplete** — typical for generative AI.

</details>

**What did you notice?** (choose all that apply)

[[correct]] Most of it was correct
[[missing]] Something important was missing
[[wrong]] Something was wrong or doubtful
[[general]] It was very general, not specific to my country or workplace
[[confident]] It sounded more confident than it should

# ④ Check

@steps(4)

--{{0}}--
Four short questions. Read the explanation after each one.

**1. Which statement fits a human-centred approach to AI in TVET?**

[( )] If an AI grades faster than a teacher, it should grade on its own.
[(X)] AI may suggest, but decisions about learners stay with people who can explain them.
[( )] Teachers should avoid AI until it makes no more mistakes.
[( )] Learners should decide alone whether AI is used in assessment.
************************************************
Human agency does not mean rejecting AI. It means that responsibility and final
decisions remain with people — especially for grades, admission and safety.
************************************************

**2. Which of these are examples of AI? (choose all that apply)**

[[X]] A camera system that detects faulty welds
[[X]] A chat assistant that drafts a lesson plan
[[ ]] A spreadsheet that adds up hours with a fixed formula
[[X]] A translation app
************************************************
The spreadsheet follows a rule a person wrote down. The other three produce
their outputs from patterns learned from data.
************************************************

**3. Complete the sentence:** The UNESCO AI Competency Framework for Teachers has three levels: Acquire, Deepen and [[Create]].
[[?]] It begins with the letter C.
************************************************
Acquire → Deepen → Create. This starter course works on the *Acquire* level.
************************************************

**4. True or false?**

[(true) (false)]
[ ( )  (X) ] Generative AI checks its answers against reliable sources before replying.
[ (X)  ( ) ] AI answers can be fluent and confident and still incomplete.
[ (X)  ( ) ] People choose the data, the purpose and the use of an AI system.
************************************************
Generative AI produces probable text, not checked facts. That is why your
expertise is needed. Nugget 2 explains why.
************************************************

# ⑤ Reflect: Back to Jonas

@steps(5)

--{{0}}--
Let us return to Jonas and connect the case to your own teaching.

Jonas decided not to ban AI but to **make the thinking visible**. The written
report stays, and each apprentice now explains two decisions from the report in a
five-minute talk at the switchboard. Jonas also discussed with the group when AI
help is fine (for language, structure) and when it is not (for the technical
reasoning that is being assessed).

<div class="box box--class">
<div class="box__label">In your classroom</div>

- Ask learners **how** they used AI, not only **whether** they did.
- Combine written work with a short **practical or oral** part.
- Agree on simple, shared rules: what AI may help with, and what must be the
  learner's own work.

</div>

**Learning journal** — your notes are saved in your browser only.

Compare your choice at the start with Jonas's decision. Would you now decide differently? Why?

[[___ ___ ___]]

**My goal for this starter course** (for example: "I want to use AI to prepare differentiated worksheets and know how to check them."):

[[___ ___]]

# ⑥ Look ahead

@steps(6)

--{{0}}--
Here is the summary of this nugget and a look at what comes next.

<div class="takeaways">

**Take-aways**

- AI is a family of systems that learn patterns from data; generative AI produces text, images and more.
- AI is already part of most trades — your learners need guidance for work, not only for school.
- A **human-centred mindset** means: people decide, learning comes first, rights are protected, skills are kept.
- The UNESCO framework gives you a map: five aspects, three levels. You start with *Acquire*.

</div>

<div class="box box--ahead">
<div class="box__label">Next: Nugget 2 · How AI Works</div>

Why did the example answer sound so sure of itself while missing a step? The
next nugget opens the box: data, patterns, and how a chat assistant produces
its answers — without mathematics.

</div>

## Sources and further reading

- UNESCO (2024). *AI competency framework for teachers.* Paris: UNESCO.
  https://www.unesco.org/en/articles/ai-competency-framework-teachers
- UNESCO (2023). *Guidance for generative AI in education and research.* Paris: UNESCO.
  https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research
- UNESCO-UNEVOC. *TVET and artificial intelligence* — resources of the UNEVOC Network.
  https://unevoc.unesco.org
- ASSET deeper nugget on this aspect: *LO 1.1.1 Human-Centred AI Mindset — Human Agency.*

**Contact:** Hannes Tegelbeckers, Otto von Guericke University Magdeburg ·
hannes.tegelbeckers@ovgu.de

*This course is licensed under CC BY-SA 4.0. You may adapt and translate it for
your context; please name the ASSET project.*
