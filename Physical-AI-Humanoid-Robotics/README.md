# 🤖 Physical AI & Humanoid Robotics

<div align="center">

![Physical AI Banner](https://img.shields.io/badge/Physical%20AI-Robotics-orange?style=for-the-badge&logo=robot&logoColor=white)
![Made with Love](https://img.shields.io/badge/Made%20with-❤️-red?style=for-the-badge)
![Hackathon](https://img.shields.io/badge/Panaversity-Hackathon%2004-blue?style=for-the-badge)

**Master the Future of Embodied Intelligence**

[🚀 Live Demo](https://syed-mujtaba-stack.github.io/Physical-AI-Humanoid-Robotics/) · [📚 Documentation](#features) · [🤝 Contributing](#contributing) · [⭐ Star on GitHub](https://github.com/syed-mujtaba-stack/Physical-AI-Humanoid-Robotics)

</div>

---

## ✨ Overview

An **AI-powered interactive textbook** that transforms robotics education through cutting-edge technology. Built for the Panaversity Hackathon 04, this platform combines comprehensive curriculum with intelligent features to create an unparalleled learning experience.

### 🎯 What Makes This Special?

- 🧠 **RAG-Powered Chatbot** - Ask questions, get context-aware answers
- 🎨 **Adaptive Content** - Personalize for beginner, intermediate, or expert levels
- 🌐 **Multilingual Support** - Dynamic Urdu translation powered by AI
- 📖 **11 Comprehensive Chapters** - From basics to advanced capstone projects
- 💬 **Smart Text Selection** - Highlight and ask questions about specific content
- 🎓 **Industry-Relevant** - Covers ROS 2, Gazebo, Unity, Isaac Sim, and more

---

## 🚀 Features

### 📚 **Interactive Textbook**
- **11 Deep-Dive Chapters** covering Physical AI fundamentals to advanced topics
- Beautiful, responsive Docusaurus interface
- Dark mode optimized for extended reading
- Mobile-friendly design

### 🤖 **AI-Powered Chat Assistant**
- Context-aware responses using **Gemini Flash 1.5**
- Vector search with **Qdrant** for semantic understanding
- Real-time chat with conversation history
- Selection-based queries - highlight text and ask questions

### 🎯 **Personalization Engine**
Three difficulty levels powered by LLMs:
- **Beginner**: Simplified explanations with analogies
- **Intermediate**: Standard technical content
- **Expert**: Advanced, concise material

### 🌐 **Translation Features**
- Dynamic **Urdu translation** maintaining markdown formatting
- Powered by state-of-the-art language models
- Preserves code blocks and technical terms

### 🔐 **User Authentication**
- Secure signup/signin system
- PostgreSQL user storage
- Ready for personalized learning paths

---

## 📖 Curriculum

### Module 1: Foundations
1. 🌍 **Humanoid Landscape** - Overview of embodied intelligence
2. 🦾 **ROS 2 Fundamentals** - Nodes, topics, services, actions
3. 🔧 **URDF Modeling** - Robot description format
4. 🎮 **Gazebo Simulation** - Physics simulation environments
5. 🎨 **Unity Visualization** - High-fidelity rendering
6. 🚀 **NVIDIA Isaac Sim** - Photorealistic simulation

### Module 2: Advanced Control & Learning
7. 👁️ **Visual SLAM** - Localization and mapping
8. 🧠 **Vision-Language-Action (VLA)** - Multimodal transformers (RT-1, RT-2)
9. 🎛️ **Control Systems** - Kinematics, locomotion, gait generation

### Module 3: Integration
10. 💬 **Conversational Robotics** - GPT integration, voice I/O
11. 🎓 **Capstone Project** - Build an autonomous humanoid robot

---

## 🏗️ Architecture

```mermaid
graph TB
    A[👤 User] --> B[⚛️ Docusaurus Frontend]
    B --> C[💬 Chat Widget]
    B --> D[🎯 Personalization]
    B --> E[🌐 Translation]
    
    C --> F[🚀 FastAPI Backend]
    D --> F
    E --> F
    
    F --> G[🔮 Qdrant Vector DB]
    F --> H[🐘 PostgreSQL]
    F --> I[🤖 OpenRouter API]
    
    I --> J[✨ Gemini Flash 1.5]
    I --> K[📊 OpenAI Embeddings]
    
    style A fill:#f97316
    style B fill:#3b82f6
    style F fill:#dc2626
    style J fill:#22d3ee
```

### 🛠️ Tech Stack

#### Frontend
- **Framework**: Docusaurus 3.9.2 (React 19)
- **Language**: TypeScript
- **Styling**: Custom CSS with modern gradients
- **Components**: Custom React components

#### Backend
- **Framework**: FastAPI (Python)
- **AI**: OpenRouter (Gemini Flash 1.5, OpenAI Embeddings)
- **Vector DB**: Qdrant Cloud
- **Database**: PostgreSQL
- **Auth**: Custom authentication system

#### DevOps
- **Containerization**: Docker + Docker Compose
- **Deployment**: Vercel (Backend) + GitHub Pages (Frontend)
- **Version Control**: Git

---

## 🚀 Quick Start

### Prerequisites

```bash
Node.js >= 20.0
Python >= 3.10
Docker (optional)
```

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/syed-mujtaba-stack/Physical-AI-Humanoid-Robotics.git
cd Physical-AI-Humanoid-Robotics
```

### 2️⃣ Frontend Setup

```bash
cd textbook-frontend
npm install
npm start
```

The app will open at `http://localhost:3000`

### 3️⃣ Backend Setup

```bash
cd rag-backend
pip install -r requirements.txt

# Create .env file
cp .env.example .env
# Add your API keys to .env

# Run ingestion (first time only)
python ingest.py

# Start server
uvicorn main:app --reload
```

Backend runs at `http://localhost:8000`

### 🐳 Docker Setup (Alternative)

```bash
docker-compose up
```

---

## 🔧 Configuration

### Frontend Environment (.env)

```env
# Optional: Override backend URL for local development
REACT_APP_API_URL=http://localhost:8000
```

### Backend Environment (.env)

```env
OPENROUTER_API_KEY=your_openrouter_key
OPENROUTER_MODEL=google/gemini-flash-1.5
OPENROUTER_EMBEDDING_MODEL=openai/text-embedding-3-small

QDRANT_URL=your_qdrant_cloud_url
QDRANT_API_KEY=your_qdrant_key

DATABASE_URL=postgresql://user:pass@host/db
```

---

## 📊 Project Structure

```
physical-ai-robotics/
├── 📁 textbook-frontend/          # Docusaurus app
│   ├── 📁 docs/                   # 11 chapters + intro
│   ├── 📁 src/
│   │   ├── 📁 components/         # React components
│   │   │   ├── ChatWidget.tsx
│   │   │   ├── ChatBot/
│   │   │   ├── PersonalizeButton.tsx
│   │   │   └── TranslateButton.tsx
│   │   ├── 📁 config/             # API configuration
│   │   └── 📁 css/                # Custom styles
│   └── 📄 package.json
│
├── 📁 rag-backend/                # FastAPI server
│   ├── 📄 main.py                 # API routes
│   ├── 📄 rag.py                  # RAG engine
│   ├── 📄 ingest.py               # Document indexing
│   ├── 📄 auth.py                 # Authentication
│   ├── 📄 db.py                   # Database connections
│   └── 📄 requirements.txt
│
├── 📁 spec/                       # Project specifications
├── 📄 docker-compose.yml          # Container orchestration
└── 📄 README.md                   # You are here! 📍
```

---

## 🎨 Features Showcase

### 💬 Smart Chat Interface

<div align="center">

![Chat Demo](https://img.shields.io/badge/Feature-Smart%20Chat-orange?style=flat-square&logo=wechat)

</div>

- **Floating Widget**: Always accessible, non-intrusive
- **Context-Aware**: Understands textbook content
- **Selection Queries**: Highlight text → Ask questions
- **Dark Theme**: Modern glassmorphism design

### 🎯 Content Personalization

<div align="center">

![Personalization](https://img.shields.io/badge/Feature-AI%20Personalization-blue?style=flat-square&logo=target)

</div>

- **One-Click Adaptation**: Transform content difficulty
- **Three Levels**: Beginner, Intermediate, Expert
- **LLM-Powered**: Intelligent rewriting
- **Preserves Formatting**: Code blocks, images intact

### 🌐 Multilingual Translation

<div align="center">

![Translation](https://img.shields.io/badge/Feature-Urdu%20Translation-green?style=flat-square&logo=google-translate)

</div>

- **Dynamic Translation**: Translate any chapter to Urdu
- **AI-Powered**: Maintains technical accuracy
- **RTL Support**: Proper right-to-left rendering

---

## 🎓 Educational Impact

### Learning Outcomes

Students will master:
- ✅ **Physical AI Concepts** - Embodied intelligence fundamentals
- ✅ **ROS 2 Ecosystem** - Industry-standard robotics framework
- ✅ **Simulation Platforms** - Gazebo, Unity, Isaac Sim
- ✅ **Advanced Topics** - SLAM, VLA models, conversational AI
- ✅ **Practical Skills** - Capstone project implementation

### Pedagogical Features

- 📚 Structured curriculum with clear progression
- 💡 Theory + Practice combination
- 🤖 AI-assisted learning
- 📱 Learn anywhere, anytime
- 🌍 Accessible in multiple languages

---

## 🏆 Hackathon Highlights

### Core Requirements ✅
- [x] Interactive textbook (11+ chapters)
- [x] RAG chatbot integration
- [x] Personalization features
- [x] Multilingual support (Urdu)
- [x] Modern, responsive UI
- [x] Backend API with vector search
- [x] Docker deployment ready

### Bonus Features ⭐
- [x] Authentication system
- [x] Text selection queries
- [x] Chunk-based RAG (500-word chunks, 100-word overlap)
- [x] Custom chat widget design
- [x] Production deployment (Vercel + GitHub Pages)
- [x] Glassmorphism UI with smooth animations

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 Fork the repository
2. 🌿 Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. 💾 Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. 📤 Push to the branch (`git push origin feature/AmazingFeature`)
5. 🎉 Open a Pull Request

### Development Guidelines
- Follow existing code style
- Add tests for new features
- Update documentation
- Use meaningful commit messages

---

## 📝 API Documentation

### Endpoints

#### Chat & RAG

```http
POST /rag/ask
Content-Type: application/json

{
  "query": "Explain ROS 2 nodes",
  "history": []
}
```

```http
POST /rag/ask-selection
Content-Type: application/json

{
  "query": "Explain this",
  "selected_text": "URDF is a XML format..."
}
```

#### Personalization

```http
POST /rag/personalize
Content-Type: application/json

{
  "text": "Markdown content...",
  "level": "beginner"
}
```

#### Translation

```http
POST /rag/translate
Content-Type: application/json

{
  "text": "Content to translate...",
  "target_language": "Urdu"
}
```

#### Authentication

```http
POST /auth/signup
POST /auth/signin
```

---

## 🐛 Troubleshooting

### Frontend Issues

**Port 3000 already in use:**
```bash
PORT=3001 npm start
```

**Build errors:**
```bash
npm run clear
npm install
npm start
```

### Backend Issues

**Qdrant connection failed:**
- Verify `QDRANT_URL` and `QDRANT_API_KEY` in `.env`
- Check Qdrant Cloud dashboard

**Vector search returning empty:**
```bash
python ingest.py  # Re-run ingestion
```

**CORS errors:**
- Backend CORS is set to allow all origins
- Check browser console for specific errors

---

## 📄 License

This project is created for **Panaversity Hackathon 04**.

---

## 🙏 Acknowledgments

- **Panaversity** - For organizing the hackathon
- **OpenRouter** - For AI model access
- **Qdrant** - Vector database platform
- **Docusaurus** - Amazing documentation framework
- **FastAPI** - Modern Python web framework

---

## 📞 Contact & Support

<div align="center">

**Built with ❤️ for Panaversity Hackathon 04**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/syed-mujtaba-stack/Physical-AI-Humanoid-Robotics)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](#)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](#)

**Questions or feedback?** Open an issue on GitHub!

</div>

---

<div align="center">

### ⭐ Star this repo if you found it helpful!

**Made with 🔥 by Mujtaba** | **Powered by Physical AI**

[⬆ Back to Top](#-physical-ai--humanoid-robotics)

</div>
