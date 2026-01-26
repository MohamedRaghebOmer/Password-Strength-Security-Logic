# 🛡️ Password Strength & Security Logic Analyzer

This project is a deep dive into **Backend Logic** and **Security Algorithms** using C#. While it uses Windows Forms for the interface, the primary focus was to build a robust engine that can accurately evaluate password complexity beyond just checking the length.

---

## 🧠 Philosophy: Logic Over UI
In this project, I intentionally kept the **User Interface simple and clean**. The goal was to dedicate 100% of my focus to the **Underlying Logic**. I wanted to ensure that the scoring system is accurate, the common password detection is efficient, and the "Time-to-Crack" estimation is based on real-world entropy principles.

---

## 🚀 Key Technical Features (The "Brain" of the App)

- **🔍 Common Password Detection:** A built-in dictionary check to flag frequently used (and insecure) passwords like `123456`, `admin`, or `password`.
- **📊 Advanced Scoring Engine:** The logic evaluates four main criteria:
  - Character Variety (Uppercase, Lowercase, Numbers, Symbols).
  - Minimum & Optimal Length requirements.
  - Unique Character Ratio (to prevent repetitive patterns).
- **⏳ Time-to-Crack Estimation:** A complex algorithm that estimates how long it would take for a brute-force attack to break the password, providing a reality check for the user.
- **🎨 Dynamic Feedback Logic:** The UI reacts instantly to every keystroke, but the magic happens in the background where the logic recalculates the "Strength Level" and "Security Color" in real-time.

---

## 🛠 How the Logic Works

The core of the program resides in `CheckStrength()` and `CalculateTimeToCrack()` methods:
1. **Initial Filter:** Checks if the password is in the "Common Passwords" list.
2. **Point Accumulation:** Grants points for each security layer (e.g., adding a symbol adds X points).
3. **Entropy Calculation:** Uses the character set size and password length to determine the mathematical difficulty of cracking it.
4. **Final Evaluation:** Maps the final score to 5 levels: *Very Weak, Weak, Medium, Strong, Very Strong*.

---

## 📂 Technical Stack
- **Language:** C#
- **Framework:** .NET WinForms (used as a shell for the logic).
- **Paradigm:** Procedural Logic & Event-Driven UI.

---

## 🚀 How to Run
1. Clone the repo.
2. Open `PasswordStrengthChecker.sln` in Visual Studio.
3. Press `F5` to build and run the logic analyzer.

---

## 👨‍💻 Author
**Mohamed Ragheb**
*Focusing on the core logic to build more secure and efficient software.*

---
*If you value backend logic and algorithm design, feel free to give this repo a ⭐!*
