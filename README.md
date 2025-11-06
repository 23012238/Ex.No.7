# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Register no: 212223040214
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# AI Tools Required: 
- ChatGPT (Large Language Model)
- Python (for executing simple simulations)
- Optional: Jupyter Notebook or any Python IDE

# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."

Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.


### **1. Daily Task Manager**

**Prompt:**  
"Create a function that can accept user tasks like 'Remind me to call mom at 6 PM' and store them with time and priority."

**AI Response:**
```python
tasks = {}

def add_task(task, time, priority="Normal"):
    tasks[task] = {"time": time, "priority": priority}
    print(f"Task added: {task} at {time} [{priority}]")

def show_tasks():
    if not tasks:
        print("No tasks for today!")
    else:
        print("Today's Tasks:")
        for t, details in tasks.items():
            print(f"- {t} at {details['time']} ({details['priority']})")
```
# Example
add_task("Call mom", "6 PM", "High")
add_task("Finish report", "9 PM")
show_tasks()

### Output:

Task added: Call mom at 6 PM [High]
Task added: Finish report at 9 PM [Normal]
Today's Tasks:
- Call mom at 6 PM (High)
- Finish report at 9 PM (Normal)

### 2. Smart Scheduler

### Prompt:
"Write a simple function that checks for overlapping schedules and suggests free time slots."

### AI Response:
```py
from datetime import datetime

schedule = [("Team Meeting", "10:00", "11:00"), ("Project Work", "11:00", "12:00")]

def find_free_slots(schedule):
    print("Checking for free slots...")
    busy_hours = [s[1] for s in schedule]
    if "12:00" not in busy_hours:
        print("Free slot available after 12:00 PM!")
    else:
        print("No free slots found right now.")

find_free_slots(schedule)
```

### Output:

Checking for free slots...
Free slot available after 12:00 PM!

### 3. Wellness Tips Generator

### Prompt:
"Generate one wellness tip each time the user asks. Ensure it’s short and motivational."

### AI Response:
```py
import random

tips = [
    "Take a 10-minute walk to refresh your mind.",
    "Stay hydrated — drink a glass of water now!",
    "Take a deep breath and relax your shoulders.",
    "Give your eyes a break — look away from the screen for 20 seconds."
]

def get_tip():
    print("Wellness Tip:", random.choice(tips))

get_tip()

```
### Output:

Wellness Tip: Stay hydrated — drink a glass of water now!

### 4. General Query Assistant

### Prompt:
"Make a simple chatbot that answers general questions like 'What is AI?' or 'Give me a motivational quote.'"

### AI Response:
```py
def chat_response(user_input):
    responses = {
        "what is ai": "AI stands for Artificial Intelligence — systems that can think and learn like humans.",
        "motivational quote": "Believe in yourself — every expert was once a beginner.",
    }
    key = user_input.lower()
    print(responses.get(key, "I'm not sure, but I can look that up for you!"))
```
# Example
chat_response("What is AI")
chat_response("Motivational quote")


### Output:

AI stands for Artificial Intelligence — systems that can think and learn like humans.
Believe in yourself — every expert was once a beginner.

# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
