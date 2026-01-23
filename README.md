# TruthGuard - Fake News Detection and Verification Tool

TruthGuard is a comprehensive web application designed to combat misinformation through advanced artificial intelligence and machine learning technologies. In today's digital age, where information spreads rapidly across various platforms, our tool provides users with reliable, real-time analysis to distinguish between credible news and potentially misleading content.

## Key Features

- **Real-time Analysis**: Lightning-fast fake news detection with response times under 100 milliseconds
- **AI-Powered Assistant**: Integrated Google Gemini AI for intelligent fact-checking guidance and contextual analysis
- **Multi-format Content Support**: Comprehensive analysis capabilities for text content, web URLs, and document uploads
- **Personal Dashboard**: Detailed analytics and historical tracking of your analysis activities
- **Administrative Control Panel**: Complete system monitoring and user management capabilities
- **Advanced Credibility Scoring**: Sophisticated algorithms that evaluate content reliability using multiple factors
- **Sentiment Analysis**: Emotional tone detection to identify potentially biased or sensationalized content
- **Source Verification**: Automated URL content extraction and validation for comprehensive fact-checking

## Project Architecture

```
Fake-News-Detection-and-Verification-Tool/
├── Milestone 1/                    # Basic authentication and core functionality
├── Milestone 2/                    # Enhanced UI and analysis features
├── Milestone 3/                    # AI integration and admin panel
├── LICENSE                         # MIT License
└── README.md                      # This file
```

## Technology Stack

- **Backend**: Python Flask
- **Database**: SQLite with SQLAlchemy ORM
- **AI Integration**: Google Gemini API
- **NLP**: NLTK for text processing and sentiment analysis
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap
- **Authentication**: Flask-Login with secure password hashing
- **Web Scraping**: BeautifulSoup4 for URL content extraction

## Installation Guide

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Fake-News-Detection-and-Verification-Tool.git
   cd Fake-News-Detection-and-Verification-Tool
   ```

2. **Navigate to the latest milestone**
   ```bash
   cd "Milestone 3/Infosys_FakeNewsDetectionAndVerification"
   ```

3. **Install dependencies**
   ```bash
   pip install flask flask-sqlalchemy flask-login werkzeug python-dotenv
   pip install nltk pandas numpy requests beautifulsoup4
   pip install google-generativeai
   ```

4. **Set up environment variables**
   Create a `.env` file in the project root:
   ```env
   SECRET_KEY=your-secret-key-here
   GEMINI_API_KEY=your-gemini-api-key-here
   GEMINI_MODEL=gemini-2.5-flash
   ```

5. **Initialize NLTK data**
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   nltk.download('wordnet')
   nltk.download('vader_lexicon')
   ```

6. **Run the application**
   ```bash
   python app.py
   ```

7. **Access the application**
   Open your browser and navigate to `http://localhost:5000`

## Default Administrator Credentials

- **Email**: admin@truthguard.com
- **Password**: Admin123!

*Important: Please change these default credentials immediately after your first login to ensure system security.*

## Usage Instructions

### For Users

1. **Register/Login**: Create an account or login with existing credentials
2. **Analyze Content**: 
   - Paste text directly into the analyzer
   - Enter a URL to analyze web content
   - Upload documents for analysis
3. **View Results**: Get instant credibility scores and detailed analysis
4. **Chat Assistant**: Use the AI-powered chat for fact-checking guidance
5. **History**: Review your analysis history and track patterns

### For Administrators

1. **Admin Dashboard**: Monitor system statistics and user activity
2. **User Management**: Activate/deactivate users and assign admin roles
3. **Content Moderation**: Review and manage analysis results
4. **System Health**: Monitor API status and performance metrics

## System Architecture and Functionality

### Analysis Engine

1. **Text Preprocessing**: Content cleaning and normalization
2. **Feature Extraction**: 
   - Sensationalism indicators
   - Credibility markers
   - Sentiment analysis
   - Source verification
3. **Classification**: Multi-factor scoring algorithm
4. **Results**: Confidence scores and actionable recommendations

### AI Integration

- **Gemini AI**: Advanced fact-checking and misinformation detection
- **Fallback System**: Rule-based responses when AI is unavailable
- **Caching**: Optimized response times with intelligent caching

## API Documentation

### Analysis
- `POST /analyze` - Analyze text or URL content
- `GET /analysis/<id>` - Get specific analysis details
- `GET /history` - User analysis history

### Chat
- `POST /chat` - Chat with AI assistant
- `POST /api/chat/simple` - Simple chat without authentication

### Admin
- `GET /admin` - Admin dashboard
- `POST /admin/user/<id>/toggle` - Toggle user status
- `GET /api/health` - System health check

## Configuration Settings

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `SECRET_KEY` | Flask secret key | `dev-secret-key-change-in-production` |
| `GEMINI_API_KEY` | Google Gemini API key | Required for AI features |
| `GEMINI_MODEL` | Gemini model version | `gemini-2.5-flash` |

### Database Configuration

The application uses SQLite by default. The database file is created automatically at:
```
instance/truthguard.db
```

## Deployment Instructions

### Production Deployment

1. **Set production environment variables**
2. **Use a production WSGI server** (e.g., Gunicorn)
3. **Configure reverse proxy** (e.g., Nginx)
4. **Set up SSL certificates**
5. **Configure database backups**

### Docker Deployment (Optional)

```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "app.py"]
```

## Testing and Quality Assurance

Run the test suite:
```bash
python -m pytest tests/
```

Test Gemini AI integration:
```bash
curl http://localhost:5000/test-gemini
```

## Contributing to the Project

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License Information

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Security Features

- Secure password hashing with PBKDF2
- CSRF protection
- Input validation and sanitization
- Rate limiting on API endpoints
- Secure session management

## Support and Documentation

For support and questions:
- Create an issue on GitHub
- Contact: [Your Email]
- Documentation: [Project Wiki]

## Acknowledgments

- Google Gemini AI for advanced language processing
- NLTK team for natural language processing tools
- Flask community for the excellent web framework
- Contributors and testers

## Future Development Roadmap

- [ ] Mobile application
- [ ] Advanced ML models
- [ ] Multi-language support
- [ ] Real-time news monitoring
- [ ] Browser extension
- [ ] API rate limiting
- [ ] Advanced analytics dashboard

---

**Developed by Peddi Manikanta**

*Dedicated to combating misinformation and promoting media literacy through innovative technology solutions.*