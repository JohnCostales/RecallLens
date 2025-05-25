# RecallLens: AI-Powered Visual Memory for Remote Work & Learning

> Turn any meeting, lecture, or tutorial into a **searchable, multimodal knowledge base**—with deep AI insight into both speech and visuals.

---

## ✨ Features

- Upload or connect remote meeting/lecture recordings
- AI-generated summaries for every segment
- Visual timeline with slide/diagram detection
- “Ask the Meeting”: Natural language Q&A (audio + visual context)
- Tag and filter by topics, speakers, slides, or screen shares
- Export highlights and action items
- Secure, scalable, and privacy-first

---

## 🚀 Quick Start

1. **Clone the repo**
2. **Install backend and frontend dependencies**
3. **Set up HuggingFace keys and auth config**
4. **Run backend and frontend locally (Docker-compose or Railway)**
5. **Connect your Zoom/Meet/YouTube account or upload a file**
6. **Open `localhost:3000` to use RecallLens!**

---

## 🏗️ System Architecture

| Section/Component        | Purpose / Role                                                    | Technology / Examples                  |
|------------------------- |-------------------------------------------------------------------|----------------------------------------|
| **User / Client**        | Initiates uploads, connects video sources, interacts with results | Web browser, mobile app                |
| **Frontend**             | User interface for uploads, search, results display               | React, Tailwind CSS                    |
| **API Gateway**          | Handles routing, integrates auth, connects frontend & backend     | API layer, handles Auth0/Firebase      |
| **Auth**                 | Authenticates users, manages sessions                             | Auth0, Firebase                        |
| **Integration APIs**     | Connects to Zoom, YouTube, LMS for source videos                  | Zoom API, YouTube API, LMS API         |
| **Backend**              | Orchestrates all processing, manages data flow                    | FastAPI (Python)                       |
| **Task Queue**           | Runs async, distributed jobs for processing                       | Celery                                 |
| **Video Processor**      | Extracts frames, audio, visuals from video                        | FFmpeg, OpenCV                         |
| **ML Processing**        | Runs AI/ML models: transcription, summarization, QA, tagging      | HuggingFace Transformers               |
| **Frame/Image Extraction**| Analyzes visuals (slides, diagrams, shared docs)                 | OpenCV, ML models                      |
| **Storage**              | Stores all files, metadata, and search indexes                    | S3 (files), PostgreSQL (metadata),     |
|                          |                                                                   | Elasticsearch (semantic search)        |
| **Search / Retrieval**   | Provides fast, structured search & retrieval                      | Elasticsearch, API queries             |

### **Components**
- **Frontend:** React (Next.js) + TailwindCSS
- **Backend:** FastAPI + Celery + PostgreSQL + S3 + Elasticsearch
- **AI Pipelines:**  
  - Speech-to-text  
  - Video/image-to-text  
  - Visual Q&A  
  - Video summarization/classification
- **Integrations:** Zoom, YouTube, LMS APIs
- **Auth:** Auth0/Firebase

---

## 🔑 Key AI Tasks (HuggingFace)

| Task                   | Example Model(s)           | Purpose                                         |
|------------------------|----------------------------|-------------------------------------------------|
| Speech-to-Text         | whisper-large              | Transcribe meetings/lectures                    |
| Video-Text-to-Text     | blip2, flamingo            | Summarize video segments                        |
| Visual QA              | OFA, blip2                 | Answer “what’s on screen” queries               |
| Image-to-Text          | Donut, pix2struct          | Describe slides, diagrams                       |
| Doc QA                 | layoutLMv3                 | Extract from shared documents                   |
| Video Classification   | timesformer, mvit          | Tag “presentation”, “Q&A”, “discussion”, etc.   |

---

## 💡 Why RecallLens?

- **Save hours** by jumping to the exact moment you need.
- **Don’t miss key visuals:** Find slides, diagrams, or shared docs instantly.
- **Better remote learning:** Retrieve context-rich moments from any lecture or training.

---

## 🛠️ Tech Stack

| Layer      | Technology                                |
|------------|-------------------------------------------|
| Frontend   | React (Next.js), TailwindCSS              |
| Backend    | FastAPI, Celery, PostgreSQL               |
| ML         | HuggingFace Transformers/Inference API    |
| Video      | FFmpeg, OpenCV                            |
| Storage    | S3                                        |
| Search     | Elasticsearch                             |
| Auth       | Auth0/Firebase                            |
| Deploy     | Docker, K8s, AWS/Railway                  |
| Integrate  | Zoom/Meet/YouTube APIs                    |

---

## 📈 Portfolio Value

- Multimodal AI integration (audio, video, images)
- Scalable cloud-native architecture
- Asynchronous, resilient processing
- Real UX for real pain points (remote work, e-learning)
- SaaS/product potential (Notion, Slack, enterprise integrations)

---

## 🤖 Getting Started (Dev Notes)

- Use provided scripts for local demo with sample videos (public datasets listed below)
- Configure HuggingFace and API keys in `.env.example`
- (See `CONTRIBUTING.md` for dev setup and architecture details)

---

## 🗃️ Useful Datasets & APIs

- [AMR Meeting Corpus](https://catalog.ldc.upenn.edu/LDC2004T12)
- [YouTube-8M](https://research.google.com/youtube8m/)
- [ICCV-VQA](https://www.robots.ox.ac.uk/~vgg/data/vqa/)
- [Zoom API](https://marketplace.zoom.us/docs/api-reference/zoom-api/)
- [Google Meet API](https://developers.google.com/calendar/api/v3/reference/)

---

## 📢 Demo & Screenshots

*(Coming soon: GIFs and walkthroughs!)*

---

## 🏆 License & Contact

MIT License.  
Questions? PRs welcome!
