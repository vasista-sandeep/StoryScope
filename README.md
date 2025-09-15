StoryScope
A micro-SaaS application for analyzing and estimating user story complexity using NLP.

🚀 Features
Natural Language Processing for story analysis
Complexity scoring based on multiple factors
RESTful API endpoints
Real-time story processing


🏗️ Architecture

StoryScope/
├── apps/
│   ├── api/         # Express.js backend service
│   ├── nlp/         # FastAPI NLP service
│   └── web/         # Frontend application (coming soon)


🛠️ Technical Stack

NLP Service

Python 3.12
FastAPI
spaCy (en_core_web_sm)

API Service

Node.js
Express.js
📋 Prerequisites
Python 3.12
Node.js
spaCy English language model


⚙️ Installation
Clone the repository

git clone https://github.com/yourusername/StoryScope.git
cd StoryScope
Set up NLP Service

cd apps/nlp
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python -m spacy download en_core_web_sm


Set up API Service

cd ../api
npm install


🚀 Running the Services

Start NLP Service
cd apps/nlp
.venv\Scripts\activate
python main.py

Service runs at http://127.0.0.1:8001

Start API Service

cd apps/api
node server.js
Service runs at http://127.0.0.1:8000

📡 API Endpoints
NLP Service
GET /health - Service health check
POST /estimate - Analyze story complexity
API Service
GET /health - Service health check
POST /estimate - Proxy endpoint for NLP analysis


📝 API Usage Example

POST /estimate
{
    "summary": "Add user authentication",
    "description": "Implement OAuth2 based authentication system",
    "labels": ["security", "authentication"]
}

🧪 Testing
Run unit tests for each service:

# NLP Service tests
cd apps/nlp
pytest

# API Service tests
cd apps/api
npm test

📈 Complexity Analysis Factors
Text length and token count
Uncertainty indicators
Technical complexity keywords
Label count and relevance


🤝 Contributing
Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit changes (git commit -m 'Add AmazingFeature')
Push to branch (git push origin feature/AmazingFeature)
Open a Pull Request


📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

👥 Authors
Vasista Sandeep - Initial work


🙏 Acknowledgments
spaCy for NLP capabilities
FastAPI for the Python backend
Express.js community
