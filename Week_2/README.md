<div align="center">

# 🐍 Week 2 — Python Programming Foundations
### Hope AI Master Program · Applied AI, Gen AI & Data Science

![Status](https://img.shields.io/badge/Status-✅%20Completed-brightgreen?style=for-the-badge)
![Module](https://img.shields.io/badge/Module-Python%20Foundations-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=for-the-badge&logo=python&logoColor=white)

> **Every AI engineer starts here.** Before models, before data pipelines, before agents — there is Python. This week is about building that foundation right, with deliberate hands-on practice.

</div>

---

## 🎯 Why Python First?

Python is the lingua franca of AI engineering. From data preprocessing to training neural networks to deploying LLM agents — Python is everywhere. Week 2 of the Hope AI Master Program focuses on building the core Python skills that every AI project depends on.

---

## 📂 Assignments Overview

| File | Topic | Concepts Practised |
|------|-------|--------------------|
| `Week2-Assignment1.ipynb` | **Control Structures** | if / elif / else, BMI classification, arithmetic operations |
| `week2-extraassignment1.ipynb` | **I/O & Arithmetic** | print, input, string handling, add / mul / div operations |
| `Week2-extraassignment2.ipynb` | **Python Practice** | Core Python problem solving |
| `week2-extraassignment3.ipynb` | **Conditionals & Validation** | if/else logic, password validation, user input handling |
| `week2extrassignment4.ipynb` | **Python Practice** | Additional problem solving exercises |
| `Welcome` | **Intro** | Course welcome and setup |

---

## 🧠 Concepts Covered

```
Python Week 2 — Skill Map
│
├── 📥 Input / Output
│       ├── print() — formatted output
│       ├── input() — user interaction
│       └── Type casting — int(), float(), str()
│
├── ➕ Arithmetic Operators
│       ├── Addition, Subtraction, Multiplication
│       ├── Division, Floor Division, Modulus
│       └── Operator precedence
│
├── 🔀 Control Structures
│       ├── if / elif / else — decision making
│       ├── Nested conditions
│       └── Comparison & logical operators (and, or, not)
│
├── 🏥 Real-World Application — BMI Calculator
│       ├── User input → float conversion
│       ├── Multi-condition classification
│       │       ├── Underweight  (BMI < 18.5)
│       │       ├── Normal Weight
│       │       ├── Overweight   (25–29.9)
│       │       ├── Class I Obesity  (30–34.9)
│       │       ├── Class II Obesity (35–39.9)
│       │       └── Class III Obesity (BMI > 40)
│       └── def check_bmi() — function definition
│
└── 🔐 Validation Logic
        ├── Password match checking
        └── Input-based conditional branching
```

---

## 💡 Key Assignments Deep Dive

### 📌 Assignment 1 — Control Structures & BMI Calculator
The main assignment puts conditionals into real use: a **BMI classifier** that takes user input and categorises obesity levels using if/elif/else chains — a perfect first taste of writing logic that mirrors clinical decision-making.

```python
def check_bmi(BMI):
    if BMI < 18.5:
        print("Underweight")
    elif 25 <= BMI <= 29.9:
        print("Overweight")
    elif 30 <= BMI <= 34.9:
        print("Class I Obesity")
    elif 35 <= BMI <= 39.9:
        print("Class II Obesity")
    elif BMI > 40:
        print("Class III Obesity")
    else:
        print("Normal Weight")
```

### 📌 Extra Assignment 3 — Validation Logic
Built a **password validator** using conditional logic — a foundational pattern that shows up in everything from web authentication to AI system prompt guards.

---

## 🛠️ Environment

```python
environment = {
    "Language"    : "Python 3.13",
    "IDE"         : "Jupyter Notebook (Anaconda / conda-base)",
    "Concepts"    : ["I/O", "Arithmetic", "Control Flow", "Functions", "Validation"],
}
```

---

## 📁 Folder Structure

```
Week_2/
├── Week2-Assignment1.ipynb       # Control structures + BMI Calculator
├── week2-extraassignment1.ipynb  # I/O & arithmetic operations
├── Week2-extraassignment2.ipynb  # Python practice problems
├── week2-extraassignment3.ipynb  # Conditionals & password validation
├── week2extrassignment4.ipynb    # Additional exercises
├── Welcome                       # Course intro
└── README.md                     # This file
```

---

## 💡 Key Learnings

- Python's simplicity is intentional — readability is a feature, not a shortcut
- Control structures are the logic engine of every program — mastering them early pays dividends across ML pipelines and agent workflows
- Real-world problems (like BMI classification) make abstract concepts stick
- Every line of code this week is practice for the data preprocessing and model logic that comes in Week 3+

---

<div align="center">

**← [Back to Main Repo](../README.md)**

*Week 2 of the Hope AI Master Program — Applied AI, Gen AI & Data Science 🚀*

</div>
