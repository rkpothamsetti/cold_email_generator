# 🧠 Cold Email Generator using Llama 3.1

An end-to-end Gen AI application built to automate the cold email outreach process for software service companies. This tool leverages Llama 3.1 for fast and relevant email generation based on job postings scraped from the web. It integrates portfolio matching, semantic search, and web scraping into a Streamlit-powered interface.

---

## 📌 Key Features

- **Automated Email Generation**  
  Creates personalized cold emails based on scraped job descriptions and matched portfolio skills.

- **Web Scraping for Job Posts**  
  Extracts job role, required skills, and description from job posting URLs using a custom web loader.

- **Portfolio Matching**  
  Parses your portfolio CSV to dynamically reference matching skills and experience in the emails.

- **Prompt Engineering with LLM Chains**  
  Uses structured prompt templates to extract key details and generate email content with Llama 3.1.

- **Vector Store Integration (ChromaDB)**  
  Stores job post data in a semantic vector database for quick retrieval and relevance-based matching.

- **Streamlit Frontend**  
  User-friendly UI for job URL input, portfolio preview, and instant email generation.

- **Environment Security**  
  Keeps sensitive API keys safe using a `.env` file and `os.getenv()` access in code.

---

## 🗂️ Project Structure

```

app/
├── **pycache**/                  # Python bytecode cache
├── resource/
│   └── my\_portfolio.csv          # CSV file containing user skills & experience
│
├── app.py                        # Streamlit UI logic
├── chains.py                     # Prompt chains and LLM logic
├── portfolio.py                  # Portfolio processing and formatting
├── utils.py                      # Web scraping and helper functions
│
├── groq.ipynb                    # Notebook for API and model experimentation
├── requirements.txt              # Dependencies list
└── README.md                     # You're reading it!

````

---

## ⚙️ Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/cold-email-gen.git
   cd cold-email-gen
````

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Create `.env` File**

   ```
   LLAMA_API_KEY=your_llama_api_key
   ```

---

## 🚀 How to Use

1. **Prepare Your Portfolio**
   Add your skills and experience to `resource/my_portfolio.csv`.

2. **Launch the App**

   ```bash
   streamlit run app/app.py
   ```

3. **Generate Emails**

   * Input the job URL.
   * The system scrapes, parses, matches, and generates the cold email using Llama 3.1.

---

## 💡 Tech Stack

* **Llama 3.1** – Language model for generating emails and extracting info.
* **ChromaDB** – Vector database for storing and querying job posts.
* **Streamlit** – For building the web UI.
* **Python** – Core programming language.
* **dotenv** – For securely managing API keys.
* **BeautifulSoup / Requests** – For web scraping (assumed in utils).

---

## 📄 License

This project is for educational and non-commercial use. Feel free to adapt and extend it for your own learning or internal use.

---

## 🙌 Acknowledgements

Inspired by Merlin AI's Gen AI project tutorial and enhanced with custom portfolio and email generation logic.

```
