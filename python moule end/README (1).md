# 🎫 Customer Support Ticket Analyzer

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

A beginner-friendly Python project that manages customer support tickets using core data structures. It lets you add tickets interactively, cleans messy issue descriptions, and generates keyword and summary insights, all with the standard library only.

## 📑 Table of Contents

- [Features](#-features)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [How It Works](#-how-it-works)
- [Sample Output](#-sample-output)
- [Limitations](#-limitations)
- [Future Improvements](#-future-improvements)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)

## ✨ Features

- 📋 **Preloaded data:** 10 sample tickets to start with
- ➕ **Interactive entry:** add any number of new tickets with auto-incrementing ticket numbers
- ✅ **Input validation:** priority must be `High`, `Medium` or `Low` (case-insensitive)
- 🧹 **Text cleaning:** strips punctuation, lowercases, normalizes whitespace and replaces slang
- 🔍 **Keyword insights:** counts tickets containing specific words
- 📊 **Summary report:** priority breakdown, longest description and unique vocabulary

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook, JupyterLab or VS Code with the Jupyter extension

No `pip install` is needed, since the project only uses Python's built-in `string` module.

### Installation

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
jupyter notebook python_module_assn.ipynb
```

## 💻 Usage

1. Open `python_module_assn.ipynb`.
2. Run the code cell. The whole program lives in one cell.
3. When prompted, enter the number of new tickets to add (`0` to skip).
4. For each ticket, enter the customer name, issue description and priority.
5. Read the cleaned data and insights printed at the end.

## 🛠 How It Works

Tickets are stored as a **dictionary of lists**, where the same index across all lists refers to one ticket:

```python
ticket_data = {
    'Ticket_No': [...],
    'Customer_Name': [...],
    'Issue_Description': [...],
    'Priority': [...]
}
```

| Step | What happens |
|------|--------------|
| **1. Load** | Preloaded tickets are printed in a formatted table via `print_ticket_table()` |
| **2. Add** | The user adds new tickets. The next number is `max(existing) + 1` |
| **3. Clean** | `clean_text()` normalizes every issue description |
| **4. Keywords** | `count_tickets_with_word()` counts `poor`, `good`, `slow`, `excellent` |
| **5. Summarize** | Prints priority counts, the longest description and unique words |

### Text Cleaning Pipeline

1. Remove all punctuation
2. Convert to lowercase
3. Collapse extra whitespace and strip the ends
4. Replace slang using `SLANG_MAP`

| Slang | Replaced with |
|-------|---------------|
| `ok` | `okay` |
| `u` | `you` |
| `plz` | `please` |
| `asap` | `as soon as possible` |
| `bad` | `poor` |

> 💡 Add more entries to `SLANG_MAP` to extend the cleaning rules.

## 🖥 Sample Output

**Adding a ticket:**

```text
How many new tickets do you want to add? 1

Entering details for Ticket 11
  Customer Name: Priya
  Issue Description: Plz fix my WiFi ASAP!!
  Priority (High / Medium / Low): high
  Ticket 11 added successfully.
```

**Cleaned description:**

```text
please fix my wifi as soon as possible
```

**Final summary includes:**

- The cleaned ticket table
- Counts of High, Medium and Low priority tickets
- The ticket with the longest description (number, customer, text, word count)
- The count and sorted list of unique words

## ⚠️ Limitations

- Keyword matching is whole-word only (`slow` does not match `slowly`).
- Punctuation is removed without adding a space, so `service...quick` becomes `servicequick`.
- Slang is replaced after cleaning, and negation is not handled (`not bad` becomes `not poor`).
- Data lives in memory only and is lost when the program ends.

## 🔮 Future Improvements

- [ ] Save and load tickets from CSV or JSON
- [ ] Replace punctuation with spaces to avoid merged words
- [ ] Add basic sentiment scoring
- [ ] Use `pandas` for deeper analysis
- [ ] Split the notebook into reusable functions or modules

## 📁 Project Structure

```text
.
├── python_module_assn.ipynb   # Main notebook with the full program
└── README.md                  # Project documentation
```

## 🤝 Contributing

Suggestions and pull requests are welcome. Fork the repo, create a feature branch, and open a PR.

## 📄 License

Add a license of your choice (for example [MIT](https://choosealicense.com/licenses/mit/)) before publishing.
