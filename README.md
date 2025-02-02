﻿# Document-Summary-Assistant-
Document Summary Assistant
Document Summary Assistant is an application that takes any document (PDF or image) and generates smart summaries using Optical Character Recognition (OCR) and AI-based summarization.

Features
1. Document Upload
Users can upload PDF and image files (scanned documents).
Supports drag-and-drop or file picker interface for easy document uploads.
2. Text Extraction
PDF Parsing: Extracts text from PDFs while maintaining formatting.
OCR (Optical Character Recognition): For image files (e.g., scanned documents), text is extracted using OCR technology (Tesseract.js).
3. Summary Generation
Automatically generates smart summaries of the document content.
Users can choose the summary length (short, medium, long).
The summary highlights key points and main ideas, ensuring the document's essential information is captured.
4. Improvement Suggestions
After generating a summary, users will receive suggestions to improve the document or additional information about the summary content.
5. UI/UX
Simple and intuitive interface for uploading documents and viewing summaries.
The design is mobile-responsive, providing a great user experience across various devices.
6. Hosting
The application is deployed on a reliable hosting service such as Netlify, Vercel, or Heroku, ensuring scalability and easy access.
Technical Requirements
Clean, production-quality code with basic error handling.
The application includes loading states for a smoother user experience.
Simple documentation that explains the approach used in the development.
Setup and Installation
Follow these steps to set up the Document Summary Assistant locally.

1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/document-summary-assistant.git
cd document-summary-assistant
2. Install Dependencies
For both frontend and backend, run the following command in the project root directory:

bash
Copy
Edit
npm install
3. Environment Variables
Create a .env file in the root directory of the project and add the following:

env
Copy
Edit
OPENAI_API_KEY=your-openai-api-key
MONGO_URI=your-mongodb-connection-string
4. Run the Application Locally
Start the server with the following command:

bash
Copy
Edit
npm start
The backend will run on http://localhost:5000.

5. Access the Application
Open your browser and visit http://localhost:5000 to start uploading documents and generating summaries.

How It Works
Document Upload:

The user selects a document (PDF or image) via the file picker or drag-and-drop interface.
The document is uploaded to the backend.
Text Extraction:

For PDF documents, the text is extracted using a library like pdf-parse.
For image files, OCR is performed using Tesseract.js to extract the text.
Summary Generation:

Once the text is extracted, it is sent to an AI-based summarization API (such as OpenAI) to generate a concise summary.
The user can select the summary length (short, medium, long) based on their preference.
Displaying Results:

The summary is shown to the user, along with improvement suggestions (if applicable).
Technologies Used
Backend:

Node.js with Express for the server.
Multer for file upload handling.
Tesseract.js for OCR text extraction.
OpenAI API (GPT-3) for summary generation.
Frontend:

HTML, CSS, and JavaScript (Vanilla) for the UI.
Fetch API for interacting with the backend.
FormData for sending the document to the server.
Database:

MongoDB for storing documents and summaries.
AI/ML Services
The application uses OpenAI's GPT-3 model to generate summaries based on the extracted text. Ensure that you provide your OpenAI API key in the .env file.

Contributing
Contributions are welcome! Please follow these steps to contribute:

Fork the repository.
Create a new branch.
Make your changes.
Submit a pull request.
License
This project is licensed under the MIT License.

Troubleshooting
If you experience issues with document uploads or OCR extraction, check the console logs for error messages.
Ensure that the OpenAI API key is correctly set in your environment variables (.env).
Ensure the uploads directory exists and has write permissions for storing the uploaded files.
