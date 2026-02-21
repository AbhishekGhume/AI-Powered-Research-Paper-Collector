# 📄 AI-Powered Research Paper Collector

An automated n8n workflow that collects research papers based on user input, formats them into a structured Google Sheet, and sends the sheet to the user's email.

---

## 🎥 Working Demo
https://drive.google.com/file/d/1GHQg8oTy76OTHw88RXk_oJ1QTinQSMlm/view?usp=sharing

---

## 🚀 Features

* 📥 Collects user input via a public **Form Trigger**

  * Project Description
  * Number of Research Papers
  * User Email
* 🤖 Uses **Semantic Scholar API** to fetch research papers
* 🧠 Uses **Google Gemini LLM** to:

  * Generate a smart spreadsheet title
  * Summarize abstracts
* 📊 Creates and formats a **Google Sheet**

  * Adds headers: Title, Authors, Summery, Year, URL, IEEE Reference
  * Appends all paper data, formatted with proper citation
* 🔗 Makes the sheet publicly accessible
* 📧 Sends an email with the link to the generated sheet

---

## 🛠 Tech Stack

* [n8n](https://n8n.io/) (self-hosted)
* Google Sheets API
* Semantic Scholar API
* Google Gemini (PaLM) via LangChain plugin
* Gmail API

---

## 📂 Folder Structure

```
project-root/
├── README.md        # You're reading it
├── ai_agent.json  # Exported n8n workflow file
```

---

## 📦 Setup Instructions

1. **Import the workflow** into n8n via "Import from file"
2. Ensure the following credentials are set up in n8n:

   * `Google Sheets account`
   * `Google Gemini(PaLM) Api account`
   * `Gmail account`
3. Enable the following APIs in Google Cloud Console:

   * Google Sheets API
   * Google Drive API
   * Gmail API
4. Deploy your n8n instance and test by submitting the public form

---

## ✨ Example Use Case

A student working on a project titled "IoT in Smart Agriculture" submits:

* Description: IoT in Smart Agriculture
* Number of papers: 5
* Email: [user@example.com](mailto:user@example.com)

The system will:

* Generate a sheet title like `Smart_Agri_IoT_Papers_2025`
* Create and populate a sheet with 5 relevant research papers
* Email the Google Sheet link to the student

---

## ✅ Output Example

| Title              | Authors                       | Research Papar Summery | Year | URL  | IEEE Reference                                                           |
| ------------------ | ----------------------------- | ---------------------- | ---- | ---- | ------------------------------------------------------------------------ |
| IoT in Agriculture | H. Gamido, M. Gamido, A. Siso | ...................... | 2024 | link | H. Gamido et al., "IoT in Agriculture", 2024. \[Online]. Available: link |

---


## 📬 Contact

Made with 💡 by Abhishek Ghume / https://github.com/AbhishekGhume

> For questions, feel free to reach out via issues or email.
