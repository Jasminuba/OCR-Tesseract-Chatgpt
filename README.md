# OCR-Tesseract-Chatgpt
A hybrid OCR pipeline combining Tesseract and GPT-4o for cleaning scanned Slovene folktales.
# OCR-Tesseract-ChatGPT

## ✨ Project Highlights

- Uses **Tesseract OCR** for initial character recognition.
- Applies **GPT-4o** via OpenAI API to fix OCR-induced errors.
- Evaluates improvements using **Word Error Rate (WER)** and **Character Error Rate (CER)**.
- Includes visual diffs between raw and corrected outputs.

---

## 📁 Folder Structure
📂 input_pdfs/ ← Your scanned PDF files
📂 ocr_results/ ← Folder for raw and corrected .txt files

---

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/OCR-Tesseract-ChatGPT.git
cd OCR-Tesseract-ChatGPT

## Install required packages
pip install pytesseract opencv-python matplotlib seaborn jiwer numpy pandas
## Set up Tesseract OCR
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
os.environ["TESSDATA_PREFIX"] = r"C:\Program Files\Tesseract-OCR\tessdata"
## Add OPENAI API KEY
export OPENAI_API_KEY="your-api-key-here"
