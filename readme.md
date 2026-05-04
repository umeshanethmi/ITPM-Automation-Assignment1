# Singlish to Sinhala Transliteration - Automation Test Suite

**Assignment:** IT3040 – ITPM Assignment 1, Option 1  
**University:** BSc (Hons) in Information Technology, Year 3

## Description
This project automates the testing of the Chat Sinhala transliteration function at [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator) using Playwright and Python. It tests 50 negative test cases where the system fails to correctly convert chat-style Singlish input into Sinhala output.

## 1. Project Structure
```text
.
├── IT23861718_Assignment1.xlsx
├── test_automation.py
├── readme.md
└── IT23861718_gitLink.txt
```

## 2. Prerequisites
- Python 3.x
- pip

## 3. Installation (one-time setup)
**Step 1:** Open a terminal or command prompt in the project's root directory.

**Step 2:** Run these commands to install the necessary packages:
```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

## 4. How to Run the Tests
You can run the test automation script in different ways depending on your needs.

### Basic Execution
To run the script with default settings (which will open a browser window), use this command:
```bash
python test_automation.py
```

### Running with a Visible Browser
To explicitly run the tests and see the browser automation in action, use the following command. This is useful for debugging.
```bash
python test_automation.py --excel "IT23861718_Assignment1.xlsx" --url "https://www.pixelssuite.com/chat-translator"
```

### Running in Headless Mode
For faster execution without a visible browser window, run the script in headless mode. This is ideal for automated environments.
```bash
python test_automation.py --excel "IT23861718_Assignment1.xlsx" --url "https://www.pixelssuite.com/chat-translator" --headless
```

## 5. What the Script Does
- Opens the chat translator website automatically.
- Reads Singlish test cases from `IT23861718_Assignment1.xlsx`.
- Inputs each test case into the website.
- Captures the actual Sinhala output.
- Compares the actual output with the expected output.
- Records "Pass" or "Fail" status in the Excel file.

## 6. Test Results
- Results are saved automatically in `IT23861718_Assignment1.xlsx`.
- The "Actual Output" and "Status" columns are filled in by the script.
- All 50 test cases are negative test cases and are expected to fail.

## 7. Notes
- Do not manually enter values in the "Actual Output" or "Status" columns.
- If the script has issues, you can adjust settings like `--wait-ms` in the `test_automation.py` file.
- The `--keep-open` flag can be added to the script's arguments to keep the browser open after the test run for debugging.

## Author Details
* **Name**: Nethmi P.P.U
* **Reg No**: IT23861718
