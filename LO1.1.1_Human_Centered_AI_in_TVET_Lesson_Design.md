> <!--
author: Hannes Tegelbeckers
email: hannes.tegelbeckers@ovgu.de
version: 0.0.1
language: en
narrator: US English Female
comment: Presentation on AI & the Future of Work

link: https://raw.githubusercontent.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/refs/heads/main/ASSET_basic.css

@@ comment olga: 

@@@
This is a block comment.
It can span multiple lines.
@@@


@style
.sector-card {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 2rem;
    margin: 1rem;
    border-radius: 15px;
    box-shadow: 0 8px 32px rgba(0,0,0,0.3);
    transition: transform 0.3s ease;
}

.sector-card:hover {
    transform: translateY(-5px);
}

.ai-tool-demo {
    background: #f8f9fa;
    border: 2px solid #007bff;
    border-radius: 10px;
    padding: 1.5rem;
    margin: 1rem 0;
}

.quiz-interactive {
    background: linear-gradient(45deg, #ff6b6b, #ffa726);
    color: white;
    padding: 1rem;
    border-radius: 10px;
    margin: 1rem 0;
}

.resource-link {
    background: #28a745;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    text-decoration: none;
    display: inline-block;
    margin: 0.25rem;
    transition: all 0.3s ease;
}

.resource-link:hover {
    background: #218838;
    transform: scale(1.05);
}
@end

@customQuiz
[[...]]
<script>
"@0" == btoa( "@input".trim().toLowerCase() )
</script>
@end

@aiDemo: <div class="ai-tool-demo">**AI Demo:** @0<br>**Tool:** @1<br>**Try it:** [Click here](@2)</div>

@sectorCard: <div class="sector-card">**@0**<br>@1</div>

@resourceLink: <a href="@1" class="resource-link" target="_blank">@0</a>

-->


<svg xmlns='http://www.w3.org/2000/svg' width='1100' height='400' viewBox='0 0 800 450'>
  <!-- Background -->
  <rect width='800' height='450' fill='#1A237E' />
  
  <!-- White rounded rectangle container -->
  <rect x='50' y='50' width='700' height='350' rx='20' fill='white' />
  
  <!-- Title -->
  <text x='400' y='130' font-family='Segoe UI, Arial, sans-serif' font-size='50' font-weight='bold' text-anchor='middle' fill='#1A237E'>
    Placeholder Learning Nugget
  </text>
  
  <!-- Presenter -->
  <text x='400' y='200' font-family='Segoe UI, Arial, sans-serif' font-size='20' font-weight='bold' text-anchor='middle' fill='#3949AB'>
   
  </text>

  <!-- Additional presenter info -->
  <text x='400' y='225' font-family='Segoe UI, Arial, sans-serif' font-size='16' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    Based on the UNESCO UNEVOC ICT and AI framework
  </text>

  <!-- Faculty info -->
  <text x='400' y='250' font-family='Segoe UI, Arial, sans-serif' font-size='16' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    A collaboration of the UNEVOC Network
  </text>

  <!-- University info -->
  <text x='400' y='275' font-family='Segoe UI, Arial, sans-serif' font-size='16' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    Academic reference: Tegelbeckers, Hannes; [further Authors] (2025) Selflearning Nuggets for UNESCO AI Competency Framework for Teachers; CC BY-SA, Repository: https://raw.githubusercontent.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative
  </text>

  <!-- License info -->
  <div style="position: fixed; bottom: 10px; right: 10px; font-size: 12px; opacity: 0.7;">
    <img src="media/CC_BY-SA_icon.png" alt="CC BY-SA" style="height: 20px; vertical-align: middle;">
    <a href="https://creativecommons.org/licenses/by-sa/4.0/" style="margin-left: 5px; text-decoration: none;">CC BY-SA 4.0</a>
  </div>
</svg>


<!-- UNEVOC -->
<div style="position: fixed; bottom: 1px; left: 20px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNEVOC Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">UNEVOC</div>
</div>

<!-- ASSET -->
<div style="position: fixed; bottom: 1px; left: 180px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">ASSET</div>
</div>

<!-- HWK Blume -->
<div style="position: fixed; bottom: 1px; left: 340px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/HWK_Blume.png?raw=true" alt="HWK Blume Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 7px;">HWK Blume</div>
</div>

<!-- GIZ -->
<div style="position: fixed; bottom: 1px; left: 500px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/giz-logo.gif?raw=true" alt="GIZ Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">GIZ</div>
</div>

<!-- UoVT -->
<div style="position: fixed; bottom: 1px; left: 660px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UoVT_Logo.png?raw=true" alt="UoVT Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">UoVT</div>
</div>

<!-- OVGU -->
<div style="position: fixed; bottom: 1px; left: 820px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/Masub27/Intro/blob/main/ovgu.png?raw=true" alt="OVGU Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">OVGU</div>
</div>

<!-- HRDC -->
<div style="position: fixed; bottom: 1px; left: 980px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/hrdc_logo.png?raw=true" alt="HRDC Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">HRDC</div>
</div>

<!-- MITD -->
<div style="position: fixed; bottom: 1px; left: 1140px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/mitd_logo.png?raw=true" alt="MITD Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">MITD</div>
</div>

---

# Human-Centred Mindset- Human Agency in the Age of AI

**A virtual training course on Ethical AI Integration in Technical and Vocational Education**

> **Learning Objective (Acquire Level):** Develop a human-centered mindset and understand ethical, pedagogical, and AI concepts to make informed decisions on using AI in TVET teaching.

**Professur für Ingenieurpädagogik und technische Bildung** 

**Lehrstuhl:** Prof. Dr. Frank Bünning  

**Presenter:** Hannes Tegelbeckers  

**Faculty of Human Sciences**

## Workshop Overview

By the end of this workshop, you will be able to:

* **Identify** human-centered AI principles and ethical guidelines relevant to TVET teaching
* **Evaluate** if and how AI tools align with your lesson's pedagogical goals
* **Decide** whether to use AI in a sample lesson and justify your choice
* **Reflect** on how AI use impacts inclusivity, student agency, and safety in your local TVET context

## Part 1: Foundation - Understanding Human-Centered AI

@@ This is a single-line comment

### What is Human-Centered AI?

@@@
This is a block comment.
It can span multiple lines.
@@@

> **Human-centered AI** means always putting *people's needs, rights, and well-being first* when adopting AI technology.

**Core Principles:**

1. **Human Agency** - AI should empower, not replace human decision-making
2. **Accountability** - Clear responsibility for AI decisions and outcomes  
3. **Social Responsibility** - Consider broader impact on society and communities
4. **Transparency** - Understanding how AI systems work and make decisions
5. **Fairness** - Ensuring equitable treatment for all users
6. **Privacy** - Protecting personal data and respecting consent


!?[Stanford Human Centred AI Technology and Application](https://youtu.be/se4CQ5UZXaM)


## The Challenge of AI in TVET

### Current Context

* Over 60% of educational tasks could be partially automated by AI
* Educational systems worldwide must develop new approaches for the changing landscape
* Students need digital and transversal competencies including:

  - Critical thinking
  - Communication skills
  - Media literacy
  - Computational Thinking and Literacy

### Key Challenges

**Technical Challenges:**

- Data protection and privacy
- Access inequalities to AI technologies
- Ensuring authentic assessment

**Pedagogical Challenges:**

- Maintaining hands-on learning in technical fields
- Developing teacher competencies
- Balancing AI support with skill development

**Ethical Challenges:**

- Bias in AI systems
- Student surveillance concerns
- Over-reliance on automated systems

## AI Applications in TVET Context

### Appropriate Use Cases

**Interactive Simulations & Virtual Labs**

- AI-powered simulations create safe, virtual environments to practice skills when physical equipment is limited.

> **Example:** An AI-driven smart sensor simulator for electrical engineering students to experiment with building lighting systems virtually.

**Predictive Maintenance Dashboards**

- Teaching students how AI analyzes sensor data to predict equipment failures.

> **Example:** AI dashboard predicting when motors or solar panels might need maintenance.

**AI Tutors and Assistants**

- Personalized support for theory learning and practice problems.

> **Example:** AI assistant that quizzes electrical trainees on circuit theory and adapts questions based on their mistakes.

**Data Analysis and Diagnostics**

- AI tools for analyzing complex technical data.

> **Example:** AI-based analyzer helping students debug microcontroller code or electrical circuits.


### Real-World Scenario

Imagine you're **Alex**, a construction trades instructor preparing a lesson on smart lighting installation. You have access to an AI-based sensor system that detects wiring faults and optimizes energy use.

**Question:** Should Alex integrate this AI tool into the classroom? What factors should influence this decision?


<div style="background: #E8F5E8; border-left: 4px solid #4CAF50; padding: 1rem; margin: 1rem 0;">

### Task: Name 5 factors you came across so far

**Think about Alex's decision from multiple perspectives:**

**Technical Factor:** (e.g., complexity, reliability, maintenance)

    [[___]]

**Pedagogical Factor:** (e.g., learning objectives, teaching methods)

    [[___]]

**Safety Factor:** (e.g., electrical safety, student protection)

    [[___]]

**Resource Factor:** (e.g., cost, training needs, time)

    [[___]]

**Ethical Factor:** (e.g., privacy, data collection, student consent)

    [[___]]

</div>



## Part 2: Self-Assessment Quiz

Test your understanding of human-centered AI principles:

### Quiz 1: Ethical Considerations

A vocational college is considering using facial recognition for automatic attendance. What are the potential concerns?

    [[ ]] Privacy - scanning faces collects sensitive biometric data
    [[ ]] Bias and accuracy - facial recognition can be less accurate for certain groups
    [[ ]] Absolutely flawless attendance tracking with no downsides
    [[ ]] Student consent & comfort - constant surveillance can create unease
    [[?]] Select all that apply
    <script>
      // Define which answers are correct (1-based indexing)
      let correct = [1, 2, 4];
      let selected = @input;
      
      // Check if selection matches correct answers
      let isCorrect = correct.every(i => selected.includes(i)) && 
                     selected.every(i => correct.includes(i)) &&
                     !selected.includes(3);
      
      if (isCorrect) {
        send.lia("✅ **Correct!** Privacy, bias/accuracy, and student comfort are all legitimate concerns. Facial recognition in schools raises significant ethical issues.");
      } else if (selected.includes(3)) {
        send.lia("❌ **Incorrect.** No technology is flawlessly beneficial - every AI system has trade-offs that must be carefully considered.");
      } else {
        send.lia("❌ **Partially correct.** Consider all the potential issues: privacy (biometric data collection), bias (accuracy varies by demographic), and student comfort (surveillance environment).");
      }
    </script>

### Quiz 2: Human-Centered Approach

Which statement best reflects a human-centered AI approach in teaching?

    [( )] AI systems can fully automate teaching, making educators unnecessary
    [(X)] AI tools should support and augment teaching, empowering students while teachers maintain oversight
    [[?]] Choose the best answer
    <script>
      if (@input === 1) {
        send.lia("❌ **Incorrect.** This contradicts human-centered principles - the goal is not to replace teachers but to enhance learning while keeping human values central.");
      } else {
        send.lia("✅ **Correct!** A human-centered approach keeps teachers and learners at the core, using AI as a helpful tool that supports rather than replaces human judgment and expertise.");
      }
    </script>

### Quiz 3: AI Tool Selection

You're teaching wiring fault diagnosis. Which approach best demonstrates human-centered AI use?

    [( )] Use an AI that instantly identifies all faults for students
    [( )] Avoid all AI tools to maintain traditional methods
    [(X)] Use an AI expert system that guides students through diagnostic questions step-by-step
    [( )] Use the newest AI tool regardless of educational value
    [[?]] Select the most appropriate approach
    <script>
      let choice = @input;
      if (choice === 3) {
        send.lia("✅ **Excellent choice!** This approach uses AI to support learning by guiding students through the logical diagnostic process, maintaining educational value while leveraging technology appropriately.");
      } else if (choice === 1) {
        send.lia("❌ **Not ideal.** Instant answers don't teach the diagnostic process - students miss the learning opportunity.");
      } else if (choice === 2) {
        send.lia("❌ **Too restrictive.** This ignores potential benefits of well-designed AI tools for education.");
      } else {
        send.lia("❌ **Poor reasoning.** Technology should be chosen based on educational value, not novelty.");
      }
    </script>

## Part 3: Hands-On Activity

### Task: AI Tool Evaluation Framework

**Scenario:** You need to evaluate an AI tool for your TVET classroom. Complete this evaluation framework:

**Step 1: Define Your Teaching Context**

Fill in your specific context:

    [[___]]

    **Subject Area:** (e.g., electrical engineering, construction, automotive)

    [[___]]

    **Lesson Topic:** (e.g., circuit diagnosis, safety procedures, equipment maintenance)

    [[___]]

    **Learning Objective:** (what should students be able to do after the lesson?)

    [[___]]

    **Student Level:** (beginner, intermediate, advanced)

**Step 2: AI Tool Analysis**

Consider an AI tool you might use. Evaluate it using these criteria:

**Pedagogical Alignment**

    [( )] Strongly supports learning objectives
    [( )] Somewhat supports learning objectives  
    [( )] Neutral impact on learning
    [( )] Potentially hinders learning objectives
    [[?]] How well does the AI tool align with your learning objectives?

**Ethical Considerations**

Check all that apply to your chosen AI tool:

    [[ ]] Requires student personal data
    [[ ]] Uses camera/audio recording
    [[ ]] Makes automated decisions about students
    [[ ]] Could exhibit bias in responses
    [[ ]] Transparent about how it works
    [[ ]] Students can opt out if desired
    [[?]] Identify potential ethical concerns

**Human-Centered Design**

    [( )] Students remain in control of their learning
    [( )] Teacher maintains oversight and final decisions
    [( )] Tool explains its reasoning when possible
    [( )] All of the above
    [(X)] Tool completely takes over the learning process
    [[?]] Which best describes your AI tool's approach?

**Step 3: Decision Matrix**

Based on your analysis, make your decision:

    [( )] Use the AI tool as planned
    [( )] Use the AI tool with modifications
    [( )] Use the AI tool with additional safeguards
    [( )] Do not use the AI tool
    [[?]] What is your decision?

**Step 4: Justification**

    **Explain your decision in 2-3 sentences:**

    [[___]]



## Part 4: Group Discussion Activity

### Discussion Forum: AI in Your TVET Context

**Instructions:** Consider the following discussion prompts and share your thoughts. In a real workshop setting, these would be discussed in small groups.

#### Discussion Prompt 1: Opportunities

> **Question:** How can AI contribute to more equitable education in your TVET field?

Think about:

- Students with different learning needs
- Access to expensive equipment or materials
- Language barriers
- Geographic limitations

**Your thoughts on AI opportunities:**

    [[___]]



#### Discussion Prompt 2: Challenges

> **Question:** What are the biggest risks of AI adoption in your teaching context?

Consider:

- Safety implications in hands-on learning
- Skills that might be lost
- Dependency on technology
- Cost and access issues

**Your thoughts on AI challenges:**

    [[___]]



#### Discussion Prompt 3: Implementation

> **Question:** What would you need to successfully implement human-centered AI in your classroom?

Think about:

- Training and support
- Infrastructure requirements
- Policy guidelines
- Student preparation

**Your implementation considerations:**

    [[___]]



### Reflection Exercise

**Personal Action Plan**

Based on what you've learned, complete this action plan:

**One AI principle I will prioritize:** (e.g., transparency, fairness, human agency)

    [[___]]


**One change I will make to my teaching approach:**

    [[___]]

**One area where I need more learning/support:**

    [[___]]

**Next step I will take within the next month:**

    [[___]]


## Part 5: Synthesis and Next Steps

### Key Takeaways

**Remember these essential points:**

1. **Human Agency First** - AI should enhance, not replace, human decision-making
2. **Ethical Foundation** - Always consider privacy, fairness, and transparency
3. **Pedagogical Purpose** - AI must serve clear educational goals
4. **Context Matters** - What works in one setting may not work in another
5. **Continuous Learning** - AI technology and best practices are constantly evolving

### Moving Forward: Action Items

**Immediate Steps (This Week):**

- [ ] Identify one AI tool relevant to your teaching area
- [ ] Research its privacy policy and ethical guidelines
- [ ] Consider how it aligns with your learning objectives

**Short-term Goals (Next Month):**

- [ ] Connect with colleagues to discuss AI experiences
- [ ] Attend a webinar or read articles about AI in education
- [ ] Pilot test one AI tool with appropriate safeguards

**Long-term Development (Next 6 Months):**

- [ ] Develop evaluation criteria for AI tools in your context
- [ ] Create guidelines for student AI use in your courses
- [ ] Contribute to institutional AI policy discussions

### Additional Resources

**Further Learning:**

- [UNESCO AI Competency Framework for Teachers](https://unesdoc.unesco.org/ark:/48223/pf0000391104)
- [KI-Campus: AI in Education](https://ki-campus.org)
- [UNESCO Ethics of AI Recommendation](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics)

**Tools to Explore:**

- [Google's Teachable Machine](https://teachablemachine.withgoogle.com/) - No-code AI model creation
- [Perplexity](https://www.perplexity.ai) - Research with source citations
- [ChatGPT](https://chat.openai.com) - General AI assistant for lesson planning

### Final Reflection

**How has your perspective on AI in education changed through this workshop?**

    [[___]]

**What questions do you still have about implementing human-centered AI?**

    [[___]]


---

**Thank you for participating in this workshop on Human-Centered AI in TVET Lesson Design!**

*Remember: Your role as an educator is irreplaceable. Armed with knowledge and the right mindset, you can harness AI to enrich learning while safeguarding what matters most - your students' growth, rights, and futures.*

## Next Steps in Your Learning Journey

What would you like to focus on next?

### 🎓 Go to next Competence
[**Competence Ethics and AI Course**](https://liascript.github.io/course/?https://raw.githubusercontent.com/OVGU-VET-TechEd/ASSET_AI_Learning_Nuggets/refs/heads/main/LO2.1.1_Ethics_AI_in_TVET_Lesson_Design.md)

- Complete comprehensive course
- In-depth learning modules
- Structured progression

### 🎯 Targeted Learning Objective  
[**Human Centred AI - Learnon Objective**](YOUR_LEARNON_OBJECTIVE_URL)

- Focused learning objective
- Same competency area
- Quick skill building
