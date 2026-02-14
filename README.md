# Drug Discovery AI Assistant 2.0
**Problem Statement**

The process of drug discovery is time-consuming, expensive, and often inefficient, with a high rate of failure in clinical trials. Traditional methods rely heavily on trial and error, requiring years of research and significant financial investment. Additionally, the complexity of biological systems and the vast chemical space make it challenging to identify promising drug candidates efficiently.
Generative AI, with its ability to analyze large datasets, predict molecular interactions, and generate novel compounds, has the potential to revolutionize this process. However, there is a lack of accessible, user-friendly tools that leverage generative AI to assist researchers in accelerating drug discovery while reducing costs and improving success rates.
This application addresses these challenges by providing:
AI-Augmented Discovery: Integration with Google Gemini and specialized chemistry APIs to predict compound properties and generate novel structures
Visualization Tools: Interactive molecular viewers and editors to intuitively explore chemical space
Collaboration Features: Real-time sharing of research findings among team members
Knowledge Integration: Aggregation of relevant pharmaceutical news and research
A comprehensive full-stack application for AI-powered drug discovery and pharmaceutical research, featuring molecular visualization, predictive analytics, and real-time collaboration tools.

![image](https://github.com/user-attachments/assets/a770845b-aefb-4295-9480-196e4e219bbe)
<img width="947" height="760" alt="image" src="https://github.com/user-attachments/assets/b634fff6-f6c8-47ce-902a-114758486a1a" />
<img width="391" height="1017" alt="image" src="https://github.com/user-attachments/assets/c8cb4750-4609-4707-8ecd-0598a8889c52" />
<img width="767" height="862" alt="image" src="https://github.com/user-attachments/assets/b1117025-bc34-4e1d-9fd7-be2fa3aded52" />
<img width="1280" height="655" alt="image" src="https://github.com/user-attachments/assets/a0f80941-d9f6-4944-8f51-9c9f85062cd4" />
<img width="657" height="945" alt="image" src="https://github.com/user-attachments/assets/595dbc3c-20f8-4a88-9962-785a3e2b29ea" />


Use below login cerdentials [Since we have use Twilio Demo so otp will come to only registered phone number so use below credentials ]
- Email - test@gmail.com
- password - 1

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Deployment](#deployment)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [License](#license)

## Features

### Backend
- Secure user authentication with JWT and bcrypt
- High-performance Redis caching layer
- MongoDB database with Mongoose ODM
- Multi-API integration:
  - Google Gemini for AI-driven drug analysis
  - MOLMIM for advanced molecular modeling
  - QWQ API for chemical property predictions
- Pharmaceutical news aggregation
- File upload handling with Multer
- Real-time collaboration with Socket.io
- PDF report generation

### Frontend
- Interactive molecular visualization (RDKit/NGL)
- Chemical structure editor (Ketcher)
- 3D molecular rendering (Three.js/Spline)
- Responsive Tailwind CSS UI
- State management with Zustand
- Animated transitions with Framer Motion
- Real-time updates via Socket.io
- AI-powered predictive analytics dashboard

## Technologies Used

Gemini Integration

Gemini serves as the core LLM powering intelligence across the Drugs Assistant application. We have tightly integrated Gemini 2.5 Flash with an agentic MCP (Model Control Protocol) server, enabling automated task orchestration and reducing the need for manual interventions by researchers.

**Key Enhancements**
Agentic Workflow with MCP Server
A custom-built MCP server manages multi-step reasoning pipelines and delegates subtasks to Gemini.
Enables autonomous decision-making for repetitive research processes such as molecule property lookups, drug cost estimations, and workflow validations.
Retrieval-Augmented Generation (RAG)
Gemini 2.5 Flash acts as the primary reasoning engine, supported by RAG pipelines.
Seamless integration with Google Embeddings API improves semantic search, contextual memory, and retrieval of relevant drug data and biomedical research.
Applied Use Cases
Drug Cost Analysis: Automated estimation and comparison of pharmaceutical costs.
Research Paper Citations: Smart citation generation for compounds and related studies, ensuring traceability and credibility.
AI Naming Suggestions: Intuitive name generation for molecules, compounds, and research projects.
Jarvis Assistant for Researchers: An AI-driven mentor that guides newbie researchers, detects workflow gaps, and ensures smooth progression through the discovery pipeline.

**Benefits**
By integrating Gemini in this multi-layered approach, we deliver:
Increased automation in the drug discovery workflow.
Reduced human intervention, freeing researchers from repetitive manual tasks.
Scalable intelligence that supports both early-stage research and advanced pharmaceutical analysis.
1. **AI-Augmented Discovery**: Integration with Google Gemini and specialized chemistry APIs to predict compound properties and generate novel structures
2. **Visualization Tools**: Interactive molecular viewers and editors to intuitively explore chemical space
3. **Collaboration Features**: Real-time sharing of research findings among team members
4. **Knowledge Integration**: Aggregation of relevant pharmaceutical news and research

### Backend Stack
- **Runtime**: Node.js (ES Modules)
- **Framework**: Express.js
- **Database**: MongoDB (Atlas)
- **Cache**: Redis (Upstash)
- **Authentication**: JWT + bcrypt
- **AI Services**: Google Generative AI, MOLMIM, QWQ
- **Real-time**: Socket.io
- **Utilities**: Axios, Multer, html2pdf

### Frontend Stack
- **Core**: React 18 + Vite
- **State**: Zustand
- **Styling**: Tailwind CSS + Animate
- **Cheminformatics**: RDKit, Ketcher, NGL
- **3D**: Three.js, Spline
- **UI**: Radix, Lucide, Heroicons
- **Charts**: To be implemented
- **Forms**: React Hook Form
- **Routing**: React Router

## Installation

### Prerequisites
- Node.js (v18+ recommended)
- MongoDB Atlas account
- Redis (Upstash recommended)
- Git

### Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/drugs-assistant.git
   cd drugs-assistant
  ```
PORT=5000
MONGODB_URI=mongodb+srv://<user>:<password>@cluster.mongodb.net/database
JWT_SECRET=complex_secret_here
GEMINI_API_KEY=your_google_ai_key
MOLMIM_API_KEY=your_molmim_key
QWQ_API_KEY=your_qwq_key
NEWS_API_KEY=your_newsapi_key
UPSTASH_REDIS_URL=redis://user:pass@host:port
ACCESS_TOKEN_KEY=access_secret
REFRESH_TOKEN_KEY=refresh_secret
```
##Running the Application
```
# Backend
npm run dev

# Frontend (in separate terminal)
cd frontend
npm run dev
```

