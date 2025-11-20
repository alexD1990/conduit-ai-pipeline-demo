# conduit-ai-pipeline-demo
End-to-end AI pipeline demo using Conduit Core, dbt, and deep learning for automated anomaly detection. Built as a production-style architecture by a single engineer.

# End-to-End AI Pipeline using Conduit, dbt & Deep Learning (Local Zero-Cost Architecture)

This project demonstrates how a complete AI system can be built by a single engineer using modern tools and iterative delivery — without relying on cloud dependencies or heavy infrastructure.

The pipeline is designed for production-style architecture but implemented locally to minimize cost and accelerate development.

---

## 🎯 Objective

Build an automated AI pipeline capable of:

- Ingesting CSV data via **Conduit Core** into PostgreSQL
- Transforming and structuring features using **dbt (Core) locally in VS Code**
- Training a **deep learning Autoencoder** on “normal” data to learn patterns
- Detecting anomalies when new data arrives (simulated incremental ingestion)

The process follows a production-oriented architecture while remaining lightweight and reproducible locally.

---

## 🧠 Architectural Role

**Designed and implemented by an AI System Solution Architect**, focused on system robustness, reproducibility, and automation — not just model experimentation.

---

## 🧱 Technology Stack

| Layer | Technology |
|-------|------------|
| Data ingestion | **Conduit Core** (YAML pipelines) |
| Source DB | **PostgreSQL via Docker** |
| Transformation | **dbt Core (local)** |
| ML | Python + PyTorch (Autoencoder) |
| Dev environment | VS Code + Colab |
| Version control | GitHub |
| Containerization | Docker Compose |

> *Snowflake or other cloud data warehouses can be integrated in a later phase to demonstrate enterprise scalability.*

---

## 🔁 Pipeline Flow

```text
CSV dataset (Kaggle)
        ↓ Conduit (YAML pipeline)
PostgreSQL – raw data
        ↓ dbt (transformation in VS Code)
PostgreSQL – ml_ready table
        ↓ export → DataFrame / CSV
Colab – train Autoencoder → detect anomalies

