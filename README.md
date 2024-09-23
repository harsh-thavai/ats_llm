# Smart ATS (Application Tracking System)

Demo: [https://atsllm.streamlit.app/](https://atsllm.streamlit.app/)


## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [AI Integration](#ai-integration)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Smart ATS is an innovative Streamlit application designed to assist job seekers in optimizing their resumes for specific job descriptions. By leveraging Google's Generative AI API, particularly the Gemini-pro model, this tool provides intelligent feedback on resume-job description compatibility. It aims to improve candidates' chances in the competitive job market by offering insights on resume matching, identifying missing keywords, and providing a concise profile summary.

## Features

- **Resume Upload**: Users can upload their resumes in PDF format.
- **Job Description Input**: A text area for pasting the target job description.
- **AI-Powered Analysis**: Utilizes Google's Gemini-pro model for advanced text analysis.
- **Comprehensive Feedback**:
  - Percentage match between resume and job description
  - List of missing keywords from the job description
  - AI-generated profile summary
- **User-Friendly Interface**: Built with Streamlit for an intuitive user experience.

## Technologies Used

- **Python**: The core programming language used.
- **Streamlit**: For creating the web application interface.
- **Google Generative AI**: Leveraging the Gemini-pro model for AI-powered analysis.
- **PyPDF2**: For parsing and extracting text from PDF resumes.
- **python-dotenv**: For managing environment variables.

## Installation

To set up the Smart ATS project locally, follow these steps:

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/smart-ats.git
   cd smart-ats
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Set up your Google API key:
   - Create a `.env` file in the project root.
   - Add your Google API key: `GOOGLE_API_KEY=your_api_key_here`

## Usage

To run the application:

1. Ensure you're in the project directory and your virtual environment is activated.

2. Run the Streamlit app:
   ```
   streamlit run app.py
   ```

3. Open your web browser and navigate to the local URL provided by Streamlit (usually `http://localhost:8501`).

4. Use the application:
   - Paste the job description in the provided text area.
   - Upload your resume in PDF format.
   - Click "Submit" to get the AI-generated analysis.

## Code Structure

The main application logic is contained in `app.py`. Here's a brief overview of its structure:

- **Imports and Setup**: Importing necessary libraries and configuring the Google AI API.
- **Helper Functions**: 
  - `get_gemini_response()`: Interfaces with the Google AI API.
  - `input_pdf_text()`: Extracts text from uploaded PDF resumes.
- **Prompt Template**: Defines the AI prompt for resume analysis.
- **Streamlit UI**: Sets up the user interface components.
- **Main Logic**: Handles file upload, job description input, and triggers the AI analysis.

## AI Integration

The application uses Google's Generative AI, specifically the Gemini-pro model. This integration allows for:

1. Natural language understanding of job descriptions.
2. Intelligent comparison between resume content and job requirements.
3. Generation of insightful feedback and suggestions.

The AI model is prompted to act as an experienced ATS with deep understanding of tech fields, ensuring relevant and accurate analysis.

## Future Improvements

Potential enhancements for the project:

1. Support for multiple resume formats (e.g., DOCX, TXT).
2. Integration with job posting APIs for automatic job description fetching.
3. More detailed resume improvement suggestions.
4. User accounts for saving and tracking multiple job applications.
5. Visualization of resume-job description matching metrics.

## Contributing

Contributions to Smart ATS are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

For any questions or support, please open an issue in the GitHub repository.
