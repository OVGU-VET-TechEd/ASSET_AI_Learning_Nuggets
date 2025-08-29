<!--
author: UNESCO UNEVOC AI Framework Team
email: contact@unesco.org
version: 1.0.0
language: en
narrator: US English Female
comment: LO4.1.1 - Human-Centered AI in TVET Lesson Design (Acquire Level)

link: https://raw.githubusercontent.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/refs/heads/main/ASSET_basic.css

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

.principle-box {
    background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%);
    color: white;
    padding: 1.5rem;
    margin: 1rem 0;
    border-radius: 10px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.2);
}

.scenario-box {
    background: #fff3cd;
    border: 2px solid #ffc107;
    border-radius: 10px;
    padding: 1.5rem;
    margin: 1rem 0;
}

.ethical-consideration {
    background: #f8d7da;
    border: 2px solid #dc3545;
    border-radius: 8px;
    padding: 1rem;
    margin: 0.5rem 0;
}

.hands-on-activity {
    background: #d1ecf1;
    border: 2px solid #17a2b8;
    border-radius: 10px;
    padding: 1.5rem;
    margin: 1rem 0;
}
@end

@aiDemo: <div class="ai-tool-demo">**AI Demo:** @0<br>**Tool:** @1<br>**Try it:** [Click here](@2)</div>

@principleBox: <div class="principle-box">**@0**<br>@1</div>

@scenarioBox: <div class="scenario-box">**Scenario:** @0<br><br>@1</div>

@ethicalBox: <div class="ethical-consideration">⚠️ **Ethical Consideration:** @0</div>

@handsOnBox: <div class="hands-on-activity">🔬 **Hands-On Activity:** @0<br><br>@1</div>

@resourceLink: <a href="@1" class="resource-link" target="_blank">@0</a>

-->

<svg xmlns='http://www.w3.org/2000/svg' width='1100' height='400' viewBox='0 0 800 450'>
  <!-- Background -->
  <rect width='800' height='450' fill='#1A237E' />
  
  <!-- White rounded rectangle container -->
  <rect x='50' y='50' width='700' height='350' rx='20' fill='white' />
  
  <!-- Title -->
  <text x='400' y='130' font-family='Segoe UI, Arial, sans-serif' font-size='36' font-weight='bold' text-anchor='middle' fill='#1A237E'>
    LO4.1.1: Human-Centered AI
  </text>
  
  <text x='400' y='170' font-family='Segoe UI, Arial, sans-serif' font-size='36' font-weight='bold' text-anchor='middle' fill='#1A237E'>
    in TVET Lesson Design
  </text>
  
  <!-- Subtitle -->
  <text x='400' y='210' font-family='Segoe UI, Arial, sans-serif' font-size='18' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    Acquire Level - Ethical AI Integration in Technical Education
  </text>

  <!-- Framework info -->
  <text x='400' y='240' font-family='Segoe UI, Arial, sans-serif' font-size='16' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    Based on the UNESCO AI Competency Framework for Teachers
  </text>

  <!-- Network info -->
  <text x='400' y='265' font-family='Segoe UI, Arial, sans-serif' font-size='16' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    A collaboration of the UNEVOC Network
  </text>

  <!-- License info -->
  <text x='400' y='290' font-family='Segoe UI, Arial, sans-serif' font-size='12' font-weight='bold' text-anchor='middle' fill='#3949AB'>
    CC BY-SA 4.0 | Repository: UNESCO ASSET Initiative
  </text>
</svg>

<!-- Partner logos - same as LO1.1.1 -->
<div style="position: fixed; bottom: 1px; left: 20px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UNESCO-UNEVOC_logo.png?raw=true" alt="UNEVOC Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">UNEVOC</div>
</div>

<div style="position: fixed; bottom: 1px; left: 180px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/ASSET_icon.png?raw=true" alt="ASSET Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">ASSET</div>
</div>

<div style="position: fixed; bottom: 1px; left: 340px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/HWK_Blume.png?raw=true" alt="HWK Blume Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 7px;">HWK Blume</div>
</div>

<div style="position: fixed; bottom: 1px; left: 500px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/giz-logo.gif?raw=true" alt="GIZ Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">GIZ</div>
</div>

<div style="position: fixed; bottom: 1px; left: 660px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/blob/main/media/UoVT_Logo.png?raw=true" alt="UoVT Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">UoVT</div>
</div>

<div style="position: fixed; bottom: 1px; left: 820px; opacity: 0.9; z-index: 1000; text-align: center; width: 100px;">
  <img src="https://github.com/Masub27/Intro/blob/main/ovgu.png?raw=true" alt="OVGU Logo" style="height: 60px; width: auto; border-radius: 10px;" />
  <div style="font-size: 0.8em; color: #555; margin-top: 5px;">OVGU</div>
</div>

---

# AI Pedagogy - Exploring AI-Assisted Teaching Approaches

**A virtual training nugget on AI Pedagogy on TVET**

> Develop a human-centered mindset and understand ethical, pedagogical, and AI concepts to make informed decisions on using AI in teaching.

## Introduction

AI is increasingly finding its way into vocational classrooms. This learning nugget is essential because teachers need to ensure AI tools truly serve learning, **not just use technology for its own sake**.

@scenarioBox(Real-World Challenge, You are planning a module on smart lighting systems for electrical engineering trainees. You have access to an AI-assisted diagnostic tool that can predict lighting faults. **Should you integrate this AI tool?** If yes, which tool and why? If not, why not? Such decisions require balancing innovation with ethics and sound pedagogy.)

### Learning Outcomes

By the end of this nugget, you will be able to:

* **Identify** human-centered AI principles and ethical guidelines relevant to teaching
* **Evaluate** if and how AI tools align with your lesson's pedagogical goals (especially in construction and electrical trades)
* **Decide** whether to use AI in a sample lesson and **justify your choice** - considering which AI tool fits best and why, or whether no AI is the better option
* **Reflect** on how AI use impacts inclusivity, student agency, and safety in your local TVET context

## Part 1: Human-Centered AI Principles

### Core Concepts

@principleBox(Human-Centered AI Mindset, Always putting people's needs, rights, and well-being first when adopting AI. UNESCO emphasizes focusing on human agency, accountability and social responsibility in AI use.)

**Key Ethical AI Principles:**

@principleBox(Fairness, Ensuring AI works equally well for all students and doesn't discriminate based on language, background, or other characteristics)

@principleBox(Transparency, Students and teachers understand how AI systems work and make decisions)

@principleBox(Privacy, Personal data is protected and used only with proper consent)

@principleBox(Accountability, Clear responsibility exists for AI decisions and their consequences)

### The "Complement, Don't Replace" Rule

An AI tutoring system might give quick feedback, but **the teacher remains the guide and decision-maker**. AI should empower students and teachers - not replace or overpower them.

Before using AI, ask yourself: *Does this tool respect my students' rights and enhance learning?*

## Part 2: Domain-Appropriate Pedagogy in TVET

### Hands-On Learning Considerations

In TVET fields like Construction and Electrical Engineering, hands-on experience and safety are paramount. Any AI tool should fit the teaching method of the topic.

@scenarioBox(Diagnostic Learning Example, If students are learning to diagnose wiring faults, an AI-driven troubleshooting app could be useful **only if** it reinforces the students' understanding without removing critical thinking practice.)

**Always align AI use with your learning objectives:**

* If the objective is systematic fault-finding, an AI that instantly gives answers might undermine learning
* An AI that guides students with hints or simulates complex scenarios **could be pedagogically helpful**

### Micro-Activity: Spot the Considerations

Alex is considering using an AI tool in a smart lighting lesson. What should Alex think about before deciding?

    [[ ]] Does the AI tool improve learning outcomes without replacing hands-on practice?
    [[ ]] Is the AI's use ethical - are student data and privacy protected?
    [[ ]] Is the AI tool the newest, "coolest" tech available, even if unrelated to lesson goals?
    [[ ]] Does it align with the lesson's objectives and the students' level?
    [[?]] Select all valid considerations for Alex's human-centered decision
    <script>
      let correct = [1, 2, 4];
      let selected = @input;
      
      let isCorrect = correct.every(i => selected.includes(i)) && 
                     selected.every(i => correct.includes(i)) &&
                     !selected.includes(3);
      
      if (isCorrect) {
        send.lia("✅ **Correct!** The decision should be guided by pedagogical and ethical factors. Using technology for novelty alone is not a valid reason to integrate AI.");
      } else if (selected.includes(3)) {
        send.lia("❌ **Be careful!** Using the 'coolest' tech without considering educational value goes against human-centered principles.");
      } else {
        send.lia("❌ **Review your choices.** Think about what truly matters for student learning and ethical AI use.");
      }
    </script>

## Part 3: AI Use Cases in TVET

### Interactive Simulations & Virtual Labs

@aiDemo(AI-Powered Virtual Labs, AI-driven smart sensor simulator, Create safe virtual environments to practice skills when physical equipment is limited)

AI-powered simulations can create safe, virtual environments to practice skills. For example, an AI-driven smart sensor simulator can emulate how a building's lighting system responds to different conditions, letting students experiment virtually.

This is especially useful when physical equipment access is limited.

### Predictive Maintenance Dashboards

In electrical engineering courses, you might use an AI dashboard that predicts equipment failures (e.g., when a motor or solar panel might need maintenance). This teaches students how AI analyzes sensor data to foresee problems - a common industry application.

### AI Tutors and Assistants

These range from chatbots that answer students' FAQs to intelligent tutoring systems for theory lessons. They can provide personalized hints or generate practice problems.

@ethicalBox(However, ensure the AI's content is accurate and bias-free. The teacher should verify AI-provided information, as human oversight remains crucial.)

### Data Analysis and Diagnostics

AI can rapidly analyze complex data - energy usage logs, electrical signal anomalies, or construction project data. If programming microcontrollers for smart devices, an AI-based analyzer might help students debug code or circuits.

**Throughout all use cases, maintaining an ethical, human-centered stance is key.**

## Part 4: Branching Scenario Analysis

### Wiring Fault Diagnosis Challenge

Consider a practical assignment on wiring fault diagnosis. Three possible approaches:

    [( )] **Expert System (A)** - AI asks students diagnostic questions and suggests likely faults
    [( )] **Machine Learning Model (B)** - Students feed photos/data to AI which identifies probable issues
    [( )] **Manual Approach (C)** - Standard multimeter and manual checklist, no AI
    [[?]] Which approach would you choose for a human-centered learning experience?

Think about:
* **Expert System (A)**: Might teach logical troubleshooting process step by step
* **ML Model (B)**: Could be quick and exciting, but does it teach diagnosis or just give answers?
* **Manual Approach (C)**: Ensures fundamental practice but misses modern industry AI exposure

<script>
let choice = @input;
if (choice === 1) {
  send.lia("🤔 **Interesting choice!** The expert system can guide students through logical steps. Consider: Does it maintain student agency? Is the reasoning transparent?");
} else if (choice === 2) {
  send.lia("⚠️ **Consider carefully:** While exciting, does this approach teach the diagnostic process or just provide answers? How transparent is the AI's decision-making?");
} else if (choice === 3) {
  send.lia("🔧 **Traditional approach!** This ensures students learn fundamentals. Consider: Are you missing opportunities to show how AI is used in modern industry?");
}
</script>

**There's no absolute "right" answer** - the best choice depends on your learning goals. A human-centered teacher might combine approaches: manual diagnosis first, then expert system comparison, discussing how AI handles the same problem.

The key is that **students gain insight**, and AI (if used) is a tool for learning, not a replacement.

## Part 5: Hands-On Exploration

@handsOnBox(Teachable Machine Experiment, We'll use Google's Teachable Machine to create a simple AI model with no coding required)

### Building Your First AI Model

**Step 1: Access the Tool**
Visit [Teachable Machine](https://teachablemachine.withgoogle.com/) in your browser.

**Step 2: Choose Image Project**
We'll train an image classification model. Think of two categories to distinguish, such as:
* "Correct Wiring" vs "Faulty Wiring" examples
* Proper electrical connections vs wrong connections
* Different tools (screwdriver vs wrench)

**Step 3: Gather Training Examples**
For each class, add 5-10 images. You can upload photos or use your webcam. Even simple sketches or diagrams work for this conceptual exercise.

**Step 4: Train the Model**
Hit "Train" - the AI will quickly train a neural network on your examples (usually takes seconds).

**Step 5: Test Your Model**
Show the model a new image to see if it classifies correctly. The model will give confidence percentages for each class.

### Reflection Questions

After experimenting, consider:

    [[___]]
    **How well did your model perform?**

    [[___]] 
    **What limitations did you notice?**

    [[___]]
    **How could you use this type of activity with students?**

**What this teaches us about AI:**
* AI is only as good as the examples given
* It may identify obvious differences but be confused by new scenarios
* Training data can be biased or incomplete
* This demystifies AI - it's not magic, it learns from data

### Low-Bandwidth Alternative

If internet access is limited, discuss conceptually:
* What examples would you feed the AI?
* What would you expect it to learn?
* How might it fail or succeed?

The core experience is understanding how AI learns from examples.

## Part 6: Learning Check

### Quiz: Ethical AI in Practice

A vocational college considers using facial recognition for automatic attendance, scanning students' faces as they enter. What are potential issues?

    [[ ]] Privacy - Scanning faces collects sensitive biometric data
    [[ ]] Bias and accuracy - Facial recognition can be less accurate for certain groups
    [[ ]] Absolutely flawless attendance tracking with no downsides
    [[ ]] Student consent & comfort - Constant surveillance can make students uneasy
    [[?]] Select all potential concerns
    <script>
      let correct = [1, 2, 4];
      let selected = @input;
      
      let isCorrect = correct.every(i => selected.includes(i)) && 
                     selected.every(i => correct.includes(i)) &&
                     !selected.includes(3);
      
      if (isCorrect) {
        send.lia("✅ **Correct!** Privacy, bias/accuracy, and student comfort are real concerns. Experts recommend caution with facial recognition in schools due to these issues.");
      } else if (selected.includes(3)) {
        send.lia("❌ **Not quite.** No technology is flawlessly beneficial - every AI system has trade-offs that must be weighed carefully.");
      } else {
        send.lia("❌ **Partially correct.** Consider all aspects: privacy (biometric data), bias (accuracy varies by group), and environment (surveillance concerns).");
      }
    </script>

### Human-Centered AI Mindset Check

Which statement best reflects a human-centered AI approach in teaching?

    [( )] AI systems can fully automate teaching, so educators eventually become unnecessary
    [(X)] AI tools should support and augment teaching, empowering students while the teacher maintains oversight
    [[?]] Choose the statement that aligns with human-centered principles
    <script>
      if (@input === 2) {
        send.lia("✅ **Perfect!** A human-centered mindset keeps teachers and learners at the core, using AI as a helpful tool that enhances rather than replaces human expertise.");
      } else {
        send.lia("❌ **Incorrect.** This contradicts human-centered principles - the goal is not to replace teachers but to enhance learning with human values central.");
      }
    </script>

### Self-Reflection

Consider a lesson you currently teach or plan to teach:

    [[___]]
    **Would you incorporate an AI tool? If yes, what type and why? If no, why not?**

    [[___]]
    **What specific change or consideration will you apply after this learning nugget?**

Write your thoughts to reinforce your learning.

## Part 7: Further Learning Pathways

### Expanding Your Knowledge

**AI for Inclusion and Special Needs:**
Learn how AI can support inclusive education through assistive technologies, text-to-speech tools, and personalized learning approaches for students with diverse needs.

**Open-Source Classroom AI Tools:**
Explore community-driven, self-hosted solutions that address data privacy concerns and can be adapted to local needs. Check educator forums and UNESCO ICT in Education resources.

**Next Module - LO4.1.2:**
The next learning objective focuses on **main categories of AI systems and applications for teaching and learning** - distinguishing between AI that tutors students, assists teachers in planning, or manages administrative tasks.

### Essential Resources

@resourceLink(UNESCO AI Competency Framework, https://unesdoc.unesco.org/ark:/48223/pf0000391104)

@resourceLink(UNESCO Ethics of AI Recommendation, https://www.unesco.org/en/artificial-intelligence/recommendation-ethics)

@resourceLink(UNESCO Guidance on Generative AI in Education, https://www.unesco.org/en/articles/what-you-need-know-about-unescos-new-ai-competency-frameworks-students-and-teachers)

@resourceLink(Teachable Machine by Google, https://teachablemachine.withgoogle.com/)

### Moving Forward

Remember: **Your role as a teacher is irreplaceable.** Armed with knowledge and the right mindset, you can harness AI to enrich learning while safeguarding what matters most - your students' growth, rights, and futures.

The field of AI in education evolves rapidly. Stay curious, stay critical, and always prioritize human-centered values in your teaching practice.

---

**Congratulations on completing LO4.1.1: Human-Centered AI in TVET Lesson Design!**

*Continue your journey with the next learning objective to deepen your understanding of AI applications in education.*
