# 🐍🧹 py-chores

> **Automate the mundane.** A curated collection of bite-sized Python scripts to sweep away repetitive, everyday digital chores.

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=for-the-badge)
![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-orange?style=for-the-badge)

---

## 📖 About

We all have those small, annoying tasks we do every day—sorting a messy `Downloads` folder, batch-renaming photos, converting file formats, or scraping a quick piece of data. **`py-chores`** is my personal Swiss Army knife of lightweight, ready-to-run Python scripts built to put those daily errands on autopilot.

---

## 🗂️ Chore Directory

Scripts are organized by category so you can quickly find the tool you need:

### 📁 File & Folder Management
| Script | Description | Dependencies |
| :--- | :--- | :--- |
| [`downloads_janitor.py`](./file_management/downloads_janitor.py) | Automatically sorts files in your Downloads folder by extension into neat subfolders. | *Standard Library* |
| [`bulk_renamer.py`](./file_management/bulk_renamer.py) | Renames a batch of files using custom prefixes, dates, or regex patterns. | *Standard Library* |
| [`duplicate_finder.py`](./file_management/duplicate_finder.py) | Scans a directory and flags/removes duplicate files using MD5 hashes. | *Standard Library* |

### 🌐 Web & Media Utilities
| Script | Description | Dependencies |
| :--- | :--- | :--- |
| [`yt_audio_grabber.py`](./web_media/yt_audio_grabber.py) | Downloads audio in MP3 format from a given video URL. | `yt-dlp` |
| [`image_compressor.py`](./web_media/image_compressor.py) | Compresses PNG/JPG images in a folder without noticeable quality loss. | `Pillow` |
| [`price_tracker.py`](./web_media/price_tracker.py) | Checks a product page and sends a desktop notification when the price drops. | `requests`, `bs4`, `plyer` |

### 📄 Docs & Data Processing
| Script | Description | Dependencies |
| :--- | :--- | :--- |
| [`pdf_merger.py`](./docs_data/pdf_merger.py) | Combines multiple PDF files in a directory into a single document. | `pypdf` |
| [`csv_to_json.py`](./docs_data/csv_to_json.py) | Quickly converts CSV spreadsheets into formatted JSON files. | *Standard Library* |

*(💡 Tip: Replace the placeholder scripts above with your own as you build out the repository!)*

---

## 🚀 Getting Started

### Prerequisites
Make sure you have **Python 3.8+** installed on your machine. You can check your version by running:
```bash
python --version
```

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/duttashi/py-chores.git
   cd py-chores
   ```

2. **Create a virtual environment (optional, but recommended):**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install required dependencies:**
   Many scripts only use Python's built-in standard library, but for those that need external packages, install them via:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🛠️ Usage

Each script is self-contained and can be run directly from your terminal. Most scripts support the `--help` flag to show available arguments.

**Example: Running the Downloads Janitor**
```bash
python file_management/downloads_janitor.py --path "~/Downloads" --dry-run
```

---

## ⏰ Automating Your Chores (Pro-Tip)

Want these scripts to run without lifting a finger? Set them up on a schedule!

* **macOS / Linux (Cron):**
  Run `crontab -e` and add a line to run a script every day at 6:00 PM:
  ```cron
  0 18 * * * /usr/bin/python3 /path/to/py-chores/file_management/downloads_janitor.py
  ```
* **Windows:**
  Use **Task Scheduler** to trigger `python.exe` with the script path as the argument on login or on a daily timer.

---

## 🤝 Contributing

Have a handy script that saves you 5 minutes every day? Contributions are always welcome!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feat/new-chore-script`)
3. Commit your Changes (`git commit -m 'Add script for X'`)
4. Push to the Branch (`git push origin feat/new-chore-script`)
5. Open a Pull Request

**Guideline for new scripts:** Keep it simple, add a clear docstring at the top explaining what it does, and use `argparse` if it takes user inputs.

---

## 📜 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.
