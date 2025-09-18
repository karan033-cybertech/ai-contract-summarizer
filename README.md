# Legal Contract AI Assistant

An AI-powered legal contract analysis tool with Hindi language support using Hugging Face API.

## Features

- 📄 **Contract Upload**: Support for PDF, DOCX, and TXT files
- 🤖 **AI Analysis**: Powered by Hugging Face Meta-Llama-3.1-8B-Instruct model
- 🌐 **Bilingual Support**: English and Hindi responses
- 🔍 **Semantic Search**: Find relevant clauses and terms
- 💬 **Q&A Chat**: Ask questions about your contracts in Hindi or English

## Quick Start

### Option 1: One-Click Start (Recommended)
```powershell
# Run this from the project root directory
.\start_app.ps1
```

### Option 2: Manual Start

#### Start Backend Server
```powershell
# From project root
.\start_backend.ps1
```

#### Start Frontend Server
```powershell
# From project root (in a new terminal)
.\start_frontend.ps1
```

## Usage

1. **Open your browser** and go to `http://localhost:3000`
2. **Upload a contract** (PDF, DOCX, or TXT)
3. **Ask questions** in Hindi or English:
   - "What are the payment terms?" (English)
   - "भुगतान की शर्तें क्या हैं?" (Hindi)
   - "Explain the termination clause in Hindi" (Bilingual)

## Hindi Language Support

The chatbot supports Hindi in several ways:

- **Direct Hindi questions**: Ask questions in Hindi
- **Bilingual requests**: Ask for responses in both languages
- **Hindi keywords**: Use words like "हिंदी में", "हिंदी भाषा"

### Example Hindi Questions:
- "इस अनुबंध में क्या शर्तें हैं?"
- "भुगतान की शर्तें हिंदी में समझाएं"
- "दोनों भाषाओं में जवाब दें"

## API Configuration

The application uses your Hugging Face API key:
- **Model**: meta-llama/Meta-Llama-3.1-8B-Instruct
- **API Key**: Already configured in the startup scripts

## Testing

To test the API integration:
```powershell
python test_api.py
```

## Troubleshooting

### Upload Failed
1. Make sure the backend server is running on port 8000
2. Check that you're uploading supported file types (PDF, DOCX, TXT)
3. Ensure file size is under 20MB

### Hindi Not Working
1. Make sure the Hugging Face API key is set correctly
2. Try asking questions with Hindi keywords like "हिंदी में"
3. Check the test script: `python test_api.py`

### Server Won't Start
1. Make sure you're running the scripts from the project root directory
2. Check that Python and Node.js are installed
3. Install dependencies: `pip install -r backend/requirements.txt`

## File Structure

```
legal contract/
├── backend/                 # FastAPI backend
│   ├── app/
│   │   ├── api/            # API endpoints
│   │   ├── services/       # Business logic
│   │   └── main.py         # Server entry point
│   └── requirements.txt    # Python dependencies
├── frontend/               # Next.js frontend
│   ├── src/
│   │   └── pages/         # React components
│   └── package.json       # Node.js dependencies
├── start_app.ps1          # Main startup script
├── start_backend.ps1      # Backend startup script
├── start_frontend.ps1     # Frontend startup script
└── test_api.py           # API test script
```

## Technologies Used

- **Backend**: FastAPI, Python
- **Frontend**: Next.js, React, TypeScript
- **AI**: Hugging Face Inference API (Meta-Llama-3.1-8B-Instruct)
- **File Processing**: PDFPlumber, python-docx
- **Translation**: Deep Translator (LibreTranslate)

## Support

If you encounter any issues:
1. Check the console output for error messages
2. Run the test script: `python test_api.py`
3. Ensure all dependencies are installed
4. Make sure you're running from the correct directory

