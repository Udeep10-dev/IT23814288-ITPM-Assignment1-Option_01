# 🧪 IT3040 – ITPM Assignment 1
## Transliteration Accuracy Testing — Chat Sinhala (Singlish → Sinhala)

| Field | Details |
|---|---|
| **Student Name** | CHANDRASIRI S.H.U.G |
| **Registration Number** | IT23814288 |
| **Module** | IT3040 – IT Project Management |
| **Year / Semester** | Year 3 / Semester 1 |
| **Assignment** | Assignment 1 — Option 1 |

---

## 📌 Project Overview

This project automates the testing of the **Chat Sinhala transliteration** function available at:

🔗 [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)

The automation identifies **50 negative test cases** where the system fails to correctly convert chat-style Singlish input into Sinhala output. The test cases cover all **24 Singlish input types** defined in Appendix 1 of the assignment.

---

## 📁 Project Structure

```
test_automation/
│
├── test_automation.py          # Main Playwright automation script
├── Assignment 1 - Test cases.xlsx  # Excel file with all 50 test cases + results
└── README.md                   # This file
```

---

## ✅ Prerequisites

Make sure the following are installed on your system before running the tests:

- **Python** 3.12.10
- **Google Chrome** (recommended) — or Playwright will use its own Chromium

---

## ⚙️ Setup Instructions

### Step 1 — Extract the project

Save the ZIP file to your **D: drive** and extract it so the folder path is:

```
D:\test_automation
```

### Step 2 — Open Command Prompt

Press `Win + R`, type `cmd`, and hit Enter.

### Step 3 — Navigate to the project folder

```bash
cd /d D:\test_automation
```

### Step 4 — Install required dependencies *(one-time only)*

Run the following commands one by one:

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## ▶️ Running the Tests

Once dependencies are installed, run the automation script with:

```bash
python test_automation.py --excel "test_automation/Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Command Arguments Explained

| Argument | Value | Description |
|---|---|---|
| `--excel` | `"test_automation/Assignment 1 - Test cases.xlsx"` | Path to the Excel test case file |
| `--url` | `"https://www.pixelssuite.com/chat-translator"` | Target URL to test |
| `--wait-ms` | `5000` | Wait time (ms) after each input for translation to load |
| `--type-delay-ms` | `80` | Delay (ms) between each keystroke |
| `--slow-mo-ms` | `200` | Slow motion delay (ms) for browser actions |
| `--save-every` | `1` | Save results to Excel after every test case |
| `--keep-open` | *(flag)* | Keeps the browser open after tests complete |

---

## 📊 Checking Results

After the script finishes:

1. Navigate to the `test_automation` folder
2. Open **`Assignment 1 - Test cases.xlsx`**
3. Verify the **`Actual output`** and **`Status`** columns — these are filled automatically by the script

---

## 🗂️ Test Case Coverage

The 50 negative test cases cover all **24 Singlish input types**:

| # | Input Type |
|---|---|
| 1 | Question forms |
| 2 | Command forms |
| 3 | Greetings |
| 4 | Requests |
| 5 | Responses |
| 6 | Repeated Words |
| 7 | Inputs with Punctuation Marks |
| 8 | Romanization / Spelling Variants |
| 9 | Isolated English Word Insertions in Singlish |
| 10 | Multi-Word English Phrases in Singlish |
| 11 | English Digital Terms in Singlish |
| 12 | Platform/App Names in Singlish |
| 13 | English Abbreviations/Acronyms in Singlish |
| 14 | English Clipped Forms in Singlish |
| 15 | Place Names Embedded in Singlish |
| 16 | Person Names Embedded in Singlish |
| 17 | Inputs with Numbers and Numeric Suffixes |
| 18 | Inputs with Currency |
| 19 | Inputs with Time Formats |
| 20 | Inputs with Dates |
| 21 | Inputs with Unit of Measurements |
| 22 | Inputs with Slang and Casual Phrasing |
| 23 | Online Identifiers in Singlish |
| 24 | Inputs Containing Emojis |

> All 50 test cases are **negative** — TC IDs follow the format `Neg_XXXX`.
> Each input type has **at least 2 test cases** as required.

---

## 📝 Notes

- The **Standard Sinhala** transliteration function, backend APIs, and performance/scalability/security testing are **out of scope**.
- The Excel file will be checked for plagiarism — similarity score must remain **below 10%**.
- Ensure the Git repository is **publicly accessible** before submission.

---



*BSc (Hons) in Information Technology — SLIIT | Year 3 | Semester 1*
