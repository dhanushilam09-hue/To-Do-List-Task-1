# 📝 To-Do List Application

A simple, console-based task manager built in Python as part of my Python Programming Internship at **DecodeLabs**.

This was Project 1 of the internship — the goal was to get comfortable storing and managing multiple pieces of data (tasks) using core Python structures like lists and dictionaries, before moving on to anything database-related. It's a small project, but it covers a lot of the fundamentals that every backend feature eventually builds on.

---

## 💡 What it does

You run the script, and it gives you a simple menu in the terminal. From there you can:

- ➕ Add a new task — each one automatically gets a unique ID
- 📋 View every task, along with its status
- ✅ Mark a task as "Done" once you've finished it
- 🗑️ Delete a task by its ID
- 🔁 Keep doing all of the above in a loop, until you choose to exit

Nothing fancy on the surface — but under the hood it's handling structured data, input validation, and state, which is exactly the point of the exercise.

---

## ⚙️ How it's built

Each task isn't just a plain string — it's stored as a **dictionary** with three fields:

```python
{
    "id": 1,
    "name": "Finish Python assignment",
    "status": "Pending"
}
```

All of these dictionaries live inside one **list**, which acts as an in-memory table — basically a tiny database that only exists while the program is running.

### Concepts used
- **Functions** — every action (add, view, mark done, delete) is its own function, so the code stays organized and easy to read
- **Lists & Dictionaries** — the core data structure: a list of dictionaries, similar to rows in a database table
- **Loops** — a `while` loop keeps the menu running, and `for` loops go through the task list
- **Conditionals** — `if/elif/else` handles menu choices and task matching
- **Exception handling** — `try/except` catches invalid input (like typing letters where a number is expected) so the program doesn't crash
- **Global state** — the `next_id` counter uses the `global` keyword to keep generating unique IDs across function calls

---

## 📂 Project structure

```
Task-1-To-Do-List/
│
├── main.py
└── README.md
```

---

## ▶️ How to run it

**1. Clone the repository**
```bash
git clone <repository-link>
```

**2. Move into the project folder**
```bash
cd Task-1-To-Do-List
```

**3. Run it**
```bash
python main.py
```

That's it — no external libraries needed, just core Python.

---

## 💾 On data storage

Right now, everything is stored in RAM — meaning once you close the program, all your tasks disappear. That's intentional for this stage of the project; the focus was on getting the logic right (adding, viewing, updating, deleting) before worrying about making it permanent.

The natural next step — which I might tackle in a later version — would be saving tasks to a JSON file or a small SQLite database, so the list survives between runs.

---

## 🎯 Why this project matters

It's a small app, but it's really a stand-in for how almost every backend system works: you take some input, store it in a structured way, let the user look at it and change it, and eventually persist it somewhere permanent. Getting comfortable with lists, dictionaries, and clean function structure here makes the jump to real databases and APIs a lot less intimidating later on.

---

**Built by:** Dhanush
**Internship:** DecodeLabs — Python Programming Track
