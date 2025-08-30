# 🤖 AI CV Personalizer

An intelligent CV personalization tool that leverages AI to analyze your LinkedIn and GitHub profiles, then generates tailored CVs for specific job descriptions.

## ✨ Features

- **🧠 AI-Powered Analysis**: Uses Google Gemini 2.0 Flash for intelligent profile analysis
- **🔗 GitHub Integration**: Analyzes your GitHub repositories and projects
- **� LinkedIn Data**: Integrates professional experience from LinkedIn
- **🎯 Job Matching**: Personalizes CV content based on job descriptions
- **📱 Modern Frontend**: React + TypeScript interface with Material-UI
- **📄 PDF Export**: Generate professional PDF CVs
- **📊 Project Selection**: Automatically selects the 3 most relevant projects

## 🏗️ Architecture

### Backend
- **FastAPI**: High-performance API server
- **CrewAI**: Multi-agent AI system for CV generation
- **Google Gemini 2.0 Flash**: Advanced language model
- **GitHub API**: Reliable repository data extraction

### Frontend
- **React + TypeScript**: Type-safe frontend development
- **Material-UI**: Modern component library
- **React Router**: Client-side routing
- **Styled Components**: CSS-in-JS styling

## 🚀 Démarrage rapide

### 1. Installation automatique
```bash
# Tout installer d'un coup
./start.sh
```

### 2. Configuration de l'API Gemini
```bash
# Copier la clé API dans backend/.env
cd backend
echo "GOOGLE_API_KEY=votre_cle_api_ici" > .env
```

### 3. Lancement (2 terminaux)

**Terminal 1 - Backend :**
```bash
cd backend
uv run uvicorn main:app --reload
# API sur http://localhost:8000
```

**Terminal 2 - Frontend :**
```bash
cd frontend  
npm start
# Interface sur http://localhost:3000
```

## 🎨 Interface utilisateur

- **Zone de saisie** : Description du poste à gauche
- **Affichage CV** : Résultat personnalisé à droite  
- **Sidebar historique** : Toutes vos conversations
- **Téléchargements** : Boutons d'export intégrés

## 🔧 Technologies

- **Frontend** : React 18, Tailwind CSS, Axios, React-Markdown
- **Backend** : FastAPI, Uvicorn, Pydantic
- **IA** : CrewAI, Google Gemini 2.0 Flash
- **Stockage** : Système de fichiers (extensible DB)

## 📁 Structure des dossiers

```
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Sidebar.js
│   │   │   ├── CVDisplay.js
│   │   │   └── JobDescriptionForm.js
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
├── backend/
│   ├── main.py              # API FastAPI
│   ├── crew.py              # Agents CrewAI
│   ├── crew_main.py         # CLI CrewAI
│   ├── pyproject.toml       # Dépendances uv
│   ├── knowledge/
│   │   └── linkedin_data.json
│   └── RECOMMENDATIONS/
└── start.sh                 # Script d'installation
```

## 🔑 Endpoints API

- `POST /generate-cv` : Génération de CV
- `GET /history` : Historique des conversations  
- `GET /cv/{id}` : Récupération d'un CV
- `GET /download/{id}` : Téléchargement de CV

## 🎯 Prochaines fonctionnalités

- [ ] Base de données persistante
- [ ] Authentification utilisateur
- [ ] Templates de CV multiples
- [ ] Export PDF
- [ ] Analyse de compatibilité
- [ ] Suggestions d'amélioration

---

**Développé avec ❤️ par l'équipe AI CV Personalizer**



