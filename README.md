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
"Create a function that can take user inputs such as ‘Finish assignment by 9 PM’ or ‘Buy vegetables at 5 PM’ and store them with a category like Work, Personal, or Shopping. It should also display tasks grouped by category."
**AI Response:**
```python
tasks = {}

def add_task(task, time, category="General"):
    if category not in tasks:
        tasks[category] = []
    tasks[category].append({"task": task, "time": time})
    print(f"Added: '{task}' at {time} under category '{category}'")

def show_tasks():
    if not tasks:
        print("No tasks added yet!")
    else:
        print("Today's Tasks by Category:")
        for category, items in tasks.items():
            print(f"\n{category}:")
            for entry in items:
                print(f" - {entry['task']} at {entry['time']}")

```
add_task("Buy vegetables", "5 PM", "Shopping")
add_task("Complete assignment", "9 PM", "Work")
add_task("Evening walk", "7 PM", "Personal")
show_tasks()


### Output:
Added: 'Buy vegetables' at 5 PM under category 'Shopping'
Added: 'Complete assignment' at 9 PM under category 'Work'
Added: 'Evening walk' at 7 PM under category 'Personal'

Today's Tasks by Category:

Shopping:
 - Buy vegetables at 5 PM

Work:
 - Complete assignment at 9 PM

Personal:
 - Evening walk at 7 PM


### 2. Smart Scheduler

### Prompt:
"Create a function that evaluates a user’s schedule and recommends the best available free slot for a 1-hour break."
### AI Response:
```py
from datetime import datetime

schedule = [
    ("Morning Exercise", "06:00", "07:00"),
    ("Office Work", "09:00", "12:00"),
    ("Lunch Break", "12:00", "01:00"),
    ("Team Discussion", "02:00", "03:00")
]

def suggest_break_slot(schedule):
    print("Analyzing schedule for a free 1-hour break slot...")

    # Convert time to numeric hours for easy comparison
    intervals = [(int(s[1].split(":")[0]), int(s[2].split(":")[0])) for s in schedule]

    # Check between 07:00 and 09:00
    if (7, 9) not in intervals:
        print("Suggested break: 07:00 AM to 08:00 AM")
    # Check between 01:00 and 02:00
    elif (13, 14) not in intervals:
        print("Suggested break: 01:00 PM to 02:00 PM")
    else:
        print("No suitable break slot found!")

suggest_break_slot(schedule)

```

### Output:

Analyzing schedule for a free 1-hour break slot...
Suggested break: 07:00 AM to 08:00 AM


### 3. Wellness Tips Generator

### Prompt:
"Write a function that returns a random mental-health wellness tip whenever the user requests one. Keep it positive and uplifting."
### AI Response:
```py
import random

mental_tips = [
    "Take a moment to appreciate something good around you.",
    "You are doing better than you think — keep going!",
    "Pause and take three slow, deep breaths.",
    "Write down one thing you're grateful for today."
]

def get_mental_tip():
    print("Wellness Tip:", random.choice(mental_tips))

get_mental_tip()

```
### Output:

Wellness Tip: You are doing better than you think — keep going!

### 4. General Query Assistant

### Prompt:
"Create a simple chatbot that can answer general queries like ‘What is Python?’ or ‘Tell me a fun fact.’ The responses should be short and friendly."
### AI Response:
```py
def chat_reply(user_input):
    replies = {
        "what is python": "Python is a popular programming language used for web apps, AI, and automation.",
        "fun fact": "Honey never spoils — archaeologists found edible honey in ancient tombs!",
    }
    key = user_input.lower()
    print(replies.get(key, "Sorry, I don’t know that yet, but I'm learning!"))

```
# Example

chat_reply("What is Python")
chat_reply("Fun fact")


### Output:

Python is a popular programming language used for web apps, AI, and automation.
Honey never spoils — archaeologists found edible honey in ancient tombs!


# Result: 
The experiment successfully led to the development of a functional prototype of a personal assistant application powered by large language models. Through this exercise, students were able to:

Understand how to design and customize LLM prompts for practical, real-world use cases.

Enhance creativity by building assistant features tailored to their personal, academic, or productivity needs.

Apply prompt engineering techniques to achieve more accurate, meaningful, and context-aware AI responses.

Recognize the flexibility, effectiveness, and real-life usefulness of generative AI in organizing tasks, giving recommendations, answering questions, and supporting daily activities.
