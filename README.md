# SportyBet Clone with ML Enhancements

A comprehensive sports betting platform clone inspired by SportyBet, featuring AI/ML predictions, real-time sports data, and modern web technologies.

## 🚀 Features

- **Real-time Sports Data**: Live match updates and statistics
- **AI Predictions**: Machine learning models predicting match outcomes (Win/Draw/Loss probabilities)
- **Odds Comparison**: Multi-bookmaker odds analysis
- **Modern UI**: Responsive design with TailwindCSS
- **Containerized Deployment**: Docker-based architecture for easy deployment

## 🏗️ Architecture

### Frontend (Port 3000)
- **Framework**: Next.js with TailwindCSS
- **Features**: Match listings, detailed match pages, prediction displays, odds charts

### Backend (Port 8000)
- **Framework**: FastAPI (Python)
- **Features**: REST API, ML predictions, sports data integration, scheduled updates

### Database
- **DBMS**: PostgreSQL
- **ORM**: SQLAlchemy
- **Tables**: matches, teams, predictions, odds, historical_results

### Machine Learning
- **Stack**: Python, scikit-learn, XGBoost, Pandas
- **Models**: Logistic Regression, Random Forest, Gradient Boosting
- **Predictions**: Win/Draw/Loss probabilities based on historical data

## 📡 Data Sources

- **Football-Data.org**: Free fixtures and results
- **TheSportsDB**: Team stats and player information
- **API-Football**: Comprehensive match data (limited free tier)

## 🐳 Quick Start

```bash
# Clone the repository
git clone <repository>
cd sportybet

# Quick deployment (recommended)
./deploy.sh

# Or manual deployment
cp .env.example .env  # Edit with your API keys
docker-compose up -d
make seed-db
make train-ml

# Access the application
Frontend: http://localhost:3000
Backend API: http://localhost:8000
API Docs: http://localhost:8000/docs
```

## 🧪 Testing

```bash
# Run all tests
make test

# Backend tests
cd backend && python -m pytest

# Frontend tests
cd frontend && npm test

# Health check
make health
```

## 📁 Project Structure

```
/sportybet
├── frontend/          # Next.js application
├── backend/           # FastAPI application
├── ml/               # ML models and training scripts
├── database/         # SQL migrations and seeders
├── nginx/            # Nginx configuration
├── docker-compose.yml
└── .env.example
```

## 🧠 ML Prediction Engine

The system uses machine learning to predict match outcomes based on:
- Team historical performance
- Head-to-head records
- Recent form and statistics
- Player availability and team strength

## 🔧 Development

```bash
# Development mode with hot reload
make dev

# Individual service development
cd frontend && npm run dev
cd backend && uvicorn app.main:app --reload
cd ml && python train_models.py
```

See individual service README files for detailed instructions:
- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)
- [ML README](./ml/README.md)
- [Deployment Guide](./DEPLOYMENT.md)

## 📊 Project Status

✅ **Completed Features:**
- Complete project architecture and Docker setup
- FastAPI backend with REST endpoints
- PostgreSQL database with comprehensive schema
- Next.js frontend with modern UI components
- ML prediction engine with multiple algorithms
- Sports data integration services
- Comprehensive testing setup
- Deployment automation scripts

🚀 **Ready for Development:**
- All core infrastructure is in place
- Sample data and dummy predictions available
- Hot reload development environment
- Comprehensive documentation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Run the test suite
6. Submit a pull request

## 📄 License

This project is for educational purposes only. Not intended for commercial use.
# sportybet
