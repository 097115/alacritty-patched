# Budget Tracker TUI

<p align="center">
  <img src="budget_tracker_icon.png" alt="Budget Tracker Logo" width="150"/>
</p>

A fast, modern, and efficient Terminal User Interface (TUI) application for tracking your personal budget, built with Rust and Ratatui.

## 📚 Table of Contents

- [🖼️ Screenshots](#️-screenshots)
- [✨ Features](#-features)
- [🚀 Getting Started](#-getting-started)
- [⚡ Quick Start](#-quick-start)
- [⚙️ Settings & Configuration](#️-settings--configuration)
- [📁 Data & CSV Format](#-data--csv-format)
- [References](#references)

## 🖼️ Screenshots

<p align="center">
  <img width="928" alt="Screenshot 2025-04-15 at 11 44 08 PM" src="https://github.com/user-attachments/assets/ab47b560-f3ab-4f95-919f-5de58a828d0c" />
  <br><i>Main transaction view with summary bar and help</i><br><br>
  <img width="926" alt="Screenshot 2025-04-15 at 11 44 30 PM" src="https://github.com/user-attachments/assets/71aa516e-4917-41d8-9257-e837491a3bd9" />
  <br><i>Monthly summary with interactive chart and budget line</i><br><br>
  <img width="926" alt="Screenshot 2025-04-15 at 11 44 45 PM" src="https://github.com/user-attachments/assets/c230ee05-b69b-457f-b108-4afe6ee5aaa1" />
  <br><i>Category summary with expandable/collapsible categories</i><br>
</p>

## ✨ Features

- **Intuitive Terminal UI:** Manage your finances directly from your terminal with a clean, responsive interface (TUI).
- **Transaction Management:** Add, view, edit, and delete income and expenses.
- **Advanced Filtering:** Filter transactions by date, description, category, type, and amount (including advanced multi-field filters).
- **Categorization:** Built-in, hierarchical categories and subcategories for all transactions.
- **Summaries & Charts:** Visualize your spending/income by month and by category, with interactive charts and tables.
- **Budget Tracking:** Set a monthly target budget and see your progress (including a budget line in summary charts).
- **Data Persistence:** All data is stored locally in a configurable CSV file. Settings are saved in a config file.
- **Cross-Platform:** Runs on Windows, macOS, and Linux.
- **Keyboard-Driven:** Fully operable with keyboard shortcuts for every action and mode.
- **Robust CSV Support:** Flexible date parsing, easy import/export, and Excel compatibility.
- **Built with Rust:** Safety, speed, and reliability.

## 🚀 Getting Started

### Windows Installer (Recommended for Windows Users)

If you are on **Windows**, you can download and run the latest installer for a quick and easy setup. This is the simplest way to get started on Windows—no Rust or Cargo required!

- [Download the latest Windows installer from the Releases page](https://github.com/Feromond/budget_tracker_tui/releases)

### Prerequisites (for manual/cargo install)

- [Rust](https://www.rust-lang.org/tools/install) (includes `cargo`)

### Installation & Running

**Build and Run Manually:**

```bash
# Clone the repository
git clone https://github.com/Feromond/budget_tracker_tui
cd budget_tracker_tui

# Build the project (use --release for optimized build)
cargo build --release

# Run the executable
./target/release/Budget_Tracker
```

**Install Globally with Cargo (Recommended for Linux/macOS):**

```bash
# Navigate to the project directory
cd budget_tracker_tui

# Install the binary to Cargo's bin directory
cargo install --path .
```

After installation, the `Budget_Tracker` command should be available in your terminal directly.

_Optional Tip:_ For even quicker access, set up a shell alias:

```bash
# Example for bash/zsh (add to your .bashrc or .zshrc)
alias bt='Budget_Tracker'
```

Then, you can just type `bt` to launch the app.

## ⚡ Quick Start

1. **Launch the app:** `Budget_Tracker` (or `bt` if you set up the alias)
2. **Add a transaction:** Press `a`, fill in the fields, and press `Enter` to save.
3. **Navigate:** Use `↑`/`↓` to move, `e` to edit, `d` to delete, `f` to filter.
4. **View summaries:** Press `s` for monthly summary, `c` for category summary.
5. **Change settings:** Press `o` to open settings (change data file path, set target budget).
6. **Quit:** Press `q` or `Esc`.

## ⚙️ Settings & Configuration

- **Data File Path:**
  - The path to your `transactions.csv` file is configurable in-app (press `o` for settings).
  - Default locations: - **Linux:** `$XDG_DATA_HOME/BudgetTracker/transactions.csv` (usually `~/.local/share/BudgetTracker/transactions.csv`) - **macOS:** `~/Library/Application Support/BudgetTracker/transactions.csv` - **Windows:** `%APPDATA%\BudgetTracker\transactions.csv` (e.g.,
    `C:\Users\<YourUsername>\AppData\Roaming\BudgetTracker\transactions.csv`)
- **Target Budget:**
  - Set a monthly target budget in settings. This will show a budget line in summary charts.
- **Config File:**
  - The application's settings are saved in a `config.json` file, which is stored in your OS's **config directory**:
    - **Linux:** `~/.config/BudgetTracker/config.json`
    - **macOS:** `~/Library/Application Support/BudgetTracker/config.json`
    - **Windows:** `C:\Users\<YourUsername>\AppData\Roaming\BudgetTracker\config.json`
  - This is separate from the data file location, which is in your OS's data directory (see above).

## 📁 Data & CSV Format

- **CSV Columns:** `date, description, amount, transaction_type, category, subcategory`
- **Date Format:** Flexible! Accepts `YYYY-MM-DD`, `YYYY/MM/DD`, `DD/MM/YYYY`, or `DD-MM-YYYY`.
- **Transaction Type:** `Income` or `Expense` (case-insensitive, also accepts `i`/`e`)
- **Category/Subcategory:** Must match the built-in set of categories and subcategories provided by the application. Custom or arbitrary categories are not currently supported.
- **Import/Export:** You can edit the CSV in Excel/LibreOffice or import from other tools (just match the columns and use valid categories).
- **Data Safety:** The app will not overwrite your CSV unless you save a transaction, close the program, or change settings.

## References

**[Ratatui](https://ratatui.rs)**
**[Rust](https://www.rust-lang.org/)**
