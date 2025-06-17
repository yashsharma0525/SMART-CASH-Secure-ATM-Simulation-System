# SMART-CASH-Secure-ATM-Simulation-System
🔐 SMART CASH – Secure ATM System A C-based ATM simulation project with smart features like PIN authentication, note serial number tracking, secure deposit &amp; withdrawal, and a torn note reporting mechanism with note verification and replacement. Built for academic learning, security logic practice, and transaction simulation.

# 💳 SMART CASH – Secure ATM Simulation System

**SMART CASH** is a secure and intelligent C-based simulation of an ATM (Automated Deposit cum Withdrawal Machine) that offers smart features like serial number tracking, note verification, deposit/withdrawal handling, and **torn note replacement** – all in a terminal-based environment.

---

## 🚀 Features

- 🔐 **PIN Authentication** (`1520`) before access
- 💰 **Check Balance** – View current account balance
- 💸 **Withdraw Cash** – Smart denomination breakdown (₹500, ₹200, ₹100)
- 💵 **Deposit Cash** – With note validity simulation (~80% acceptance)
- 🧾 **Note Tracking System** – Unique serial number for each note (e.g., `SN12345`)
- 🧯 **Report Torn Note** – Verify and **replace damaged notes**, with **refund if it was deposited**
- ✅ **Valid Denomination Check** – Amounts must be multiples of ₹100
- 📜 **Transaction Logging in Memory** – Track up to 200 transactions
- 🖥️ **User-Friendly Terminal Interface**

---

## 🧠 How It Works

### 🔑 1. PIN Verification
User must enter the secure PIN (`1520`) to begin transactions.

### 🧾 2. Serial Number Tracking
Every deposited or withdrawn note is given a unique `SNXXXXX` ID and tracked in memory.

### 💳 3. Transactions
- **Withdraw**: Breaks down amount into 500/200/100 rupee notes, logs serial numbers.
- **Deposit**: Validates note (80% chance of success), logs the transaction if valid.
- **Report Torn Note**:
  - Enter the serial number of the damaged note.
  - If the note was **issued by this ATM**, it is verified.
  - A **replacement note** is issued with a new serial.
  - If the torn note was **originally deposited**, the amount is **credited back** to your balance.
  - Invalid or fake serials are **rejected** with an error.

### 💡 4. Denomination Validation
Only allows amounts that can be constructed from ₹100, ₹200, and ₹500 notes.

---

## 🧪 Requirements

- C Compiler (GCC or any standard C compiler)
- Works on Windows/Linux/MacOS terminals

---

## 🔧 How to Run

1. Copy the code into a file, e.g., `smart_cash_atm.c`
2. Compile:

```bash
gcc smart_cash_atm.c -o smartcash

## 🔄 Sample Workflow
> Enter PIN: 1520

> 1. Check Balance
> 2. Withdraw Cash
> 3. Deposit Cash
> 4. Report Torn Notes
> 5. Quit

> Choice: 4
> Enter Serial Number: SN23456

NOTE VERIFIED (WITHDRAWN 500 Rs NOTE)
REPLACEMENT NOTE GENERATED:
500 Rs NOTE: SN67891

## 🏷️ Project Info
Project Name: SMART CASH – Secure ATM System

Language: C (Procedural Programming)

Developer: Yash Sharma

License: Open for academic and personal use

## 🙌 Acknowledgements
Inspired by the idea of secure ATM machines with smart verification and accountable currency tracking to reduce fraud and increase customer trust.
