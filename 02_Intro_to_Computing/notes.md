# 🧠 INTRODUCTION TO COMPUTING

---

## 🧮 THE BINARY SYSTEM

**Binary** is the language computers use to communicate.  
Computers only understand **1s (ones)** and **0s (zeros)**.

---

### 🔢 Converting Numbers into Decimals

**Decimal** is a **Base 10** numbering system (0–9).

#### Steps:
1. Number the position of digits **from right to left** (starting at position 0).  
2. Multiply each digit by **10 raised to the power of its position**.  
3. Add all results together to get the decimal value.  
4. Remember: Any number raised to the exponent **0** equals **1**.

#### Example:
Decimal → Base 10 → (0,1,2,...9)
163 = (1 × 10²) + (6 × 10¹) + (3 × 10⁰)
= 100 + 60 + 3
= 163

| Position | 2 | 1 | 0 |
|-----------|---|---|---|
| Value     |100|10 |1  |

**Notes:**
- In computing, numbers often start with **0**.
- Each digit in Base 10 can represent up to 10 values (0–9).

---

## 💡 BINARY SYSTEM

**Binary** is a **Base 2** numbering system (only uses 0 and 1).

#### Example: Convert Binary to Decimal
Binary: 10100011
= (1 × 2⁷) + (0 × 2⁶) + (1 × 2⁵) + (0 × 2⁴) + (0 × 2³) + (0 × 2²) + (1 × 2¹) + (1 × 2⁰)
= 128 + 32 + 2 + 1 = 163


| Position | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----------|---|---|---|---|---|---|---|---|
| Value     |128|64 |32 |16 |8  |4  |2  |1  |

✅ **Binary → Decimal** = **163**

---

## 🧮 HEXADECIMAL SYSTEM

**Hexadecimal** is used to represent binary values more easily when dealing with large numbers.  
It is a **Base 16** system that uses digits **0–9** and letters **A–F**.

| Letter | Value |
|---------|--------|
| A | 10 |
| B | 11 |
| C | 12 |
| D | 13 |
| E | 14 |
| F | 15 |

#### Example:
Hexadecimal: A3
= (10 × 16¹) + (3 × 16⁰)
= 160 + 3
= 163


---

## 💾 BITS AND BYTES

- **Bit (Binary Digit):** The smallest unit of data (0 or 1).  
- **Byte:** 8 bits make up **1 byte**.  
- **Nibble:** 4 bits make up **1 nibble**.

🧠 *Tip:* Use the Windows Calculator → “Programmer” mode for binary/hex/decimal conversions.

---

## 🔡 ENCODING

**Encoding** is how computers turn text (letters, numbers, symbols) into numbers so they can be stored, read, and transmitted.

### 🅰️ ASCII (American Standard Code for Information Interchange)
A basic encoding system that assigns a number to each character.

| Character | ASCII Value |
|------------|--------------|
| A | 65 |
| a | 97 |
| 1 | 49 |
| Space | 32 |
| @ | 64 |

➡️ When you type **“A”**, the computer stores it as **65**.

---

### 🌍 UTF (Unicode Transformation Format)

**UTF** is a universal text encoding system that supports **letters, symbols, emojis, and languages** from all over the world.

Computers don’t understand letters like **é**, **中**, or **😊** — they only understand numbers.  
UTF converts these characters into numeric codes so computers can display them correctly.

🧠 Think of UTF as a **universal translator** that helps all computers understand text consistently.

---

## 🎨 VIDEO AND IMAGE ENCODING

For video and picture color encoding, use the RGB color system.

🔗 **Try it here:** [RGB Color Reference](https://www.rapidtables.com/web/color/RGB_Color.html)

---

## ⚙️ HOW COMPUTERS COMPUTE

### 🧠 CPU (Central Processing Unit)
The **brain** of the computer.  
It processes instructions and displays results on the monitor.

### 🔌 Transistors in the CPU
Tiny electronic switches that store binary data (1s and 0s).  
They hold temporary data in **internal registers** and can combine to form **logic gates**.

---

## 🧩 LOGIC GATES

Logic gates perform **Boolean Logic** — the foundation of all computer decisions.

### Common Gates

#### ✅ AND Gate
Works like multiplication:
| Input A | Input B | Output |
|----------|----------|--------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

*(True × False = False)*

#### ✅ OR Gate
Works like addition:
| Input A | Input B | Output |
|----------|----------|--------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

*(True + False = True)*

---

## 🧩 COMPILATION AND ABSTRACTION

### 📦 Compilation
A **compiler** converts code written by humans into **machine language** (binary) that computers can run.

Example:
1. Programmer writes code in **C++**.  
2. Compiler converts it into an **.exe** (executable file).  
3. The user runs the `.exe` file.

Most executable files have **magic numbers** — signatures that tell the computer what kind of file it is.

---

### 🧱 Abstraction

**Abstraction** means hiding unnecessary details and focusing on what matters.  
It’s how we simplify complex systems.

#### Why It Matters in IT Help Desk:
1. You’ll deal with complex systems (networks, printers, OS, etc.).  
2. Users only care about **solutions**, not technical details.  
3. Abstraction helps you troubleshoot **step-by-step**.

#### Example:
A user says: “I can’t access the Internet.”  
You don’t jump into coding or network configs immediately — you:
- Check if Wi-Fi is on.  
- See if other devices can connect.  
- Restart the router.

That’s **abstraction in action** — solving layer by layer.

---

📘 **End of Notes**

