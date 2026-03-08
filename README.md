# 🚀 Landing Page Remaster Agent

A high-performance, autonomous CRO (Conversion Rate Optimization) agent that analyzes existing landing pages and generates high-converting remasters with integrated brand assets.

## 👨‍💻 Team: Marketing Vibe Coders
- **Alina East**
- **Ludovica Toscano**

---

## 🏗️ Technical Architecture

### 1. Frontend (Dashboard)
- **Tech Stack**: Vanilla HTML5, CSS3 (Glassmorphism), JavaScript (ES6+).
- **Hosting**: Google Cloud Storage Static Website.
- **Features**:
  - Live status tracking of the 3-phase generation process.
  - Interactive "Strategic Audit" view.
  - Real-time "Visual Preview" iframe rendering.

### 2. Backend (Engine)
- **Tech Stack**: Node.js 20, Google Cloud Functions (Gen 1).
- **Core Intelligence**: Gemini 1.5 Flash & Gemini 1.5 Pro (via Google Generative AI SDK).
- **Stability Features**:
  - **Universal Failover**: Automatically cycles through multiple models to bypass quota limits.
  - **Brand API Integration**: Real-time extraction of company logos and favicons (via Clearbit & Google).
  - **Robust Parsing**: Custom regex-based HTML extraction to ensure 100% reliable rendering even with malformed AI responses.

## 🛠️ Deployment & Maintenance

### Deploy Backend
```bash
gcloud functions deploy LandingPageMakeover \
  --runtime nodejs20 \
  --trigger-http \
  --allow-unauthenticated \
  --region us-central1
```

### Deploy Frontend
```bash
gsutil cp -r src/* gs://landing-page-agent-489615-site/
```

---

*This project was built to revolutionize how marketing teams prototype and iterate on landing page designs.*
