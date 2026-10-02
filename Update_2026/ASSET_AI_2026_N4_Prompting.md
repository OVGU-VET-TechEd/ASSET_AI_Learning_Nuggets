<!--
author:   Hannes Tegelbeckers · OVGU Magdeburg · ASSET project (UNESCO-UNEVOC Network)
email:    hannes.tegelbeckers@ovgu.de
version:  2026.1.0
language: en
narrator: UK English Female
license:  CC BY-SA 4.0
comment:  ASSET AI starter course 2026, Nugget 4 of 5 (Prompting): the T-R-A-C-E building blocks, improving and grounding prompts, and an outlook from prompts to AI agents. Acquire level.

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

# Nugget 4 · Prompting

--{{0}}--
Welcome to nugget four. Today you learn to talk to AI with purpose, and you get a look at where prompting is heading: towards AI agents.

<div class="hero">
<div class="hero__kicker">ASSET · AI for Skills, Sustainability and Training · Starter course 2026 · Nugget 4 of 5</div>
<div class="hero__title">Prompting: <em>talking to AI with purpose</em></div>
<div class="hero__sub">Five building blocks for good prompts, four moves to improve results — and an outlook from single prompts to AI agents.</div>
<div class="chips">
<span class="chip chip--level">Level: Acquire</span>
<span class="chip">⏱ about 35 minutes</span>
<span class="chip">UNESCO AI CFT: AI foundations and applications · AI pedagogy</span>
<span class="chip">🌐 works offline</span>
</div>
</div>

**After this nugget you can …**

1. write a prompt using the five building blocks **T·R·A·C·E**;
2. improve a result step by step instead of starting again;
3. ground a prompt in your own source material;
4. build a small personal prompt library for your teaching;
5. explain in simple words how prompting has developed into AI assistants and agents — and what does, and does not, "learn" in them.

@steps(0)

<div class="partners">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNESCO-UNEVOC logo">
<img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET project logo">
<span>A UNESCO-UNEVOC Network Coaction Initiative · CC BY-SA 4.0</span>
</div>

# ① Start: "Make a quiz about brakes"

@steps(1)

--{{0}}--
We return to Nuwan's automotive workshop.

<div class="persona">
<div class="persona__avatar">🔧</div>
<div>
<div class="persona__name">Nuwan · automotive mechatronics instructor, Sri Lanka</div>

Nuwan types into a chat assistant: **"Make a quiz about brakes."**

The result: ten questions. Four are about the history of brakes, three are about
bicycle brakes, the language is too difficult for first-year learners, and there
are no answers. Nuwan thinks: *"AI is useless for my teaching."*

</div>
</div>

<div class="box box--case">
<div class="box__label">Your diagnosis</div>

The AI did exactly what it was asked. What information was missing in Nuwan's
request? Write down as many points as you can find.

</div>

[[___ ___ ___]]

# ② Understand: Five building blocks

@steps(2)

--{{0}}--
A good prompt is like a good work order: it says what, for whom, under which conditions, and what the result should look like.

Think of a prompt as a **work order** for a very fast, very well-read
assistant who knows nothing about your learners, your workshop or your country.
Five building blocks, easy to remember as **T·R·A·C·E**:

<div class="cards">
<div class="card"><div class="card__title">T · Task</div>What exactly should be produced? Use a clear verb: <em>create, explain, compare, check, rewrite</em>.</div>
<div class="card card--green"><div class="card__title">R · Role</div>Which expert perspective should the AI take? <em>"Act as an experienced automotive instructor."</em></div>
<div class="card card--amber"><div class="card__title">A · Audience and context</div>Who are the learners, what level, which trade, which country, what do they already know?</div>
<div class="card card--violet"><div class="card__title">C · Constraints</div>Rules and limits: length, language level, what to avoid, which standard or source to follow.</div>
<div class="card card--teal"><div class="card__title">E · Example and format</div>How should the result look? Table, list, number of items — ideally with a short example.</div>
</div>

You do not need all five every time. For important tasks, the more blocks you
use, the less the AI has to **guess** — and guessing is where generic or wrong
results come from.

## Before and after

--{{0}}--
Here is Nuwan's prompt, rebuilt with the five building blocks.

**Before**

```text
Make a quiz about brakes.
```

**After**

```text
TASK         Create a quiz with 6 multiple-choice questions on disc brake
             systems in passenger cars.
ROLE         Act as an experienced automotive mechatronics instructor.
AUDIENCE     First-year learners in a vocational programme in Sri Lanka.
             They know the basic parts of a car, not yet the hydraulic system.
             English is their second language.
CONSTRAINTS  Focus on function, wear and safety checks. Use short sentences
             and simple words. Each question has 4 options, exactly one correct.
             No questions about history or bicycles.
EXAMPLE /    After the questions, give an answer key with one sentence
FORMAT       explaining why each correct answer is right.
             Example: "1. (b) — Brake fluid transfers the pedal force ..."
```

The labels are only there to show the structure — you can write the same as a
normal paragraph.

## Four moves to improve results

--{{0}}--
Prompting is a conversation. The first answer is a draft, not the end.

The first answer is a **draft**. Instead of starting again, continue the
conversation with one of four moves:

<div class="cards">
<div class="card"><div class="card__title">① Refine</div><em>"Questions 3 and 5 are too difficult. Replace them with questions about visual wear checks."</em></div>
<div class="card card--green"><div class="card__title">② Ask for options</div><em>"Give me three different ways to introduce this topic: a story, a problem, a demonstration."</em></div>
<div class="card card--amber"><div class="card__title">③ Let it ask you</div><em>"Before you start, ask me up to five questions about my learners and my goal."</em></div>
<div class="card card--violet"><div class="card__title">④ Make it show its limits</div><em>"List the assumptions you made, and mark every statement I should check against the manufacturer's manual."</em></div>
</div>

<div class="box box--warn">
<div class="box__label">Careful with "Are you sure?"</div>

Language models tend to **agree with the user**. If you ask *"Are you sure?"*,
many will change a correct answer. Check with sources and people, not by asking
the same system.

</div>

## Ground it in your source

--{{0}}--
The most effective way to get correct, local content is to give the AI your own source.

In Nugget 2 you met **grounding**: the AI cannot know your curriculum, your
workshop manual or your national standard — unless you give it.

```text
Here is the section on brake inspection from our training manual:

"""
[paste the text here]
"""

Using ONLY the text above, create 5 true/false statements for first-year
learners. If the text does not contain enough information, say so instead
of adding facts.
```

Three good habits:

1. Put the source in **clear quotation marks** or between `"""` lines.
2. Say **"only from the text above"**.
3. Allow the AI to **say "I don't know"**. By default, models always produce something.

## Pattern cards for TVET teachers

--{{0}}--
Here are six prompt patterns you can adapt. Copy them into your own prompt library.

| Pattern | Prompt skeleton |
| --- | --- |
| **Lesson starter** | *"Suggest three short, realistic workplace situations from [trade] that make [topic] relevant for [learners]. Each ends with a question for discussion."* |
| **Differentiate** | *"Rewrite this text at three levels: simple language (A2), standard, and extended with one extra challenge. Keep all technical terms and explain them."* |
| **Quiz with reasons** | *"Create [n] multiple-choice questions on [topic] from the text below. For each wrong option, give the misconception behind it."* |
| **Feedback helper** | *"Here is an anonymised learner answer and my marking criteria. Suggest feedback in two parts: one strength, one next step. Do not give a grade."* |
| **Role-play partner** | *"Play a customer at [workplace] who is unhappy about [situation]. Stay in role. After 6 exchanges, stop and give the learner feedback on politeness and clarity."* |
| **Socratic tutor** | *"Help me find the fault in [system] by asking me one question at a time. Do not tell me the answer."* |

<div class="box">
<div class="box__label">Save what works</div>

When a prompt works well, **save it** — in a document, a note on your phone, or as
the *custom instructions* of your assistant. Share it with colleagues. A good
prompt library is worth more than a new tool.

</div>

# ③ Try: Rebuild a prompt

@steps(3)

--{{0}}--
Now build your own prompt with the five blocks. The task takes about ten minutes.

<div class="box box--try">
<div class="box__label">Task · 10 minutes</div>

1. Choose a **real task** for your next teaching week (a quiz, a worksheet, an
   example case, a text in simpler language).
2. Write a **one-line prompt** first and send it. Save the answer.
3. Write a **T·R·A·C·E prompt** for the same task, in the fields below. Send it.
4. Use **one of the four moves** to improve the result.
5. Compare: what changed?

**No AI access?** Write the prompt anyway — the thinking is the main skill — and
look at the example comparison below.

</div>

**T · Task**

[[___]]

**R · Role**

[[___]]

**A · Audience and context**

[[___ ___]]

**C · Constraints**

[[___ ___]]

**E · Example and format**

[[___]]

<details>
<summary><strong>Example comparison (Nuwan's quiz)</strong></summary>

| | One-line prompt | T·R·A·C·E prompt |
| --- | --- | --- |
| Relevance | history, bicycles, cars mixed | only disc brakes in cars |
| Level | too difficult | short sentences, simple words |
| Usable in class | no answer key | answer key with reasons |
| Time to a usable quiz | 20 minutes of rework | 5 minutes of checking |
| Still to check | everything | technical details against the manual |

The better prompt did not make the AI more intelligent. It **reduced the
guessing**.

</details>

# ④ Check

@steps(4)

--{{0}}--
Five questions. Read the explanation after each one.

**1. What does the "A" in T·R·A·C·E stand for?**

[( )] Answer
[(X)] Audience and context
[( )] Accuracy
[( )] Assessment
************************************************
The AI does not know your learners. Telling it who they are is often the single
biggest improvement.
************************************************

**2. Which building block is missing?** *"Act as an experienced chef. Create 5 questions on knife safety for first-year learners with little reading experience. Use a numbered list."*

[( )] Task
[( )] Role
[(X)] Constraints (for example: short sentences, one correct answer, which standard to follow)
[( )] Format
************************************************
Task, role, audience and format are there. Constraints — rules and limits — are missing.
************************************************

**3. The first answer is almost right, but two questions are too hard. What is the best next step?**

[( )] Start a new chat with the same prompt
[(X)] Continue the conversation and ask to replace exactly those two questions
[( )] Ask "Are you sure?"
************************************************
Refining keeps what is good and fixes what is not. "Are you sure?" invites the
model to simply agree with you.
************************************************

**4. Which instructions help ground an answer in your source? (choose all that apply)**

[[X]] Paste the source text into the prompt
[[X]] "Use only the text above."
[[X]] "If the text does not contain the answer, say so."
[[ ]] "Use your general knowledge to fill any gaps."
************************************************
The last instruction does the opposite: it invites facts from outside your source.
************************************************

**5. Which prompt keeps the effortful thinking with the learner?**

[( )] "Explain the fault and write the repair steps."
[(X)] "Ask me one question at a time to help me find the fault. Do not tell me the answer."
[( )] "Summarise the chapter so I don't have to read it."

# ⑤ Reflect and transfer

@steps(5)

--{{0}}--
Let us connect prompting with your teaching — and with your learners.

<div class="box box--class">
<div class="box__label">In your classroom · "Work order for a machine" (20 minutes)</div>

Learners already know work orders from their trade. Let them write a **work order
for an AI**: in pairs, they write a T·R·A·C·E prompt for a task from their field,
swap it with another pair, and check it like a supervisor: *Is it clear? What
would a new colleague have to guess?* Only then do they try it.

Clear instructions, checking results, taking responsibility — these are
**vocational competences**, and they are exactly what good prompting needs.

</div>

**Learning journal**

Look at your diagnosis of Nuwan's prompt from the start. Which of the five building blocks did you already find, and which did you miss?

[[___ ___]]

My first entry for my personal prompt library (a prompt I will really use):

[[___ ___ ___]]

# ⑥ Look ahead: From prompts to agents

@steps(6)

--{{0}}--
Prompting is only the beginning. In a few years, the way we work with AI has changed a lot. Here is an overview, for orientation only.

This part is an **outlook**. You do not need to use any of this now — but your
learners will meet it at work, and you will hear the words everywhere.

Since 2022, people have kept doing the same thing: **moving what worked out of the
chat window and into something that can be reused, checked and run again.**

```ascii
 2022              2023-2024            2025                  2026
+------------+    +---------------+    +----------------+    +-------------------+
| 1 PROMPT   |--->| 2 STORED      |--->| 3 HARNESS      |--->| 4 LOOP / AGENT    |
| one request|    |   INSTRUCTION |    | a program runs |    | checks, revises,  |
| one answer |    | rules + source|    | fixed steps,   |    | decides next step,|
|            |    | saved & reused|    | uses tools,    |    | stops on a rule;  |
|            |    |               |    | keeps records  |    | keeps notes of    |
|            |    |               |    |                |    | what it learned   |
+------------+    +---------------+    +----------------+    +-------------------+
  you type          you write the        you design the        you set the goal,
  every time        rules once           steps and checks      checks and limits
```

| Stage | What it is | Everyday example |
| --- | --- | --- |
| **1 · Prompt** | one request, one answer | you ask for a quiz, as in this nugget |
| **2 · Stored instruction** | rules and sources saved and reused: *custom instructions*, custom assistants, "skills" | a saved "quiz assistant" that always follows your format and uses your manual |
| **3 · Harness** | a program around the model runs fixed steps on many inputs, can use tools (search, files, calculator) and records what it did | every learner email is sorted, a draft reply is written, and each draft is saved with a note of how it was made |
| **4 · Loop / agent** | the system checks its own output against rules, revises, **chooses its next action** and stops when a condition is met | an assistant plans a workshop schedule, checks room and machine availability, fixes conflicts, and asks a person to approve |

The dates show when each stage became **common practice**. All four stages
exist side by side today — and for most teaching tasks, **stage 1 and 2 are the
right choice**. A later stage is not better; it retains and automates more — and
creates more that has to be checked.

## Assistant or agent?

--{{0}}--
The words assistant and agent are often mixed up. One question separates them.

One question tells them apart: **who decides what happens next?**

<div class="cards">
<div class="card"><div class="card__title">Assistant</div>A person decides every next step. The AI answers, the person acts. <br><em>A chat assistant, a "summarise" button.</em></div>
<div class="card card--indigo"><div class="card__title">Agent</div>The system decides the next step itself, from a set of allowed actions, and repeats until it is done.</div>
</div>

A system is only an agent if it passes **three tests**:

1. **It chooses** — the order of steps is not fixed in advance by a person.
2. **It acts** — its choices change something: a file is written, a booking made, a message sent.
3. **It stops on a rule** — there is a clear, checkable condition for "finished", and a limit on the number of rounds.

<div class="box box--warn">
<div class="box__label">Why this matters</div>

An agent can only do what people **allow** it to do. The list of allowed actions
is also the list of things that can go wrong. A system that can act but has **no
stop rule** is not a smart agent — it is an uncontrolled process with access to
your data.

</div>

## Do agents learn by themselves?

--{{0}}--
You will hear about self-learning or self-improving agents. Here is what that really means.

You will hear of **"self-learning"** or **"self-improving"** agents. Remember
Nugget 2: **the model does not change when it is used.** What changes is
**stored text** that the system reads at the start of every run:

- **memory notes** about the user and earlier conversations;
- **lessons** written after a failed check (*"Always take torque values from the manufacturer's manual, never from memory."*);
- **skills** — instruction files for recurring tasks;
- a **knowledge file or wiki** with approved answers to earlier questions.

```ascii
 +---------+     +-----------+     +---------+     +----------+
 |  read   |---->|  do the   |---->|  check  |---->|  write   |
 |  notes  |     |  task     |     | results |     |  lesson  |
 +---------+     +-----------+     +---------+     +----------+
      ^                                                 |
      |              +------------------+               |
      +--------------+  a PERSON        |<--------------+
                     |  reviews notes   |
                     +------------------+
```

This makes a system better over time **without changing the model**. It also
brings new responsibilities: whoever can edit the notes influences every later
result; errors in the notes are repeated; and personal data must not be stored
there. **Someone has to review what the system "learned".**

## What this means for TVET

--{{0}}--
Finally, what does this development mean for you and your learners?

<div class="cards">
<div class="card card--indigo"><div class="card__title">The human role moves</div>From typing every prompt to <strong>setting goals, rules, checks and limits</strong> — and approving results.</div>
<div class="card card--teal"><div class="card__title">Vocational skills matter more</div>Specifying a job clearly, checking work, knowing when to stop, taking responsibility: this is what a master craftsperson does — and what supervising AI needs.</div>
<div class="card card--amber"><div class="card__title">Prompting stays the base</div>Every stage builds on clear instructions. What you practised today is the foundation for all of it.</div>
</div>

| Stage | UNESCO level it relates to (this course's assignment) |
| --- | --- |
| Prompting | **Acquire** — use an AI tool appropriately |
| Stored instructions, harness | **Deepen** — integrate AI into your practice and check it systematically |
| Designing loops and agents, deciding stop rules | **Create** — design new AI-supported ways of working |

<div class="takeaways">

**Take-aways**

- A good prompt is a good work order: **T·R·A·C·E** — task, role, audience and context, constraints, example and format.
- The first answer is a draft. Improve it with four moves: refine, ask for options, let it ask you, make it show its limits.
- **Ground** important content in your own sources, and allow "I don't know".
- Save good prompts: your prompt library is your first "stored instruction".
- Prompting has developed into stored instructions, harnesses and agents. The model does not learn during use — stored notes do, and **people must review them**.

</div>

<div class="box box--ahead">
<div class="box__label">Next: Nugget 5 · Quality and Ethics</div>

Better prompts give better drafts — but drafts still need checking. The last
nugget gives you a routine for checking AI output and a framework for ethical
decisions in TVET.

</div>

## Sources and further reading

- UNESCO (2024). *AI competency framework for teachers.*
  https://www.unesco.org/en/articles/ai-competency-framework-teachers
- Anthropic (2024). *Building effective agents.*
  https://www.anthropic.com/engineering/building-effective-agents
- OpenAI. *Prompt engineering* (platform documentation).
  https://platform.openai.com/docs/guides/prompt-engineering
- Walking Labs. *Learn Harness Engineering* (open course, 2025–2026).
  https://walkinglabs.github.io/learn-harness-engineering/en/
- ASSET / OVGU Magdeburg (2026). *AI in Teaching: Tools, Strategies and Reflection* —
  the five stages of prompting in detail (EU GREEN Masterclass, V7).
  https://github.com/OVGU-VET-TechEd/Masterclass_EU_Green_Tegelbeckers

*CC BY-SA 4.0 · ASSET project · contact: hannes.tegelbeckers@ovgu.de*
