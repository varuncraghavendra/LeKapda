# Robots Trained to Fold Clothes

**Project by Chirag Sharma, Pratham Jain, and Shubhkarman Singh**

---

## What We Built

We built a robot that can fold clothes on its own! Think of it as teaching a robot the way you'd teach a child - by showing it how to do it over and over again. We used two robotic arms working together (just like using both your hands to fold a shirt), and after watching us fold clothes about 50 times, the robot learned to do it by itself.

The cool part? We used something called the ACT model (Action Chunking with Transformers), which basically helps the robot remember and copy the movements we showed it, making the folding motions smooth and natural.

---

## The Hardware We Used

### The Robot Arms - SO-101 (We Used 4 of Them!)
We used **four SO-101 robotic arms**. These are like really precise robot hands that can move in 6 different directions:
- **2 "Teacher" Arms**: We moved these arms ourselves to show the robot how to fold
- **2 "Student" Arms**: These copied what we did and actually folded the clothes

What makes these arms special:
- Strong motors that can move precisely
- Safe to work with - you can physically guide them with your hands
- Sensors that know exactly where they are at all times
- Small enough to fit on a table
- Grippers that can gently hold fabric without damaging it

---

## The Software & Tools

### LeRobot - Our Main Tool
[LeRobot](https://github.com/huggingface/lerobot) is a free, open-source tool made by Hugging Face. Think of it as a complete package that handles everything:
- Recording what we teach the robot
- Training the robot to learn from our demonstrations  
- Running different AI methods to help robots learn
- Connecting easily with robot hardware
- Visualizing the data we collect

LeRobot made everything easier - from recording our demonstrations to getting the robot working on its own.

### The Computer Power We Needed
- **NVIDIA H100 GPU**: A super powerful graphics card that made training much faster (like having a sports car instead of a bicycle)
- **NVIDIA AI Workbench (Brew)**: NVIDIA's software that helped us:
  - Set up everything quickly
  - Keep our work organized and repeatable
  - Run the training as fast as possible
  - Manage all the computing resources efficiently

---

## How We Taught the Robot

### Watch Us in Action!


### The Teaching Process
Here's how we collected the data to train our robot:

**Step 1: Setting Up the Arms**
   - We had two pairs of robot arms on a table
   - One pair (the "teacher" arms) we moved with our own hands
   - The other pair (the "student" arms) copied our movements in real-time and did the actual folding
   - We also set up cameras to record everything

**Step 2: Recording Demonstrations**
   - One of us would physically guide the teacher arms through the folding motions
   - The robot recorded everything - where each arm was, how fast it moved, whether the gripper was open or closed
   - The student arms followed along and actually folded the cloth
   - Cameras captured video from different angles
   - We did this about 50 times with different cloth positions and types

**Step 3: What Got Saved**
   - Every movement of all four arms
   - Whether the grippers were holding or releasing
   - Video footage from multiple angles
   - Timestamps for everything

This way of teaching is intuitive - instead of programming every single movement, we just showed the robot what to do, like teaching someone by example!

---

## Training the AI Brain

Once we collected all our demonstrations, we fed them into the ACT model (think of it as the robot's brain):

**What is ACT?**
- It's an AI model that's really good at learning complex movements that happen over time
- It can predict what the robot should do next based on what it sees
- It learns patterns from our demonstrations

**How We Trained It:**
- Used the powerful NVIDIA H100 GPU to process all the data quickly
- Fine-tuned settings to work best with our 50 demonstrations
- Added variations to the data so the robot could handle different situations
- Watched the progress using LeRobot's visualization tools to make sure it was learning properly

**What Makes It Work:**
- The robot learns to predict smooth, natural movements (not jerky or robotic)
- It uses camera images to understand what's happening
- It controls both arms together in a coordinated way

Even with just 50 demonstrations, the ACT model learned to fold clothes reliably!

---

## The Results

### See It in Action!

https://github.com/user-attachments/assets/0824a92a-9c56-4902-9450-c2472a67a28c

What the robot can now do:
- Pick up and fold clothes completely on its own
- Use both arms together smoothly
- Handle clothes that start in slightly different positions
- Execute clean, consistent folding motions

---

## What's Next?

We want to make this even better:
- Teach it to fold more types of clothes (towels, pants, etc.)
- Make it even more reliable
- Help it learn and adapt in real-time
- Add better cameras so it can see the cloth more clearly

---

*Want to know more or collaborate? Feel free to reach out to us!*
