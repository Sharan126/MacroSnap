# 🥗 MacroSnap

MacroSnap is an AI-powered nutrition assistant built with **Streamlit** and **Google Gemini**. Snap a photo of a meal or type a description, and MacroSnap provides an instant breakdown of estimated calories and macros (protein, carbohydrates, fat). When finished, send a complete summary of your conversation directly to your email inbox with one click.

---

## ✨ Features

- **Multimodal AI**: Upload food images or type meal descriptions.
- **Instant Macro Breakdown**: Estimates calories and macronutrients without complex diaries.
- **Conversational Memory**: Chat with the nutrition buddy naturally with follow-up questions.
- **Email Delivery**: Sends the full summary directly to your Gmail inbox via SMTP.
- **Fast & Responsive**: Powered by Google Gemini (`gemini-2.5-flash-lite`).

---

## 📁 Project Structure

```
macrosnap/
├── app.py                      # Core Streamlit application & logic
├── prompts.py                  # AI personality, system prompt & templates
├── requirements.txt            # Python dependencies
├── .gitignore                  # Keeps secrets and virtual environments out of Git
├── README.md                   # Project documentation
└── .streamlit/
    ├── secrets.toml.example    # Configuration template
    └── secrets.toml            # Private credentials (git-ignored)
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Sharan126/Macrosnap.git
cd Macrosnap
```

### 2. Set up virtual environment

**Windows (PowerShell):**
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Keys & Credentials

Copy the example secrets template:
```bash
cp .streamlit/secrets.toml.example .streamlit/secrets.toml
```

Edit `.streamlit/secrets.toml` and provide your credentials:
```toml
GEMINI_API_KEY = "your-gemini-api-key"
GMAIL_ADDRESS = "your-email@gmail.com"
GMAIL_APP_PASSWORD = "your-16-char-app-password"
```

> **Note on Gmail App Password**:
> 1. Enable 2-Step Verification in your Google Account.
> 2. Visit [Google App Passwords](https://myaccount.google.com/apppasswords).
> 3. Create an app password named `MacroSnap` and paste the 16-character code into `secrets.toml`.

### 5. Run the application

```bash
streamlit run app.py
```
Open [http://localhost:8501](http://localhost:8501) in your browser.
