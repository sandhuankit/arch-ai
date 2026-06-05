# Arch-AI: AI-Powered Architectural Design Platform

Welcome to **Arch-AI** - A revolutionary web application that generates architectural designs from simple text prompts using AI.

## 🎯 Features

- 🏗️ **AI-Powered Design Generation** - Generate floor plans from natural language prompts
- 📐 **Interactive Floor Plans** - View and customize room layouts with real-time updates
- 🎨 **3D Visualization** - Interactive 3D models with rotate, zoom, and pan controls
- 📋 **Technical Specifications** - Plumbing, electrical, lighting, and structural details
- 💾 **Design Gallery** - Save, manage, and share your designs
- 📥 **Export Options** - Download as PNG, PDF, or specifications document
- 🎯 **Multiple Styles** - Modern, Traditional, Contemporary, Minimalist designs

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn
- MongoDB (local or Atlas cloud)
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/sandhuankit/arch-ai.git
cd arch-ai

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local

# Run development server
npm run dev
```

## 📁 Project Structure

```
arch-ai/
├── frontend/           # Next.js React application
├── backend/            # Express.js API server
├── docs/               # Documentation
├── docker-compose.yml  # Docker configuration
└── README.md          # This file
```

## 🛠️ Tech Stack

- **Frontend:** Next.js 14, React, TypeScript, Tailwind CSS
- **Backend:** Node.js, Express.js, TypeScript
- **Database:** MongoDB
- **AI/ML:** Hugging Face API, Stable Diffusion
- **3D Graphics:** Three.js
- **Deployment:** Vercel, Railway/Render

## 📖 Documentation

- [Setup Guide](docs/SETUP.md) - Detailed installation and configuration
- [API Documentation](docs/API.md) - Backend API endpoints
- [Deployment Guide](docs/DEPLOYMENT.md) - Deploy to production
- [Usage Guide](docs/USAGE.md) - How to use the application

## 🔗 API Endpoints

### Design Management
- `POST /api/designs/generate` - Generate new design
- `GET /api/designs` - List designs
- `GET /api/designs/:id` - Get design details
- `PUT /api/designs/:id` - Update design
- `DELETE /api/designs/:id` - Delete design

### Export
- `GET /api/designs/:id/export/pdf` - Export as PDF
- `GET /api/designs/:id/export/png` - Export as PNG

## 🎨 Example Prompts

```
"2-story house with south-facing room 12x13 feet, attached bathroom on right, carport 10 feet wide, modern style"

"Modern apartment with open kitchen-living, 3 bedrooms, 2 bathrooms, glass railings"

"Traditional Indian home with courtyard, traditional red brick materials"
```

## 🤖 AI Integration

This project uses free AI services:
- **Hugging Face Inference API** - For prompt parsing and design analysis
- **Stable Diffusion** - For generating architectural images
- **Open-source LLMs** - For design specifications

## 📦 Dependencies

See `frontend/package.json` and `backend/package.json` for complete dependency lists.

## 🐳 Docker Setup

```bash
# Build and run with Docker Compose
docker-compose up

# Access the app at http://localhost:3000
```

## 🚢 Deployment

### Vercel (Frontend)
```bash
npm run deploy:frontend
```

### Railway/Render (Backend)
See [Deployment Guide](docs/DEPLOYMENT.md) for detailed instructions.

## 📝 License

MIT License - feel free to use this project

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 💬 Support

For issues and questions, please create a GitHub issue or contact support.

---

**Happy Designing! 🏗️✨**

Built with ❤️ using AI and modern web technologies.
