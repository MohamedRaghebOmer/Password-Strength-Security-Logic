# 🔐 Password Strength Checker

A Windows Forms application that evaluates password strength in real time and estimates how long it would take to crack a given password using brute-force techniques.

> ⚠️ This project was designed, planned, and implemented entirely from scratch with no external guidance or templates.

---

## 🚀 Features

- **Real-time password strength evaluation**
  - Very Weak
  - Weak
  - Medium
  - Strong
  - Very Strong

- **Dynamic UI feedback**
  - Background color changes based on strength
  - Strength label with color indicators
  - Character-type indicators (Lowercase, Uppercase, Numbers, Symbols)

- **Time to Crack Estimation**
  - Calculates the theoretical brute-force time
  - Displays time in human-readable formats:
    - Seconds, Minutes, Hours, Days
    - Years, Centuries, Millennia
    - Million / Billion years (scientific notation for extreme cases)

- **Show / Hide password option**

- **Common password detection**
  - Detects weak patterns like:
    - Common words
    - Repeated characters
    - Keyboard patterns
    - Names and years

---

## 🧠 How It Works

### 1. Password Analysis
The password is analyzed for:
- Length
- Character diversity:
  - Lowercase letters
  - Uppercase letters
  - Numbers
  - Symbols

### 2. Strength Classification
Strength is determined using a custom rule-based system that considers:
- Password length
- Number of character types
- Uniform character usage
- Common password patterns

### 3. Time-to-Crack Calculation
- Uses the formula: `attempts = (possible_characters) ^ password_length`
- Assumes:
- **1 billion attempts per second**
- Converts the result into readable time units
- Uses logarithmic calculations to safely handle extremely large values

---

## 🎨 UI Feedback System

| Strength       | Color        |
|---------------|-------------|
| Very Weak     | Red         |
| Weak          | Orange      |
| Medium        | Yellow      |
| Strong        | Light Green |
| Very Strong   | Dark Green  |

Each change happens instantly as the user types.

---

## 🛠 Technologies Used

- **Language:** C#
- **Framework:** .NET (Windows Forms)
- **IDE:** Visual Studio
- **Paradigm:** Structured & modular design

---

## 📂 Project Structure

- Password analysis logic is separated into clear functions
- UI updates are handled through dedicated update methods
- Strength calculation and time estimation are fully decoupled from the UI

This structure allows:
- Easy maintenance
- Fast feature additions
- Clean readability

---

## 💡 Design Philosophy

This project prioritizes:
- Planning before coding
- Readability over shortcuts
- Logical separation of concerns
- Real-time user feedback

> Most of the development time was spent on designing the structure and logic before writing the final code — resulting in a clean and scalable implementation.

---

## ⚠️ Disclaimer

- The "Time to Crack" feature is an **estimation**, not a guarantee.
- Real-world cracking speeds depend on:
- Hardware
- Attack method
- Hashing algorithms
- Security measures

This tool is intended for **educational and awareness purposes only**.

---

## ✨ Future Improvements

- Adjustable attack speed (CPU / GPU / Cluster)
- Password improvement suggestions
- Progress bar or visual strength meter
- Export analysis report
- Unit tests for core logic
