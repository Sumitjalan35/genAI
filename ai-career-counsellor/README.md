# AI Career Counsellor

A comprehensive AI-powered career guidance platform that provides personalized career advice for both students and working professionals using Google's Gemini AI.

## 🌟 Features

### For Students
- **Academic Profile Analysis**: Comprehensive assessment based on academic performance, stream, and interests
- **Career Path Recommendations**: AI-powered suggestions for suitable career paths
- **Skills Development Plan**: Personalized roadmap for technical and soft skills development
- **Education & Certification Guidance**: Recommendations for courses and certifications within budget
- **Competitive Exam Strategy**: Preparation guidance for relevant competitive exams
- **Action Plan**: Short-term, medium-term, and long-term career milestones

### For Working Professionals
- **Career Advancement Strategy**: Analysis of current position and growth opportunities
- **Skill Development Roadmap**: Critical skills to develop based on career goals
- **Transition Planning**: Steps for career transitions or industry changes
- **Professional Development**: Learning opportunities and mentorship recommendations
- **Compensation & Negotiation**: Salary benchmarking and negotiation strategies
- **Industry Insights**: Market trends and future skill requirements

### General Features
- **Modern UI/UX**: Beautiful, responsive interface built with React and Tailwind CSS
- **Real-time AI Analysis**: Instant career advice using Google Gemini AI
- **Interactive Dashboard**: Comprehensive overview of career recommendations
- **Career Explorer**: Detailed exploration of different career paths
- **AI Toolkit**: Various AI-powered career tools and resources

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- Node.js 16 or higher
- npm or yarn

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Sumitjalan35/genAI.git
   cd genAI/ai-career-counsellor
   ```

2. **Run the startup script**
   ```bash
   ./start.sh
   ```

   This script will:
   - Create a Python virtual environment
   - Install all Python dependencies
   - Install all Node.js dependencies
   - Start both backend and frontend servers

3. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:8000
   - API Documentation: http://localhost:8000/docs

### Manual Setup (Alternative)

If you prefer to set up manually:

#### Backend Setup
```bash
cd backend
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

#### Frontend Setup
```bash
npm install
npm run dev
```

## 🏗️ Architecture

### Backend (Python/FastAPI)
- **Framework**: FastAPI for high-performance API development
- **AI Integration**: Google Gemini AI for career advice generation
- **Data Models**: Pydantic models for request/response validation
- **CORS**: Configured for frontend communication

### Frontend (React/Vite)
- **Framework**: React 19 with Vite for fast development
- **Styling**: Tailwind CSS for modern, responsive design
- **Animations**: Framer Motion for smooth animations
- **Routing**: React Router for navigation
- **Icons**: Lucide React for consistent iconography

### API Endpoints

#### Student Career Advice
- `POST /api/student/career-advice` - Get personalized career advice for students
- `GET /api/student/career-advice/sample` - Get sample request format

#### Professional Career Advice
- `POST /api/professional/career-advice` - Get personalized career advice for professionals
- `GET /api/professional/career-advice/sample` - Get sample request format

#### General
- `GET /` - API health check
- `GET /health` - Detailed health status
- `GET /docs` - Interactive API documentation

## 📁 Project Structure

```
ai-career-counsellor/
├── backend/
│   ├── main.py                 # Main FastAPI application
│   ├── requirements.txt        # Python dependencies
│   ├── student.py             # Student-specific API (legacy)
│   └── professional.py        # Professional-specific API (legacy)
├── src/
│   ├── pages/
│   │   ├── LandingPage.jsx    # Landing page
│   │   ├── ProfileSetup.jsx   # Multi-step profile setup
│   │   ├── SummaryPage.jsx    # Profile summary with AI advice
│   │   ├── Dashboard.jsx      # Main dashboard
│   │   ├── CareerExplorer.jsx # Career exploration
│   │   └── AIToolkit.jsx      # AI tools
│   ├── services/
│   │   └── api.js             # API service layer
│   ├── App.jsx                # Main app component
│   └── main.jsx               # App entry point
├── public/                    # Static assets
├── package.json               # Node.js dependencies
├── start.sh                   # Startup script
└── README.md                  # This file
```

## 🔧 Configuration

### Environment Variables
The application uses a hardcoded Google Gemini API key. For production, you should:

1. Create a `.env` file in the backend directory
2. Add your API key:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```
3. Update `main.py` to read from environment variables

### API Key Setup
1. Get a Google Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Replace the hardcoded key in `backend/main.py`

## 🎯 Usage

### For Students
1. Visit the application
2. Click "Get Started"
3. Select "Student" as your user type
4. Complete the multi-step profile setup:
   - Academic information
   - Interests and skills
   - Career preferences
   - Additional information
5. View your personalized AI-generated career advice
6. Explore the dashboard for detailed recommendations

### For Professionals
1. Visit the application
2. Click "Get Started"
3. Select "Working Professional" as your user type
4. Complete the multi-step profile setup:
   - Current professional status
   - Career goals
   - Skills assessment
   - Work preferences
   - Challenges and development goals
5. View your personalized AI-generated career advice
6. Explore the dashboard for detailed recommendations

## 🛠️ Development

### Adding New Features
1. Backend: Add new endpoints in `main.py`
2. Frontend: Create new components in `src/pages/`
3. API Integration: Update `src/services/api.js`

### Testing
- Backend: Use the interactive API docs at http://localhost:8000/docs
- Frontend: Use browser developer tools for debugging

### Deployment
- Backend: Deploy to services like Heroku, Railway, or AWS
- Frontend: Deploy to Vercel, Netlify, or similar platforms
- Update API_BASE_URL in `src/services/api.js` for production

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

If you encounter any issues:
1. Check the console for error messages
2. Ensure all dependencies are installed
3. Verify the API key is correct
4. Check that both servers are running

## 🔮 Future Enhancements

- [ ] User authentication and profiles
- [ ] Save and manage multiple career plans
- [ ] Integration with job boards
- [ ] Resume builder with AI assistance
- [ ] Interview preparation tools
- [ ] Networking recommendations
- [ ] Progress tracking and analytics
- [ ] Mobile app development

---

Built with ❤️ using React, FastAPI, and Google Gemini AI