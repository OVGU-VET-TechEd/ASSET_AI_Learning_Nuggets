# Lia Script Training Workshop - Quick Media Integration

## Workshop Overview
This condensed training sequence teaches participants how to quickly add multimedia elements to their Lia Script presentations. Each task focuses on essential skills with ready-to-use code snippets and includes text-to-speech narration for an interactive learning experience.

**Duration**: 20 minutes  
**Target Audience**: Educators, content creators, beginners in Lia Script  
**Prerequisites**: Basic understanding of markdown syntax

---

## Task 1: Adding Pictures (5 minutes)

--{{0}}--
Welcome to our first task! We'll start by learning how to add images to your Lia Script presentations.

--{{1}}--
Here are your instructions: First, copy the code block I'm about to show you. Then, paste it directly into the Lia Script live editor. Finally, observe how each image appears differently based on the syntax used.

### Quick Demo & Practice
**Instructions**: Copy and paste this code into the Lia Script live editor:

```markdown
# Images in Lia Script

--{{0}}--
Let me show you three ways to add images to your presentation.

## Basic Image
![Nature scene](https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=400)

--{{1}}--
This is the simplest way to add an image using markdown syntax.

## Styled Image
<img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=300" alt="Forest" style="width: 250px; border-radius: 10px;">

--{{2}}--
For more control over appearance, use HTML img tags with custom styling.

## Image Gallery
<div style="display: flex; gap: 10px;">
  <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=150" alt="Image 1" style="width: 100px; height: 100px; object-fit: cover;">
  <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=150" alt="Image 2" style="width: 100px; height: 100px; object-fit: cover;">
</div>

--{{3}}--
And here's how to create a simple image gallery using flexbox layout.
```

**Key Points**: 
- Use `![alt text](URL)` for basic images
- Use `<img>` tags for styling and sizing
- Create galleries with flexbox

--{{4}}--
Great! Now you know the three essential ways to add images. Let's move on to audio content.

---

## Task 2: Adding Audio Files (5 minutes)

--{{5}}--
Now let's explore audio integration. Audio can make your presentations more engaging and accessible.

--{{6}}--
For this task, your instructions are: Copy the audio code examples I'll show you, paste them into your editor below your previous image code, and then test each audio player by clicking on them to hear the difference between clickable and auto-playing audio.

### Quick Demo & Practice
**Instructions**: Add this audio code to your presentation:

```markdown
# Audio in Lia Script

--{{0}}--
There are two main ways to add audio to your presentations.

## Clickable Audio
?[Listen to this sound](https://www.soundjay.com/misc/sounds/bell-ringing-05.wav)

--{{1}}--
This creates a clickable audio player that users can control.

## Auto-playing Background Audio
!?[Background music](https://www.soundjay.com/misc/sounds/bell-ringing-05.wav)

--{{2}}--
This audio will start playing automatically when the slide loads.

## Audio with Quiz
?[Question audio](https://www.soundjay.com/misc/sounds/bell-ringing-05.wav)

--{{3}}--
You can also combine audio with interactive elements like quizzes.

After listening, choose the correct answer:

[[X]] Audio enhances learning
[[ ]] Audio is distracting
[[ ]] Audio is unnecessary

--{{4}}--
Perfect! Audio combined with interaction creates engaging learning experiences.
```

**Key Points**: 
- Use `?[title](URL)` for clickable audio
- Use `!?[title](URL)` for auto-playing audio
- Combine with interactive elements

--{{7}}--
Excellent! You've learned how to add both clickable and auto-playing audio. Next, we'll explore video integration.

---

## Task 3: Adding Video Files (5 minutes)

--{{8}}--
Now for the most engaging multimedia element - video! Videos can demonstrate complex concepts effectively.

--{{9}}--
Here are your instructions for this task: Copy the video code examples, paste them into your editor below your existing content, and then play each video to see how both direct video files and YouTube videos work within Lia Script. Don't forget to try the interactive quiz after the video!

### Quick Demo & Practice
**Instructions**: Add video content with this code:

```markdown
# Video in Lia Script

--{{0}}--
Video integration in Lia Script is straightforward and powerful.

## Embedded Video
!?[Sample video](https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4)

--{{1}}--
This embeds a direct video file that plays within your presentation.

## YouTube Video
!?[YouTube example](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

--{{2}}--
You can also embed YouTube videos using the same syntax.

## Video with Interaction
!?[Educational video](https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ElephantsDream.mp4)

--{{3}}--
After watching videos, you can add interactive elements to test comprehension.

Quick check - what did you see in the video?

[[ ]] A documentary
[[X]] An animated short
[[ ]] A tutorial

--{{4}}--
Great job! Video combined with interactive questions reinforces learning.
```

**Key Points**: 
- Use `!?[title](URL)` for videos
- Works with direct video files and YouTube
- Add interactive elements after videos

--{{10}}--
Wonderful! You now understand how to embed videos and combine them with interactions. Let's put it all together in our final task.

---

## Task 4: Quick Integration Practice (5 minutes)

--{{11}}--
Time for the final challenge! Let's create a complete multimedia presentation that combines everything you've learned.

--{{12}}--
Your instructions for this comprehensive task are: Copy the complete template code I'll provide, paste it into a new section of your editor, and then interact with all the elements - click the audio, watch the video, and answer the quiz question. This will show you how all multimedia elements work together in a single presentation.

### Hands-on Exercise
**Instructions**: Create a complete multimedia slide using this template:

```markdown
# My Multimedia Presentation

--{{0}}--
Welcome to my interactive multimedia presentation! Let me guide you through each section.

## Welcome Section
![Header image](https://images.unsplash.com/photo-1516321318423-f06f85e504b3?w=500)

--{{1}}--
This header image sets the visual tone for our presentation.

## Audio Introduction
?[Welcome message](https://www.soundjay.com/misc/sounds/bell-ringing-05.wav)

--{{2}}--
Click the audio player above to hear an introduction message.

## Video Content
!?[Main video](https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4)

--{{3}}--
This video demonstrates the main concepts we're exploring today.

## Visual Summary
<div style="display: flex; gap: 10px; justify-content: center;">
  <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=100" alt="Point 1" style="width: 80px; height: 80px; object-fit: cover;">
  <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=100" alt="Point 2" style="width: 80px; height: 80px; object-fit: cover;">
  <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=100" alt="Point 3" style="width: 80px; height: 80px; object-fit: cover;">
</div>

--{{4}}--
These images summarize our key learning points visually.

## Quick Assessment
What multimedia element do you find most effective?

[[ ]] Images only
[[ ]] Audio only
[[ ]] Video only
[[X]] Combined multimedia approach

--{{5}}--
Excellent choice! Research shows that combining multiple media types creates the most engaging and effective learning experience.
```

--{{13}}--
Congratulations! You've successfully created a complete multimedia presentation that includes images, audio, video, text-to-speech narration, and interactive elements.

---

## Key Takeaways & Next Steps

### Essential Syntax to Remember
--{{14}}--
Here are the key syntax patterns you'll use most often in Lia Script:

- **Images**: `![alt](URL)` or `<img src="URL" alt="alt" style="...">`
- **Audio**: `?[title](URL)` (clickable) or `!?[title](URL)` (auto-play)
- **Video**: `!?[title](URL)` (works with direct files and YouTube)
- **Text-to-Speech**: `--{{0}}--` followed by your text

### Quick Tips
--{{15}}--
Remember these important guidelines for effective multimedia presentations:

- Always include alt text for accessibility
- Test multimedia on different devices
- Keep file sizes reasonable
- Use consistent styling
- Number your text-to-speech segments sequentially

### Practice Assignment
--{{16}}--
Here's your homework challenge:

Create a 3-slide presentation using all multimedia elements. Focus on:
1. One slide with images and narration
2. One slide with audio and interaction
3. One slide with video and quiz

### Resources
--{{17}}--
For continued learning, explore these resources:

- Lia Script documentation
- Free media: Unsplash for images, YouTube for videos
- Test your presentations on different devices

--{{18}}--
Congratulations! You've completed the multimedia training. You now have the skills to create engaging, interactive presentations with images, audio, video, and text-to-speech narration. Time to practice and create amazing content!
