# 🧠 BetMaestro

[![Watch demo on YouTube](https://img.shields.io/badge/%F0%9F%93%BD%20Demo%20on%20YouTube-red?style=for-the-badge)](https://youtu.be/gpr9XA1yVy4)
[![Watch promo video](https://img.shields.io/badge/%F0%9F%8E%A5%20Promo%20Video-purple?style=for-the-badge)](https://www.youtube.com/watch?v=MBa65teaebc&ab_channel=CokeStuyck)

---

## 🛠️ Tech Stack

- **Python**: Main language for APIs, Cloud Functions, and data processing
- **Docker**: Containerization for APIs and frontend
- **Terraform**: Infrastructure as code for GCP deployment
- **Google Cloud Platform**:
  - Cloud Functions
  - Pub/Sub
  - BigQuery
  - Cloud SQL (PostgreSQL)
  - Cloud Run
  - Cloud Storage
- **Streamlit**: Interactive frontend for data visualization
- **Next.js**: Vibe-coded frontend for presentation purposes [Link to repo](https://github.com/cokecancook/betmaestro-frontend)

---

## 🎯 Project Description

**BetMaestro** was created with a clear goal: to help users make better decisions in the world of sports betting. This project transforms data into value, automating the entire flow of ingestion, processing, and storage of sports information from different sources, and laying the foundation for future applications based on Artificial Intelligence.

---

## 🧱 Technical Architecture

The system is fully deployed on **Google Cloud Platform** and automated with **Terraform**.  
Our solution follows a modular and scalable approach, composed of:

🔹 **External APIs**  
Data obtained from [NBA API](https://github.com/swar/nba_api) and [SportsData.io](https://sportsdata.io/), including:

- Game statistics
- Betting odds
- Player injuries

🔹 **Cloud Functions**  
Python functions with different triggers:

- **Pub/Sub**: for real-time data processing
- **Cloud Storage**: for loading historical data from CSV

🔹 **Pub/Sub**  
Messaging system that decouples data producers and consumers.

🔹 **BigQuery**  
Analytical storage for massive processing and data exploration. Ready for use in AI models.

🔹 **Cloud SQL (PostgreSQL)**  
Relational database for storing structured information accessible to the backend.

🔹 **Cloud Run + Docker**  
Our internal APIs are also automatically deployed as containers.

🔹 **Streamlit**  
Interactive frontend to visualize insights and explore data easily and accessibly.

---

## 🤖 Artificial Intelligence (Future Vision)

Although the current focus has been on building a solid infrastructure, BetMaestro is already prepared to be integrated with prediction models. Thanks to structured and automated storage, it is possible to develop:

- Prediction models for results or odds
- Real-time alert systems
- Personalized recommenders based on betting patterns

All this will be possible thanks to the quality and continuity of the data pipeline we have designed.

---

## 🚀 Deployment

Full deployment is completed in a few minutes with:

```bash
terraform init
terraform apply
```

### Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed
- Google Cloud Platform account and credentials configured (`gcloud auth application-default login`)
- Python 3.9+ installed
- Docker installed (for APIs and frontend)

### Deployment Structure

1. **Terraform**: Initializes and applies infrastructure in GCP (BigQuery, Cloud SQL, Pub/Sub, Cloud Functions, Cloud Run, Storage)
2. **APIs and Cloud Functions**: Automatically deployed as containers and functions in GCP
3. **Streamlit**: Can be run locally or deployed as a container

### Example Deployment

```bash
cd terraform
terraform init
terraform apply
```

---

## 📁 Project Structure

```
README.md
AI-agent/           # AI agent for prediction and analysis
API/                # Main API for data ingestion and queries
API-AI/             # API for integration with AI models
cloudfunctions/     # Python functions for processing and triggers
data/               # Historical data and processing scripts
streamlit/          # Interactive frontend for visualization
terraform/          # Infrastructure as code (IaC) for GCP
```

- **AI-agent/**: Scripts and logic for prediction agents
- **API/**: REST endpoints for sports and betting data
- **API-AI/**: Dedicated API for AI and prediction models
- **cloudfunctions/**: Serverless functions for ingestion and processing
- **data/**: CSVs, scripts, and utilities for data handling
- **streamlit/**: Frontend app for visualization and exploration
- **terraform/**: Configuration files to deploy all infrastructure on GCP

---

## 🧪 Usage Examples

### Run API locally
```bash
cd API
python main.py
```

### Run Streamlit frontend locally
```bash
cd streamlit
streamlit run main.py
```

### Trigger a Cloud Function locally (example)
```bash
cd cloudfunctions/games
python main.py
```

### Build and run API as Docker container
```bash
cd API
docker build -t betmaestro-api .
docker run -p 8000:8000 betmaestro-api
```

---

## Authors

- [Claudia Romero](https://github.com/Claudiarg13)
- [Lara Rubio](https://github.com/lararub14)
- [Ting Wang](https://github.com/e-watch)
- [Eduardo Abad](https://github.com/eabadz)
- [Jaime Olano](https://github.com/jaimeolanolopez)
- [Coke Stuyck](https://github.com/cokecancook)
