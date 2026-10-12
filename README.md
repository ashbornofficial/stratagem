# Stratagem

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.9+" />
  <img src="https://img.shields.io/badge/Flask-3.0-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask 3.0" />
  <img src="https://img.shields.io/badge/Google%20Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Gemini AI" />
</p>

<p align="center">
  <strong>Think Deeper. Question Assumptions. Connect Ideas.</strong>
</p>

Stratagem is a modern AI-powered study assistant designed to help users think critically, analyze arguments, and explore ideas in a deeper and more meaningful way.

Built with Python and Flask, Stratagem allows users to submit text and receive AI-generated analysis through multiple specialized modes.

Whether you're studying a chapter, reviewing an article, or preparing for a debate, Stratagem transforms passive reading into active intellectual engagement.

## Why Stratagem?

Traditional AI tools often focus on summarizing content. Stratagem goes further by helping users:

- Identify weaknesses in arguments.
- Challenge assumptions and uncover hidden logic.
- Generate meaningful discussion questions.
- Connect ideas across different disciplines.
- Develop deeper understanding through critical thinking.

### Who Is It For?

- Students
- Researchers
- Educators
- Critical thinkers
- Lifelong learners

## Core Features

### 1. Find the Flaw

Identifies weak arguments, logical fallacies, hidden assumptions, and unanswered questions in the submitted text.

### 2. Socratic Quiz

Generates conceptual, high-value questions designed to test understanding and encourage deeper reflection.

### 3. Connect Concepts

Connects the submitted topic with ideas from other disciplines to uncover surprising patterns and cross-domain insights.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Flask | Backend web framework |
| Google Gemini AI | AI-powered analysis |
| HTML | Page structure |
| CSS | Styling and layout |
| JavaScript | Frontend interactions |
| python-dotenv | Environment variable management |

## Project Structure

```text
stratagem/
├── main.py
├── requirements.txt
├── .replit
├── .env.example
├── .gitignore
├── README.md
├── static/
│   ├── script.js
│   └── style.css
└── templates/
    └── index.html
```

## Getting Started

Follow these steps to run Stratagem locally on your computer.

### Prerequisites

Before getting started, make sure you have:

- Python 3.9 or later
- A valid Google Gemini API key
- Git (optional, for cloning the repository)

### 1. Clone the Repository

```bash
git clone https://github.com/nisarg1212/stratagem.git
cd stratagem
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment

**Windows:**

```powershell
.venv\Scripts\activate
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables

Create a `.env` file in the project's root directory and add your Gemini API key:

```env
GEMINI_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your actual API key.

If you're using Replit, add the same variable to your project's Secrets:

```text
GEMINI_API_KEY
```

**Important:** Never publish your actual API key or commit your `.env` file to GitHub.

### 6. Run the Application

```bash
python main.py
```

Open your browser and visit:

```text
http://localhost:8080
```

The application should now be accessible locally, provided the server starts successfully on port `8080`.

## How It Works

Stratagem follows a straightforward analysis workflow:

1. The user enters text into the application.
2. The user selects an analysis mode.
3. The frontend sends the text and selected mode to the Flask backend.
4. The backend constructs a prompt for Google Gemini.
5. Gemini generates the requested analysis.
6. The frontend displays the generated response.

### Available Analysis Modes

| Mode | Description |
|---|---|
| `flaw` | Finds weaknesses, fallacies, and hidden assumptions. |
| `quiz` | Generates questions to test understanding. |
| `connect` | Explores connections between concepts and disciplines. |

## API Documentation

### Analyze Text

**Endpoint:** `POST /api/analyze`

**Content-Type:** `application/json`

#### Example Request

```json
{
  "text": "Paste your notes, article, essay, or chapter here.",
  "mode": "flaw"
}
```

#### Valid Modes

- `flaw`
- `quiz`
- `connect`

#### Example Response

```json
{
  "response": "Generated analysis text from Gemini."
}
```

The response shown above is an illustrative example of the expected response format.

## Configuration Notes

- The application uses the Google Gemini API for AI-generated analysis.
- The configured model is reported as `gemini-1.5-pro-latest`; verify that it remains available for your API account and update the model configuration if necessary.
- A valid API key must be configured for AI analysis requests to work.
- The application must be able to reach the configured Gemini API endpoint.

## Security

Follow these practices when running or deploying Stratagem:

- Keep API keys private.
- Store secrets in environment variables or a secure secret manager.
- Never commit `.env` files containing real credentials.
- Add appropriate input validation and error handling to API endpoints.
- Avoid exposing sensitive server configuration or API errors to users.
- Use HTTPS and appropriate request protections when deploying publicly.

## Future Improvements

Stratagem can be extended with additional features, including:

- Chat history and saved analysis sessions
- User authentication
- Export options for generated analyses
- Support for multiple AI models
- Custom analysis modes
- Study progress tracking
- Improved error handling and API usage controls

These are potential future enhancements, not claims about existing functionality.

## Contributing

Contributions, bug reports, and suggestions are welcome.

To contribute:

1. Fork this repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes and test them.
4. Commit your changes:

   ```bash
   git add .
   git commit -m "Add your change description"
   ```

5. Push your branch to your fork:

   ```bash
   git push origin feature/your-feature-name
   ```

6. Open a pull request against the original repository.

Please keep contributions focused, clearly documented, and consistent with the existing project structure.

## License

No license file is currently included in this repository.

Until a license is added, others should not assume they have permission to reuse, modify, or redistribute the project. The repository owner can choose an appropriate open-source license, such as MIT or Apache-2.0.

## Author

**Created by [nisarg1212](https://github.com/nisarg1212)**

## Repository

[View Stratagem on GitHub](https://github.com/nisarg1212/stratagem)

---

<p align="center">
  <strong>Stratagem — Think Critically. Learn Deeply.</strong>
</p>
