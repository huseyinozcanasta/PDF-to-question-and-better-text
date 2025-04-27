# TÖDS (Tıp Öğrencileri Destek Sistemi) - AI-Powered Document Processing Web Application

## Description
TÖDS is a Flask-based web application that allows users to upload various document types (PDF, DOC, DOCX, PPT, PPTX, TXT) and process them using Google Gemini AI. The app can rewrite the content in a clearer, more understandable way or generate challenging test questions based on the document content. The processed results are returned as downloadable Word documents (.docx).

## Features
- Upload multiple document formats: PDF, Word, PowerPoint, and text files.
- AI-powered content rewriting for better understanding.
- AI-generated challenging test questions based on the document.
- Download processed results as Word documents.
- Simple web interface with progress indicators.
- API key management for Google Gemini AI.

## Requirements
- Python 3.7+
- Flask
- python-dotenv
- google-generativeai
- PyPDF2
- python-docx
- python-pptx
- Werkzeug

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ai-ders
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv myenv
   myenv\Scripts\activate   # On Windows
   source myenv/bin/activate  # On Linux/macOS
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root and add your Google Gemini API key:
   ```
   GEMINI_API_KEY=your_api_key_here
   FLASK_SECRET_KEY=your_secret_key_here
   ```

## Usage

1. Run the Flask app:
   ```bash
   python app.py
   ```

2. Open your browser and go to:
   ```
   http://127.0.0.1:5000/
   ```

3. If you haven't set your API key yet, you will be redirected to the API key setup page.

4. Upload your document, select the desired processing options, and submit.

5. Download the processed Word document when ready.

## API Key Setup

- You can set or update your Google Gemini API key via the web interface at `/set_api_key`.
- The API key is stored in the `.env` file.

## Supported File Types

- PDF (.pdf)
- Microsoft Word (.doc, .docx)
- Microsoft PowerPoint (.ppt, .pptx)
- Text files (.txt)

## Notes

- Ensure your API key is valid and has access to Google Gemini AI services.
- The app uses AI to generate content and questions, which may take some time depending on the document size.

## License

This project is licensed under the MIT License.
