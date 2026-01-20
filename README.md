# Markdown to Google Docs Converter (Google Colab)

## 📌 Overview

This project is a Python-based automation tool that converts structured **markdown meeting notes**
into a **well-formatted Google Document** using the **Google Docs API**.
The solution is designed to run in **Google Colab** and demonstrates document automation,
API integration, and markdown parsing.

This project was developed as part of a **Full Stack Software Engineer assessment task**.

---

## 📂 Project Structure

```
MARKDOWN-TO-GDOC/
├── README.md
├── src/
│   ├── notes_to_google_doc.ipynb
│   └── notes_to_google_doc.py
└── sample_output/
    └── Product Team Sync.docx
```

### Folder Details

- **src/**
  - `notes_to_google_doc.ipynb`  
    Google Colab notebook to run and demonstrate the solution.
  - `notes_to_google_doc.py`  
    Core Python script for markdown parsing and Google Docs API integration.

- **sample_output/**
  - `Product Team Sync.docx`  
    Sample output document showing expected formatting.

---

## 🎯 Features

- Programmatically creates a Google Doc
- Converts markdown syntax to Google Docs formatting:
  - `#` → Heading 1
  - `##` → Heading 2
  - `###` → Heading 3
- Preserves nested bullet hierarchy with indentation
- Converts markdown checkboxes (`- [ ]`) into Google Docs checkboxes
- Styles assignee mentions (`@username`) with bold and color
- Applies distinct styling to footer information
- Uses batch updates for efficient API calls
- Includes error handling and clean code structure

---

## 🧱 Technology Stack

| Component | Technology |
|---------|-----------|
| Language | Python 3 |
| Platform | Google Colab |
| API | Google Docs API |
| Auth | Google OAuth (Colab built-in) |
| Libraries | google-api-python-client, google-auth |

---

## ⚙️ How to Run (Google Colab)

### 1. Open Notebook
Open the following file in Google Colab:

```
src/notes_to_google_doc.ipynb
```

### 2. Install Dependencies

```python
!pip -q install google-api-python-client google-auth google-auth-httplib2 google-auth-oauthlib
```

### 3. Authenticate Google Account

```python
from google.colab import auth
auth.authenticate_user()

import google.auth
creds, _ = google.auth.default()
```

### 4. Run the Script

- Execute all cells in the notebook
- A new Google Doc will be created automatically
- The document link will be printed in the output

---

## 📝 Markdown to Google Docs Mapping

### Headings

| Markdown | Google Docs |
|--------|-------------|
| `# Title` | Heading 1 |
| `## Section` | Heading 2 |
| `### Subsection` | Heading 3 |

### Checkboxes

Markdown:
```
- [ ] @sarah: Finalize roadmap
```

Converted to:
- Google Docs interactive checkbox
- Styled assignee mention

---

## 🔐 Authentication & Security

- Uses Google Colab’s secure OAuth flow
- No API keys or secrets are stored in the code
- Credentials managed by Colab runtime

---

## 🛠 Error Handling

- Try/except blocks for API calls
- Clear error messages
- Safe failure handling

---

## 📄 License

This project is provided for assessment and demonstration purposes only.

---

## 👤 Author

- Name: Thananchayan T.
- Role: Full Stack Software Engineer Candidate
