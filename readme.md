# Singlish to Sinhala Transliteration - Automation Test Suite

**Assignment:** IT3040 – ITPM Assignment 1, Option 1  
**University:** BSc (Hons) in Information Technology, Year 3

## Description
This project automates the testing of the Chat Sinhala transliteration function at [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator) using Playwright and Python. It tests 50 negative test cases where the system fails to correctly convert chat-style Singlish input into Sinhala output.

## 1. Project Structure
```text
test_automation/
├── IT23861718_Assignment1.xlsx
├── test_automation.py
├── Command.txt
└── README.md
```

## 2. Prerequisites
- Python 3.x
- pip

## 3. Installation (one-time setup)
**Step 1:** Open Command Prompt and navigate to the `test_automation` folder.

**Step 2:** Run these commands:
```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

## 4. How to Run the Tests
Run this command from the `test_automation` folder:
```bash
python test_automation.py --excel "IT23861718_Assignment1.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 8000 --type-delay-ms 80 --slow-mo-ms 300 --save-every 1 --keep-open
```

## 5. What the Script Does
- Opens the chat translator website automatically.
- Inputs each of the 50 Singlish test cases one by one.
- Captures the actual Sinhala output from the system.
- Compares actual output with expected output.
- Records Pass or Fail status in the Excel file automatically.

## 6. Test Results
- Results are saved automatically in `IT23861718_Assignment1.xlsx`.
- Actual output and Status columns are filled automatically.
- All 50 test cases are negative test cases (expected to Fail).

## 7. Notes
- Do NOT manually enter values in the Actual output or Status columns.
- Increase the `--wait-ms` value if the output does not update correctly.
- Keep the browser open after the run using the `--keep-open` flag.

## Author Details
* **Name**: Nethmi P.P.U
* **Reg No**: IT23861718
