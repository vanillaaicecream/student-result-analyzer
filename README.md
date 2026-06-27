# Student Result Analyzer

A beginner Python project that reads student marks from a CSV file and generates a structured result report — with grades, SGPA, pass/fail status, and class statistics.

## Features

- Reads student data from a CSV file
- Calculates letter grades (O / A+ / A / B+ / B / C / F) based on MU-style grading
- Computes SGPA for each student (equal credit weightage)
- Flags PASS / FAIL based on minimum 40 marks per subject
- Prints a clean terminal report with class statistics and subject-wise averages

## Project Structure

```
student-result-analyzer/
├── data/
│   └── sample_marks.csv    # Input: student marks
├── analyzer.py             # Core logic: grades, SGPA, pass/fail
├── report.py               # Output: formatted terminal report
├── main.py                 # Entry point
└── README.md
```

## How to Run

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/student-result-analyzer.git
cd student-result-analyzer

# No external libraries needed — uses only Python built-ins
python main.py
```

## Sample Output

```
=================================================================
         STUDENT RESULT ANALYZER — SUMMARY REPORT
=================================================================

Student : Priya
Status  : PASS
SGPA    : 9.6   |   Average %: 91.6%
-----------------------------------------------------------------
Subject          Marks  Grade
------------------------------
Maths               92      O
Physics             88     A+
...
=================================================================
                     CLASS STATISTICS
=================================================================
Total Students : 5
Passed         : 3
Failed         : 2
Class Avg SGPA : 7.24
Class Topper   : Priya (91.6%)
```

## Tech Stack

- Python 3.x
- `csv` module (standard library — no pip install needed)

## Grading Scale

| Marks | Grade | Grade Point |
|-------|-------|-------------|
| 90–100 | O | 10 |
| 80–89  | A+ | 9 |
| 70–79  | A  | 8 |
| 60–69  | B+ | 7 |
| 50–59  | B  | 6 |
| 40–49  | C  | 5 |
| < 40   | F  | 0 |

## What I Learned

- Reading and parsing CSV files with Python's `csv.DictReader`
- Modular code design (splitting logic across multiple files)
- List comprehensions, dictionaries, and f-strings
- Basic statistical calculations (average, max)

---

*Built as part of my GSoC 2027 preparation journey.*
