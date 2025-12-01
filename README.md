# Mergington High School Activities

A simple web application that allows students to view and sign up for extracurricular activities at Mergington High School.

## Overview

This project provides a user-friendly interface for students and teachers to manage extracurricular activities. Students can browse available activities and sign up with their email address, while the system tracks participation and capacity limits.

## Features

- 📋 **View Activities** - Browse all available extracurricular activities with details
- ✍️ **Sign Up** - Register for activities using student email
- 👥 **Track Participation** - Monitor current participant counts and capacity limits
- 🔄 **Real-time Updates** - See activity availability in real-time
- 📊 **Interactive API** - Access comprehensive API documentation

## Technology Stack

- **Backend:** Python with FastAPI
- **Frontend:** HTML, CSS, JavaScript
- **Server:** Uvicorn (ASGI)
- **Database:** In-memory storage (data resets on server restart)
- **Security:** Argon2 password hashing

## Quick Start

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Rumit0270/skills-expand-your-team-with-copilot.git
   cd skills-expand-your-team-with-copilot
   ```

2. Install dependencies:
   ```bash
   pip install -r src/requirements.txt
   ```

3. Run the application:
   ```bash
   python -m uvicorn src.app:app --host 0.0.0.0 --port 8000
   ```

4. Open your browser and navigate to:
   - **Web Interface:** http://localhost:8000
   - **API Documentation:** http://localhost:8000/docs
   - **Alternative API Docs:** http://localhost:8000/redoc

## Usage

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with details and participant counts |
| POST | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up for an activity |

### Example API Request

```bash
# View all activities
curl http://localhost:8000/activities

# Sign up for an activity
curl -X POST "http://localhost:8000/activities/Chess%20Club/signup?email=student@mergington.edu"
```

> [!IMPORTANT]
> All data is stored in memory and will be reset when the server restarts.

## Development

For detailed development setup and debugging instructions, see the [Development Guide](docs/how-to-develop.md).

### Development Environment

This project is designed for development in GitHub Codespaces, which provides a pre-configured environment with all necessary tools.

### Quick Development Setup

1. Open the repository in a Codespace
2. Install dependencies: `pip install -r src/requirements.txt`
3. Use VS Code's Run and Debug view (Ctrl+Shift+D)
4. Select "Launch Mergington WebApp" and press F5

The application includes FastAPI's auto-reload feature, which automatically restarts the server when you make code changes.

## Project Structure

```
skills-expand-your-team-with-copilot/
├── docs/                   # Documentation files
│   └── how-to-develop.md  # Detailed development guide
├── src/                    # Source code
│   ├── app.py             # Main FastAPI application
│   ├── backend/           # Backend logic
│   │   ├── database.py    # In-memory database
│   │   └── routers/       # API route handlers
│   ├── static/            # Frontend files
│   │   ├── index.html     # Main web interface
│   │   ├── styles.css     # Styling
│   │   └── app.js         # Frontend logic
│   └── requirements.txt   # Python dependencies
├── .devcontainer/         # Codespace configuration
└── README.md              # This file
```

## Contributing

Contributions are welcome! This project is designed to be simple and easy to maintain for non-technical staff.

### Guidelines

- Keep code simple and well-documented
- Use only HTML, CSS, JavaScript, and Python
- Maintain the existing project structure
- Test changes thoroughly before submitting

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

This project was created as part of the "Expand your team with GitHub Copilot" GitHub Skills exercise.

---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

