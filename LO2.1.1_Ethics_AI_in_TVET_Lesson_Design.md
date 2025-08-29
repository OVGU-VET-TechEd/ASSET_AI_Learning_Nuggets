<!--
author: UNESCO UNEVOC Network
email: ai.framework@unesco.org
version: 1.0.0
language: en
narrator: US English Female
comment: AI Ethics in TVET - Identifying Ethical Controversies

link: https://raw.githubusercontent.com/OVGU-VET-TechEd/ASSET_UNESCO_Coinitiative/refs/heads/main/ASSET_basic.css

@style
.ethics-card {
    background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
    color: white;
    padding: 2rem;
    margin: 1rem;
    border-radius: 15px;
    box-shadow: 0 8px 32px rgba(0,0,0,0.3);
    transition: transform 0.3s ease;
}

.ethics-card:hover {
    transform: translateY(-5px);
}

.case-study {
    background: #f8f9fa;
    border: 2px solid #e74c3c;
    border-radius: 10px;
    padding: 1.5rem;
    margin: 1rem 0;
}

.ethical-lens {
    background: linear-gradient(45deg, #3498db, #2980b9);
    color: white;
    padding: 1rem;
    border-radius: 10px;
    margin: 1rem 0;
}

.resource-link {
    background: #27ae60;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    text-decoration: none;
    display: inline-block;
    margin: 0.25rem;
    transition: all 0.3s ease;
}

.resource-link:hover {
    background: #219a52;
    transform: scale(1.05);
}

.reflection-box {
    background: #fff3cd;
    border: 1px solid #ffeaa7;
    border-radius: 8px;
    padding: 1rem;
    margin: 1rem 0;
}
@end

@ethicsDemo: <div class="case-study">**Case Study:** @0<br>**Context:** @1<br>**Ethical Issue:** @2</div>

@ethicalLens: <div class="ethical-lens">**@0**<br>@1</div>

@resourceLink: <a href="@1" class="resource-link" target="_blank">@0</a>

@reflection: <div class="reflection-box">**Reflection:** @0</div>

-->

<svg xmlns='http://www.w3.org/2000/svg' width='1100' height='400' viewBox='0 0 800 450'>
  <!-- Background -->
  <rect width='800' height='450' fill='#C0392B' />
  
  <!-- White rounded rectangle container -->
  <rect x='50' y='50' width='700' height='350' rx='20' fill='white' />
  
  <!-- Title -->
  <text x='400' y='120' font-family='Segoe UI, Arial, sans-serif' font-size='42' font-weight='bold' text-anchor='middle' fill='#C0392B'>
    AI Ethics in TVET
  </text>
  
  <!-- Subtitle -->
  <text x='400' y='160' font-family='Segoe UI, Arial, sans-serif' font-size='24' font-weight='bold' text-anchor='middle' fill='#E74C3C'>
    Identifying Ethical Controversies
  </text>

  <!-- Learning Objective -->
  <text x='400' y='195' font-family='Segoe UI, Arial, sans-serif' font-size='18' text-anchor='middle' fill='#2C3E50'>
    Learning Objective 2.1.1 - Acquire Level
  </text>

  <!-- Framework reference -->
  <text x='400' y='220' font-family='Segoe UI, Arial, sans-serif' font-size='16' text-anchor='middle' fill='#34495E'>
    Based on the UNESCO AI Competency Framework for Teachers
  </text>

  <!-- Network collaboration -->
  <text x='400' y='245' font-family='Segoe UI, Arial, sans-serif' font-size='16' text-anchor='middle' fill='#34495E'>
    A collaboration of the UNESCO UNEVOC Network
  </text>

  <!-- Academic reference -->
  <text x='400' y='270' font-family='Segoe UI, Arial, sans-serif' font-size='12' text-anchor='middle' fill='#7F8C8D'>
    Academic reference: UNESCO UNEVOC Network (2025) AI Ethics Learning Nuggets
  </text>
  
  <!-- License -->
  <text x='400' y='290' font-family='Segoe UI, Arial, sans-serif' font-size='12' text-anchor='middle' fill='#7F8C8D'>
    CC BY-SA 4.0 License
  </text>
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

# Ethics of AI - Grasping Ethical Principles of AI in Education

**A virtual training nugget on AI Ethics in Technical and Vocational Education**

> **Learning Objective (Acquire Level):** Identify and exemplify key ethical controversies in the use of AI tools in education through four critical lenses: Human Agency, Privacy, Security, and Linguistic & Cultural Relevance.

**UNESCO UNEVOC Network Collaboration**  
**Framework:** UNESCO AI Competency Framework for Teachers  
**Target Audience:** TVET Educators in Germany, Sri Lanka, Mauritius, and beyond

## Learning Nugget Overview

By the end of this learning nugget, you will be able to:

* **Identify** the four key ethical lenses for evaluating AI in education
* **Recognize** ethical red flags in AI tools used in TVET settings
* **Analyze** real-world scenarios through ethical frameworks
* **Apply** ethical decision-making to your own teaching context
* **Advocate** for responsible AI use in your institution

## Part 1: Foundation - Understanding AI Ethics in TVET

### What is AI Ethics in Education?

> **AI Ethics in Education** means ensuring that artificial intelligence tools in teaching and learning contexts respect human rights, promote fairness, protect privacy, and serve the best interests of all learners.

**Why Ethics Matter in TVET:**

* AI systems are increasingly used for grading, attendance, tutoring, and student monitoring
* Without careful consideration, AI may undermine teacher autonomy, violate student privacy, or introduce biases
* Vocational educators need awareness to ensure AI is used responsibly and aligns with local values and regulations

### The Four Ethical Lenses

@ethicalLens(Human Agency, Who controls decisions when AI is involved? Does AI support or undermine teacher and student autonomy?)

@ethicalLens(Privacy, How is data about students and staff used and protected? Are AI tools respecting confidentiality and consent?)

@ethicalLens(Security, How safe and secure are AI systems in schools? Consider both data security and physical/emotional safety of students.)

@ethicalLens(Linguistic & Cultural Relevance, Are AI tools inclusive for all languages and cultures present in your classroom? Who might be excluded or disadvantaged?)

### Real-World Scenario Introduction

Meet **Maria**, a carpentry instructor who has been asked to use a new AI-powered assessment tool that automatically grades student project photos and provides instant feedback.

**Initial Questions to Consider:**
- What ethical concerns might arise with this AI tool?
- How can Maria evaluate whether this technology serves her students' best interests?

## The Challenge of AI Ethics in TVET

### Current Context in Technical Education

* AI tools are rapidly entering workshops, labs, and classrooms
* Students need protection from surveillance, bias, and privacy violations
* Teachers must balance innovation with ethical responsibility
* Institutions need frameworks for making AI adoption decisions

### Key Ethical Challenges

**Human Agency Challenges:**
- AI systems making decisions about student progress or abilities
- Teachers feeling pressured to accept automated assessments
- Students losing control over their learning paths

**Privacy Challenges:**
- Extensive data collection through AI platforms
- Biometric data use (facial recognition, voice analysis)
- Unclear consent processes, especially with minors

**Security Challenges:**
- Protecting sensitive student and institutional data
- Ensuring AI systems don't create safety risks in workshops
- Preventing misuse of monitoring technologies

**Cultural & Linguistic Challenges:**
- AI systems trained primarily on English or dominant languages
- Cultural bias in AI recommendations and assessments
- Exclusion of local contexts and values

## AI Ethics Applications in TVET Context

### Common AI Tools and Their Ethical Implications

**AI-Powered Attendance Systems**
> Facial recognition or biometric scanning for automatic attendance tracking.

**Ethical Concerns:** Privacy (biometric data), bias (recognition accuracy varies by demographics), surveillance atmosphere

**Automated Assessment Tools**
> AI systems that grade written work, projects, or practical demonstrations.

**Ethical Concerns:** Bias against non-standard language use, lack of transparency in grading criteria, teacher autonomy

**Adaptive Learning Platforms**
> AI that personalizes learning paths based on student performance data.

**Ethical Concerns:** Student agency in learning choices, data privacy, algorithmic decision-making about student capabilities

**Workshop Safety Monitoring**
> AI cameras and sensors that monitor safety compliance in technical workshops.

**Ethical Concerns:** Constant surveillance, false alerts, cultural bias in behavior recognition

## Part 2: Self-Assessment Quizzes

Test your understanding of AI ethics principles:

### Quiz 1: Human Agency Scenarios

A vocational school implements an AI system that automatically assigns students to different skill level tracks based on their quiz performance. Students cannot override these assignments. What is the primary ethical concern?

    [(X)] Human Agency - the AI removes student choice and may override teacher professional judgment
    [( )] Privacy - this is mainly about decision-making, not data protection
    [( )] Security - no immediate security risk is described
    [( )] Cultural relevance - the issue is about control, not cultural bias
    [[?]] Select the most relevant ethical lens

### Quiz 2: Privacy in Practice

Your school's administration proposes using an AI system with cameras to monitor classrooms for safety and attendance. Which ethical concerns should you raise? (Select all that apply)

    [[ ]] Privacy and consent of students (constant video monitoring)
    [[ ]] Data security (sensitive biometric data could be hacked)
    [[ ]] Bias or discrimination (face recognition less accurate for some groups)
    [[ ]] No ethical issues - it's purely beneficial
    [[?]] Select all applicable concerns
    <script>
      let correct = [1, 2, 3];
      let selected = @input;
      
      let isCorrect = correct.every(i => selected.includes(i)) && 
                     selected.every(i => correct.includes(i)) &&
                     !selected.includes(4);
      
      if (isCorrect) {
        send.lia("✅ **Correct!** Privacy, security, and bias are all legitimate concerns with classroom surveillance systems.");
      } else if (selected.includes(4)) {
        send.lia("❌ **Incorrect.** No AI system is purely beneficial - all have ethical trade-offs that must be considered.");
      } else {
        send.lia("⚠️ **Partially correct.** Consider all potential issues: privacy (surveillance), security (data protection), and bias (unequal recognition accuracy).");
      }
    </script>

### Quiz 3: Cultural and Linguistic Relevance

An AI career counseling system consistently suggests university pathways while ignoring local trade opportunities popular in your region. Many students feel the system doesn't understand their context. This represents which ethical issue?

    [( )] Privacy - no data leakage is mentioned
    [( )] Security - no safety risks are described  
    [( )] Human agency - students can still choose their path
    [(X)] Linguistic/cultural relevance - the AI lacks local context and cultural awareness
    [[?]] Identify the primary ethical concern

## Part 3: Hands-On Case Study - "GradeMaster" Analysis

### Activity: Ethical Analysis Framework

**Scenario:** You are a vocational instructor considering "GradeMaster," an AI-powered grading assistant for your carpentry course assignments.

**Observed Issues:**
- Non-native speakers consistently receive lower scores
- Creative solutions are marked as incorrect when they don't match the AI's database
- The AI provides vague feedback without clear explanations
- Administration wants all teachers to accept AI grades without review

### Step 1: Identify Ethical Issues

For each scenario element, identify which ethical lens applies:

**Issue: Non-native speakers receive lower scores**

    [( )] Human Agency
    [( )] Privacy  
    [( )] Security
    [(X)] Linguistic & Cultural Relevance
    [[?]] Which ethical lens best applies?

**Issue: Administration wants teachers to accept all AI grades**

    [(X)] Human Agency
    [( )] Privacy
    [( )] Security  
    [( )] Linguistic & Cultural Relevance
    [[?]] Which ethical lens is most relevant?

**Issue: Vague AI feedback without explanations**

    [(X)] Human Agency (and transparency)
    [( )] Privacy
    [( )] Security
    [( )] Linguistic & Cultural Relevance
    [[?]] Which lens addresses transparency concerns?

### Step 2: Decision Framework

Based on your ethical analysis, what would you recommend?

    [( )] Use GradeMaster as intended by administration
    [( )] Use GradeMaster only as a draft grader with teacher review
    [( )] Request modifications to address bias and transparency issues
    [( )] Reject GradeMaster due to ethical concerns
    [(X)] Use as draft grader AND request modifications AND provide feedback to developers
    [[?]] What's the most ethical approach?

### Step 3: Justify Your Decision

    [[___]]
    **Explain your reasoning in 2-3 sentences:**

## Part 4: Interactive Activities

### Activity 1: Ethical Red Flag Detection

Review each AI tool scenario and identify potential ethical red flags:

**Scenario A: Smart Workshop Monitor**
An AI system uses cameras to detect when students aren't wearing safety equipment and automatically logs safety violations.

    [[___]]
    **Potential ethical issues:**

    [[___]]  
    **Which ethical lens is most relevant:**

**Scenario B: Adaptive Skills Assessment**
An AI platform tracks student performance across multiple exercises and automatically determines when they're ready for certification tests.

    [[___]]
    **Potential ethical issues:**

    [[___]]
    **Which ethical lens is most relevant:**

### Activity 2: Stakeholder Perspective Analysis

Consider the GradeMaster scenario from different viewpoints:

**Student Perspective:**

    [[___]]
    **Main concerns students might have:**

**Teacher Perspective:**  

    [[___]]
    **Main concerns teachers might have:**

**Administrator Perspective:**

    [[___]]
    **What administrators should consider:**

**Parent/Guardian Perspective:**

    [[___]]
    **Concerns parents might raise:**

### Activity 3: Creating Ethical Guidelines

Design three key ethical guidelines for AI use in your teaching context:

**Guideline 1:**

    [[___]]
    **Your first ethical guideline for AI in TVET:**

**Guideline 2:**

    [[___]]
    **Your second ethical guideline:**

**Guideline 3:**

    [[___]]
    **Your third ethical guideline:**

## Part 5: Synthesis and Next Steps

### Key Takeaways

**Essential Principles to Remember:**

1. **Human-Centered Approach** - AI should enhance, not replace, human judgment in education
2. **Four-Lens Analysis** - Always examine AI tools through agency, privacy, security, and cultural relevance lenses  
3. **Context Matters** - What's appropriate in one setting may not be in another
4. **Transparency is Crucial** - AI systems should be explainable and contestable
5. **Continuous Vigilance** - Ethical considerations require ongoing attention, not one-time assessment

### Critical Questions for AI Evaluation

Before adopting any AI tool, ask:

**Human Agency:**
- Does this preserve teacher professional autonomy?
- Do students maintain meaningful choice in their learning?
- Can human judgment override AI decisions?

**Privacy:**  
- What data is collected and how is it protected?
- Do students/parents understand and consent to data use?
- Are privacy rights respected throughout the process?

**Security:**
- How secure is the data storage and transmission?
- What happens if the system is breached or fails?
- Does the AI create new safety risks?

**Cultural Relevance:**
- Does the AI work equally well for all student populations?
- Are local contexts and values reflected?
- Who might be excluded or disadvantaged?

### Moving Forward: Professional Development Plan

**Immediate Actions (This Week):**
- [ ] Review one AI tool you currently use through the four ethical lenses
- [ ] Identify potential bias or fairness issues in your context
- [ ] Discuss ethical concerns with a colleague

**Short-term Goals (Next Month):**  
- [ ] Develop ethical evaluation criteria for new AI tools
- [ ] Research your institution's AI policies and guidelines
- [ ] Attend training on AI ethics in education

**Long-term Development (Next 6 Months):**
- [ ] Advocate for ethical AI guidelines at your institution  
- [ ] Mentor other educators on AI ethics considerations
- [ ] Contribute to policy discussions about AI in TVET

### Resources for Continued Learning

**Essential Readings:**
@resourceLink(UNESCO AI Ethics Recommendation, https://www.unesco.org/en/artificial-intelligence/recommendation-ethics)
@resourceLink(UNESCO AI Competency Framework for Teachers, https://unesdoc.unesco.org/ark:/48223/pf0000391104)
@resourceLink(European Commission AI in Education Guidelines, https://education.ec.europa.eu/focus-topics/digital-education/action-plan)

**Communities and Networks:**
@resourceLink(UNESCO UNEVOC Network, https://unevoc.unesco.org/)
@resourceLink(European School Education Platform - AI Group, https://school-education.ec.europa.eu/)

**Practical Tools:**
@resourceLink(AI Ethics Checklist Template, #)
@resourceLink(Student Data Privacy Audit Guide, #)

### Final Reflection and Action Planning

**Personal Reflection:**

    [[___]]
    **How has this learning nugget changed your perspective on AI in education?**

    [[___]]
    **Which ethical concern resonates most with your teaching context?**

    [[___]]
    **What's one specific action you'll take based on this learning?**

**Action Commitment:**

    [[___]]
    **I commit to implementing the following ethical practice in my teaching:**

    [[___]]
    **I will advocate for this change in my institution:**

    [[___]]
    **I will seek additional learning/support in this area:**

### Learning Outcome Verification

**Self-Assessment Checklist:**

Can you now:

- [ ] Identify ethical issues using the four-lens framework (Agency, Privacy, Security, Cultural Relevance)?
- [ ] Recognize ethical red flags in common AI educational tools?
- [ ] Analyze scenarios using ethical reasoning?
- [ ] Provide real-world examples of each ethical concern?  
- [ ] Make informed decisions about AI tool adoption?
- [ ] Advocate for ethical AI use in your context?

**Congratulations!** You have successfully completed Learning Objective 2.1.1 at the Acquire level.

---

**Remember:** Your role as an ethical educator is to protect and serve your students' best interests while embracing beneficial innovations. By applying these ethical frameworks consistently, you contribute to a more responsible and inclusive future for AI in technical and vocational education.

*Ready for the next level? Proceed to LO2.1.2 to deepen your understanding and develop practical skills for implementing ethical AI in your teaching practice.*
