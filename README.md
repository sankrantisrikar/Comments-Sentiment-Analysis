# 📺 Real-Time YouTube Comments Sentiment Analysis | Modern GCP Data Engineering Project  

![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?logo=ansible&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white)
![Apache Beam](https://img.shields.io/badge/Apache%20Beam-F47E20?logo=apache&logoColor=white)
![Dataflow](https://img.shields.io/badge/Dataflow-1A73E8?logo=googlecloud&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?logo=googlebigquery&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Cloud%20Composer-017CEE?logo=apacheairflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)
![CI/CD](https://img.shields.io/badge/CI%2FCD-000000?logo=githubactions&logoColor=white)

---

## 📌 Project Overview
This project demonstrates an **end-to-end real-time data engineering pipeline** on **Google Cloud Platform (GCP)** — automating infrastructure with **Terraform**, provisioning configurations via **Ansible**, orchestrating CI/CD with **Jenkins**, and visualizing live sentiment data in **Power BI**.

We capture **YouTube comments in real time**, analyze their **sentiment using NLP**, and stream them through a fully managed GCP data stack — mirroring how real-world enterprises handle **streaming analytics** and **data automation**.

👉 Think of it as a **production-grade cloud pipeline** combining **Data Engineering + DevOps + AI**.

---

## 🏗️ Architecture  

<img width="5925" height="3212" alt="Architecture_" src="https://github.com/user-attachments/assets/246fc228-a001-43c1-94cc-d4d3bdbbb921" />

**Pipeline Flow:**
1. **YouTube API + Python** → Collects live YouTube comments via Google API.  
2. **Pub/Sub** → Ingests real-time comment streams into GCP.  
3. **Dataflow (Apache Beam)** → Processes comments, applies **sentiment analysis**, and writes output to **BigQuery**.  
4. **BigQuery** → Central data warehouse for analytics and dashboards.  
5. **Cloud Composer (Airflow)** → Orchestrates and monitors workflow DAGs.  
6. **Power BI** → Connects to BigQuery for live dashboards and insights.  
7. **Terraform + Ansible + Jenkins** → Automates setup, deployment, and CI/CD of the entire infrastructure.  

---

## ⚡ Tech Stack
- **Google Cloud Platform (GCP)** → Core infrastructure  
- **Terraform** → Infrastructure as Code (IaC)  
- **Ansible** → Automated configuration management  
- **Jenkins** → CI/CD pipeline automation  
- **Pub/Sub** → Real-time message streaming  
- **Dataflow (Apache Beam)** → Data transformation and sentiment scoring  
- **BigQuery** → Scalable cloud data warehouse  
- **Cloud Composer (Airflow)** → Workflow orchestration  
- **Power BI** → Visualization and real-time reporting  
- **Python** → API integration, ETL logic, and NLP sentiment analysis  

---

## ✅ Key Features
- ⚙️ **Infrastructure as Code** with Terraform for reproducible environments  
- 🤖 **Ansible automation** for dependency setup and service configurations  
- 🧩 **CI/CD pipelines** in Jenkins for automated deployment  
- 📡 **Real-time ingestion** using Pub/Sub and streaming pipeline  
- 🧠 **Sentiment Analysis** applied to YouTube comments using NLP  
- 💾 **BigQuery as central warehouse** for query and reporting  
- 🎛️ **Cloud Composer DAGs** for scheduled orchestration and monitoring  
- 📊 **Interactive Power BI dashboard** for live insights (top sentiments, word clouds, comment trends)  

---

## 📂 Repository Structure
```text
yt-comments-gcp/
├───ansible
│   ├───group_vars
│   │   └───all.yml
│   └───playbooks
│   │   └───deploy_cf.yml
│   │   └───deploy_dag.yml
│   │   └───deploy_dataflow.yml
│   │   └───run_pretrained_sentiment.yml
├───app
│   ├──config.yaml
│   ├──main.py
│   ├──requirements.txt
├───commands
│   ├──VM_initial.txt
│   ├──tree_create.txt
│   ├──yt-comments_procedure.docx
├───dags
│   ├──yt_pipeline_dag.py
├───dataflow
│   ├──config.yaml
│   ├──pipeline.py
│   ├──requirements.txt
│   ├──setup.py
├───infra
│   ├───envs
│   │   └───dev
│   │   │   ├───main.tf
│   │   │   ├───outputs.tf
│   │   │   └───variables.tf
│   └───modules
│   │   ├───bigquery
│   │   │   └───main.tf
│   │   ├───composer
│   │   │   └──main.tf
│   │   ├───iam
│   │   │   └──main.tf
│   │   ├───pubsub
│   │   │   └──main.tf
│   |   └───storage
│   │   │   └──main.tf
│   └───backend.tf
│   └───providers.tf
├───ml
│   └───pretrained_sentiment.py
├───.gitignore
├───Jenkinsfile
└───README.md
```

## ⚙️ Step-by-Step Implementation  

### **1. Infrastructure Setup with Terraform**  
- Defined **GCP resources** including Pub/Sub topics, Dataflow jobs, BigQuery datasets, and IAM roles.  
- Automated provisioning using `terraform apply`.  

---

### **2. Configuration Management with Ansible**  
- Installed required packages and dependencies across **VMs and Jenkins**.  
- Managed **service account permissions** and **environment variables** centrally.  

---

### **3. CI/CD Automation with Jenkins**  
- Integrated **Jenkins with GitHub** for automated builds and deployments on every commit.  
- Triggered **Terraform** and **Ansible** workflows for full infrastructure + config automation.  

---

### **4. Real-Time Data Ingestion**  
- **YouTube API + Python script** fetches live comments and publishes them to **Pub/Sub** in real time.  

---

### **5. Stream Processing with Dataflow**  
- Built an **Apache Beam pipeline** to transform and classify comment sentiments (**Positive**, **Negative**, **Neutral**).  
- Stored structured results into **BigQuery** for analytics and visualization.  

---

### **6. Orchestration with Cloud Composer**  
- Created **Airflow DAGs** to automate daily health checks, batch jobs, and metadata validation tasks.  

---

### **7. Visualization with Power BI**  
- Connected **BigQuery → Power BI** to visualize real-time dashboards showing:  
  - Sentiment trends  
  - Comment volumes  
  - Regional and time-based insights  

---

## 📊 Final Deliverables  
✅ Automated **GCP infrastructure** via Terraform  
✅ Full **CI/CD pipeline** using Jenkins  
✅ Real-time **YouTube comments ingestion** with Pub/Sub  
✅ Stream processing & **sentiment classification** with Dataflow  
✅ Centralized storage in **BigQuery**  
✅ Workflow automation with **Cloud Composer**  
✅ Live **Power BI dashboard** showing sentiment insights  

---

## 🧠 Insights from Dashboard  
- Sentiment distribution across comments (**Positive / Neutral / Negative**)  
- Most active commenters and channels  
- Real-time comment volume trends  
- Geographic and time-based sentiment shifts  

---

## 🧩 Future Enhancements  
- Integrate **Looker Studio** as an alternative BI layer  
- Add a custom **NLP model using Vertex AI** for fine-tuned sentiment detection  
- Extend ingestion to **multiple YouTube channels concurrently**  
- Implement **alerting system** for spikes in negative sentiment  

---

**Author:** *Srikar Sankranti*  
*Texas A & M University*
flowchart LR
    A[X12 837 Claim] --> B[Parse 837 to JSON]
    C[X12 835 ERA] --> D[Parse 835 to JSON]

    B --> E[Claim–ERA Reconciliation Engine]
    D --> E

    F[Prior Auth] --> G[Document Retrieval]
    H[Supporting Docs] --> G
    I[Payer Guidelines] --> G

    G --> J[Summarized History Builder]
    E --> K[Feature Engineering / Signal Extractor]
    J --> L[Context Pack Builder]
    K --> L

    L --> M[Rules Engine]
    L --> N[LLM Reasoning Layer]

    M --> O[Checklist Generator]
    N --> O

    O --> P[UI – Persistent Checklist]

    P --> Q[Human Feedback Loop]
    Q --> K

    P --> R[Correct Claim Checklist]
