<!--  
author: Hannes Tegelbeckers (hannes.tegelbeckers@ovgu.de)  
email: hannes.tegelbeckers@ovgu.de  
license: CC BY-NC-SA  
-->  

# Nugget 1: AI Basics – Understanding AI Techniques and Applications (Level 1: Acquire)

                          --{{0}}--
This module introduces the fundamentals of Artificial Intelligence and its applications, tailored for technical and vocational education and training teachers at the Acquire level of UNESCO's AI Competency Framework.

*Knowledge Acquisition* – This module introduces the fundamentals of Artificial Intelligence (AI) and its applications, tailored for technical and vocational education and training (TVET) teachers at the **Acquire** level of UNESCO's AI Competency Framework. By the end, you should grasp basic AI concepts, common techniques, and real-world examples relevant to vocational education. AI is transforming education and the teacher's role, so let's build foundational knowledge to engage with AI confidently.

## What *Is* Artificial Intelligence?

                          --{{0}}--
AI, or Artificial Intelligence, refers to computer systems capable of performing tasks that typically require human intelligence. These tasks include learning from data, recognizing patterns, making decisions, and even generating content.

*Knowledge Acquisition* – AI, or **Artificial Intelligence**, refers to computer systems capable of performing tasks that typically require human intelligence. These tasks include learning from data, recognizing patterns, making decisions, and even generating content. In simple terms, AI enables machines to **"think" or solve problems** in ways we associate with human thinking. For example, an AI can *learn* to recognize images of equipment, understand speech commands, or suggest personalized learning resources. Unlike traditional programs with fixed instructions, many AI systems can improve their performance with experience (data) – this is known as **machine learning**. AI is already part of daily life: whenever you see a movie recommendation pop up or use voice assistants like Siri/Alexa, you're witnessing AI in action.

> **Note:** According to UNESCO, the integration of AI in education is reshaping the classic classroom into a new *teacher–AI–student* dynamic. Understanding AI at a basic level will help you navigate this shift.

## Key AI Concepts and Techniques

                          --{{1}}--
To demystify AI, let's break down a few core concepts and techniques in simple terms. Think of algorithms as recipes and models as the learned knowledge from following those recipes.

     {{1}}
*Knowledge Acquisition* – To demystify AI, let's break down a few core concepts and techniques in simple terms:

     {{2}}
* **Algorithms and Models:** An *algorithm* is a step-by-step procedure or recipe for solving a problem. In AI, algorithms process data to produce an outcome. A *model* is the result of an AI algorithm learning from data – essentially, it's the learned pattern or "knowledge" that can make predictions.

     {{3}}
* **Machine Learning (ML):** The most common AI approach today. In ML, we feed examples (data) to a program so it can *learn* how to perform a task instead of explicitly programming every rule. For instance, rather than programming all rules to identify defective products, we can train an ML model with many examples of "defective" vs "good" products so it learns the distinguishing patterns. Two popular types of ML are:

       {{4}}
  * *Supervised Learning:* Learning from labeled examples (e.g. a dataset of symptoms **→** diagnosis, or part measurements **→** defect yes/no). The model tries to generalize so it can predict labels for new, unseen data.
  
       {{5}}
  * *Unsupervised Learning:* Finding patterns in unlabeled data (no given correct answer). For example, grouping students by learning behavior similarities, or clustering similar items together.

     {{6}}
* **Neural Networks:** A technique inspired by the human brain's neurons. Neural networks are used in many advanced AI applications (like image and speech recognition). At a basic level, think of it as a network of interconnected simple units that collectively learn complex patterns. (At Acquire level, you don't need to dive into the math – just know this is a key technique behind many "smart" systems.)

     {{7}}
* **Rule-Based AI:** Before the rise of learning algorithms, many AI systems were based on predefined rules (if-then logic). For example, an expert system might have a rule like "IF engine temperature is high AND oil pressure is low, THEN recommend checking the cooling system." These are still used in cases where expert knowledge can be coded explicitly. However, rule-based systems don't learn from new data on their own.

                          --{{8}}--
Knowing these basics allows you to understand what an AI tool is doing. For instance, if a student asks how a learning app predicts their weaknesses, you'll know it's likely using a machine learning model trained on many other students' data to find patterns.

     {{8}}
**Why does this matter for teachers?** Knowing these basics allows you to understand what an AI tool is doing. For instance, if a student asks how a learning app predicts their weaknesses, you'll know it's likely using an ML model trained on many other students' data to find patterns. This foundational literacy is the first step in UNESCO's *Acquire* level competencies.

## Examples of AI Applications

                          --{{0}}--
AI isn't a futuristic concept; it's already widely used across industries and daily life. Let's explore some relatable examples that you might encounter in vocational education.

*Knowledge Acquisition* – AI isn't a futuristic concept; it's already widely used across industries (including vocational fields) and daily life. Here are some relatable examples:

     {{1}}
* **Smart Assistants and Chatbots:** Tools like Siri or Alexa use AI to understand speech and respond. In education, AI chatbots can answer frequently asked questions for students or even help with tutoring by simulating conversation.

     {{2}}
* **Recommendation Systems:** Ever noticed how Netflix or YouTube suggests content you might like? That's AI analyzing your past choices to recommend movies or tutorials. A vocational training platform might similarly recommend courses or exercises based on a learner's progress.

     {{3}}
* **Quality Control in Manufacturing:** In many technical fields, AI-driven camera systems inspect products on assembly lines, automatically detecting defects. This uses image recognition algorithms – an AI model has been trained on many images of "good" vs "bad" products. For example, an AI camera can flag faulty circuit boards or poor welds much faster than a manual inspection.

     {{4}}
* **Predictive Maintenance:** AI can predict when machines might fail by analyzing sensor data (temperature, vibration, etc.). In automotive or industrial machine training, students might encounter AI systems that warn technicians of likely issues *before* breakdowns occur.

     {{5}}
* **Personalized Learning:** Educational AI software can adapt to each learner. If a student struggles with a certain topic, the AI can provide additional exercises or hints. This is common in e-learning platforms for IT training, language learning apps, etc. The AI *learns* from the student's performance and adjusts difficulty accordingly.

     {{6}}
* **Translation and Accessibility:** AI-driven translation (like Google Translate) and speech-to-text or text-to-speech tools help break language barriers and assist learners with disabilities. For instance, an AI can live-caption a technical demonstration or translate an English tutorial into Spanish for students.

                          --{{7}}--
These applications highlight how AI techniques are applied in practice. They also show why even basic AI knowledge is valuable for vocational educators – from understanding industry tools to enhancing your teaching with AI-powered resources.

     {{7}}
These applications highlight how AI techniques are applied in practice. They also show why even basic AI knowledge is valuable for vocational educators – from understanding industry tools to enhancing your teaching with AI-powered resources.

                          --{{8}}--
Here's a short video that explains what AI is in simple terms, highlighting some uses of AI in about 5 minutes.

     {{8}}
**Embedded Video – AI Basics:** Here's a short video that explains "What is AI?" in simple terms, highlighting some uses of AI in about 5 minutes:

!?[What is Artificial Intelligence? (5-min Video)](https://www.youtube.com/watch?v=ad79nYk2keg)

*(If the video doesn't play, you can find "What is Artificial Intelligence? | AI in 5 Minutes (Simplilearn)" on YouTube.)*

## Simple AI in Action (Editable Code)

                          --{{0}}--
Let's solidify our understanding by seeing a very basic AI example in code. Don't worry, you don't need to be a programmer – we'll explain what's happening step by step.

*Knowledge Deepening* – Let's solidify our understanding by seeing a **very basic AI example** in code. Don't worry, you don't need to be a programmer – we'll explain what's happening. The following Python code trains a **simple AI model** to make a prediction. We'll simulate a scenario: predicting whether a machine is likely to fail soon based on its age and daily usage. This mimics how AI might be used in predictive maintenance. Feel free to run the code and even tweak the input values to see how the prediction changes.

```python
# Simple AI example: Predictive Maintenance (Decision Tree)
# Feature 1: machine age (years), Feature 2: daily usage (hours)
# Label: 1 = "Likely to fail soon", 0 = "Not likely to fail soon"

# Sample training data: [age, hours] -> label
training_data = [
    [1, 2],   # A 1-year-old machine used 2h/day -> (assume) not failing
    [2, 5],   # 2-year-old, 5h/day -> not failing
    [5, 8],   # 5-year-old, 8h/day -> likely failing
    [7, 3],   # 7-year-old, 3h/day -> likely failing (old machine)
    [3, 7],   # 3-year-old, 7h/day -> likely failing (heavy use)
    [4, 4]    # 4-year-old, 4h/day -> not failing (moderate conditions)
]
labels = [0, 0, 1, 1, 1, 0]  # Corresponding outcomes

# Train a simple decision tree classifier on the data
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier(max_depth=2, random_state=0)
model.fit(training_data, labels)

# Try a prediction for a new machine scenario:
new_machine = [[4, 6]]  # e.g., 4-year-old machine, 6h usage per day
prediction = model.predict(new_machine)[0]
print("Machine status prediction:", 
      "Likely to FAIL soon!" if prediction == 1 else "Not likely to fail yet.")
```

                          --{{1}}--
After running, you'll see the model's prediction for the example input. Try changing the values in new_machine to represent different scenarios and re-run the code.

After running, you'll see the model's prediction for the example input. **Try This:** Change the values in `new_machine` to represent different scenarios and re-run:

     {{1}}
* Example: a brand new machine `[0, 8]` (0 years old, 8h/day) – the model will likely say "Not likely to fail" because it's new, despite heavy use.

     {{2}}
* Example: an old lightly-used machine `[8, 2]` – the model might predict failure due to age.

                          --{{3}}--
This toy example demonstrates machine learning at a very basic level: we gave the model some examples of data about machines and it learned simple rules to predict the label.

     {{3}}
This toy example demonstrates machine learning at a very basic level: we gave the model some examples (data about machines) and it "learned" simple rules to predict the label. In real life, of course, much more data and tuning would be needed! But even this small demo shows how an AI can capture patterns (in this case, that higher age or very high usage correlates with failures in our sample data).

                          --{{4}}--
As an educator, you don't need to write AI algorithms, but understanding the input-output nature of models helps. For instance, if an AI tool predicts something about your students or equipment, you'll consider: What data was it trained on? Could it be biased or missing context?

     {{4}}
**Reflection:** As an educator, you don't need to write AI algorithms, but understanding the input-output nature of models helps. For instance, if an AI tool predicts something about your students or equipment, you'll consider: *What data was it trained on? Could it be biased or missing context?* Those are great questions at the Deepen/Create stages, but for now, you've taken the first step by seeing an AI model in action. 🎉

## Knowledge Check (Quiz)

                          --{{0}}--
Test your understanding of basic AI concepts with a quick quiz. Take your time and think through each question carefully.

*Knowledge Acquisition* – Test your understanding of basic AI concepts with a quick quiz.

**Quiz 1:** Which of the following best describes what "machine learning" means?

                          --{{1}}--
Machine learning is when a computer program improves at a task by learning from data, rather than by explicit programming. This is different from just having a fast computer or robotic machinery.

? Machine learning is…
[[ ]] …any computation done by a very fast machine or supercomputer.
[[ ]] …a robot that learns how to operate machinery in a factory.
[[ ]] …software that is installed on a computer to make it run faster.
[[X]] …when a computer program improves at a task by learning from data, rather than by explicit programming.

**Quiz 2:** Which scenario is **not** an example of AI in everyday life?

                          --{{2}}--
A digital clock that changes from day to night mode on a fixed schedule is pre-programmed with a fixed rule. It doesn't adapt or learn from new information, so it's not considered artificial intelligence.

? Select the option that is *not* driven by AI.
[[ ]] An email spam filter that moves junk mail to a spam folder.
[[X]] A digital clock that changes from day to night mode on a fixed schedule.
[[ ]] A navigation app that finds the fastest route using traffic data.
[[ ]] A voice assistant that can answer questions about the weather.

**Quiz 3:** Interactive Knowledge Check

                          --{{3}}--
Let's test your understanding with a more interactive approach. Can you match these AI applications with their descriptions?

What type of AI application would be most suitable for each scenario?

| Scenario | AI Application |
|----------|----------------|
| Detecting defective products on an assembly line | [[ Quality Control | (Computer Vision) | Predictive Maintenance | Chatbot ]] |
| Predicting when a machine needs repair | [[ Quality Control | Computer Vision | (Predictive Maintenance) | Chatbot ]] |
| Answering student questions automatically | [[ Quality Control | Computer Vision | Predictive Maintenance | (Chatbot) ]] |
| Personalizing learning content for each student | [[ Quality Control | Computer Vision | Predictive Maintenance | (Recommendation System) ]] |

*(The clock is pre-programmed with a fixed rule; it doesn't adapt or learn, so it's not "intelligent." The others use AI models or algorithms to adapt to data.)*

## Further Reading and Resources

                          --{{0}}--
Congratulations on completing the AI Basics module! If you're curious to learn more, here are some high-quality resources to continue your journey.

*Knowledge Acquisition* – Congratulations on completing the AI Basics module! If you're curious to learn more, here are some resources (free/open where possible) to continue your journey:

                            {{English Female |>}}
**************************************************
You've taken an important first step in understanding AI! The resources below will help you continue building your knowledge at your own pace.
**************************************************

     {{1}}
* **UNESCO's AI Competency Framework for Teachers (2024):** The framework defining *Acquire, Deepen, Create* levels and various AI competencies for educators. This can provide context on what to aim for as you progress beyond basics.

     {{2}}
* **Elements of AI – Free Online Course:** A beginner-friendly course on AI (University of Helsinki), providing a deeper dive into how AI works, ethics, and examples. Great for self-paced learning (available under a CC license).

     {{3}}
* **AI Literacy for Educators:** *AI 101 for Teachers* by Code.org – a series of short videos and tutorials demystifying AI in education (e.g., how AI models like ChatGPT work, and how to use them responsibly in class).

     {{4}}
* **Machine Learning for Kids:** A free tool that lets you and your students train simple machine learning models with a friendly interface. Useful if you want to introduce AI concepts in class without coding (by IBM, designed for education).

     {{5}}
* **Google Teachable Machine:** An easy, web-based tool to create simple AI models (e.g., recognize images or sounds) using your own examples. No coding required – a fun way to experiment with AI applications relevant to vocational projects.

                          --{{6}}--
All resources above are Open Educational Resources or provide free access, making them perfect for teachers who want to continue learning about AI.

     {{6}}
All resources above are Open Educational Resources (or provide free access) suitable for teachers. Remember, the key at the Acquire stage is to **build confidence and curiosity** about AI. You've taken a big step by covering the basics – well done! Keep exploring, and you'll be ready for the next level where we *deepen* these skills. 🚀

## Reflection and Next Steps

                          --{{0}}--
Before we conclude, take a moment to reflect on what you've learned and how you might apply this knowledge in your teaching practice.

     {{1}}
**Reflect on Your Learning:**

? What was the most surprising thing you learned about AI today?
[[ ]]

? How might you explain AI to your students now?
[[ ]]

? Which AI application mentioned do you think would be most relevant to your subject area?
[[ Quality Control in Manufacturing | Predictive Maintenance | Personalized Learning | Translation and Accessibility | Recommendation Systems | Smart Assistants ]]

                          --{{2}}--
These reflections will help you connect the theoretical knowledge with practical applications in your teaching context.

     {{2}}
These questions help you connect what you've learned to your specific teaching context. There are no right or wrong answers – it's about making the content relevant to your professional practice.

                            {{Australian Male |>}}
************************************************
Remember, becoming comfortable with AI is a journey, not a destination. You're now equipped with the foundational knowledge to confidently engage with AI concepts and tools in your educational practice.
************************************************

*This module is licensed under **CC BY-NC-SA** (Attribution-NonCommercial-ShareAlike), which means you may reuse and adapt it for non-commercial purposes as long as you credit the author.*