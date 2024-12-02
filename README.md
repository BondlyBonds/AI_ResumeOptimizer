
# AI-Powered Resume and Cover Letter Generator

This project is an AI-powered web application that generates ATS-friendly resumes and professional cover letters based on the user's input and a provided job description. The app ensures the resumes are optimized for Applicant Tracking Systems (ATS) and comply with professional standards.

---

## Features

- **ATS Optimization**: Automatically rewrites resumes to align with job descriptions and improve ATS scores.
- **Cover Letter Generation**: Creates tailored cover letters based on the resume and job description.
- **Template Integration**: Uses a professional Harvard CV template to format the resume and cover letter.
- **File Upload**: Supports `.pdf` and `.docx` file formats for input resumes.
- **Real-time ATS Score Calculation**: Displays ATS score improvements during the optimization process.
- **Download Options**: Allows downloading optimized resumes and cover letters in `.docx` format.
- **Error Handling**: Logs errors and provides meaningful feedback to the user.

---

## Prerequisites

1. **Python**: Install Python 3.8 or higher.
2. **Virtual Environment**: Use a virtual environment to manage dependencies.
3. **API Key**: Obtain an API key from [Groq](https://groq.com/) and set it in the script.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/resume-generator.git
   cd resume-generator
   ```

2. **Set Up the Virtual Environment**:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # macOS/Linux
   .venv\Scripts\activate     # Windows
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up API Key**:
   Open the `JobApp.py` file and replace the placeholder API key with your Groq API key:
   ```python
   groq_client = Groq(api_key="your_api_key_here")
   ```

5. **Add Templates**:
   - Place your Harvard CV template (`MAKE A COPY OF THE DOC - Harvard CV Template.docx`) in the `templates` directory.
   - Ensure the path to the template matches the script.

---

## Usage

1. **Start the Application**:
   ```bash
   python JobApp.py
   ```
   The app will run locally on `http://127.0.0.1:5000`.

2. **Navigate to the Web App**:
   Open your browser and go to `http://127.0.0.1:5000`.

3. **Generate Resume and Cover Letter**:
   - Upload your resume in `.pdf` or `.docx` format.
   - Paste the job description.
   - (Optional) Add extra information or instructions.
   - Click `Generate`.

4. **Preview Results**:
   - View the ATS-optimized resume and cover letter directly in the web app.
   - Check the ATS score.

5. **Download Files**:
   - Click the "Download Resume" or "Download Cover Letter" buttons to save the optimized documents.

---

## Project Structure

```plaintext
resume-generator/
├── templates/
│   ├── MAKE A COPY OF THE DOC - Harvard CV Template.docx
│   ├── index.html             # Web interface for the app
├── uploads/                   # Folder for uploaded/generated files
├── JobApp.py                  # Main Flask app script
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
└── job_application.log        # Log file (created at runtime)
```

---

## Key Dependencies

- **Flask**: Web framework for building the app.
- **Python-Docx**: For manipulating `.docx` files.
- **pdfplumber**: To extract text from `.pdf` resumes.
- **Groq**: API client for AI model integration.

---

## Troubleshooting

1. **Session Cookie Too Large**:
   - Ensure large data like files are stored on the server, not in the session.

2. **API Rate Limits**:
   - The app uses exponential backoff for handling API rate limits. Check the logs for retries.

3. **Missing Templates**:
   - Ensure the Harvard CV template exists in the correct directory with the expected name.

---

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request.

---

## Contact

For questions or issues, contact BondlyBonds@gmail.com.
