<div align="center">

# Ahtisham Farooq

**Senior Software Engineer** · Retrieval systems, streaming data, and the infrastructure under both

France · Open to remote

<a href="https://linkedin.com/in/ahtisham-farooq-3a449b356"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:ahtishamm.farooq@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>

</div>

---

### Projects

<table>
<tr>
<td width="50%">
<a href="https://github.com/Sam-Farooq/rag-agent"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Sam-Farooq&repo=rag-agent&theme=github_dark&hide_border=true&bg_color=00000000" alt="rag-agent"></a>
<p>Grades its own retrieval, retries, and <b>refuses</b> rather than answering from memory.</p>
</td>
<td width="50%">
<a href="https://github.com/Sam-Farooq/lakehouse-pipeline"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Sam-Farooq&repo=lakehouse-pipeline&theme=github_dark&hide_border=true&bg_color=00000000" alt="lakehouse-pipeline"></a>
<p>Kafka is at-least-once, so a duplicated payment reaches the daily total. This stops it.</p>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/Sam-Farooq/model-serving"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Sam-Farooq&repo=model-serving&theme=github_dark&hide_border=true&bg_color=00000000" alt="model-serving"></a>
<p>Watches input drift before labels exist, and refuses to boot on a feature-order mismatch.</p>
</td>
<td width="50%">
<a href="https://github.com/Sam-Farooq/hybrid-search"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Sam-Farooq&repo=hybrid-search&theme=github_dark&hide_border=true&bg_color=00000000" alt="hybrid-search"></a>
<p>Vector search collapses on identifiers. BM25 and embeddings fused by rank, not score.</p>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/Sam-Farooq/eks-infra"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Sam-Farooq&repo=eks-infra&theme=github_dark&hide_border=true&bg_color=00000000" alt="eks-infra"></a>
<p>Production EKS in Terraform, with every convenient-but-wrong default overridden.</p>
</td>
<td width="50%">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sam-Farooq&layout=compact&theme=github_dark&hide_border=true&bg_color=00000000&langs_count=6" alt="Languages">
<p><sub>Python for services and pipelines, HCL for the infrastructure under them.</sub></p>
</td>
</tr>
</table>

### Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

<details>
<summary><b>How the five repositories fit together</b></summary>

<br>

```mermaid
flowchart LR
    SRC[["events · documents"]]
    SRC --> LP["lakehouse-pipeline"]
    SRC --> HS["hybrid-search"]
    LP --> MS["model-serving"]
    HS --> RA["rag-agent"]
    MS --> EKS["eks-infra"]
    RA --> EKS

    classDef data fill:#0B3D2E,stroke:#16A34A,color:#E8F5EE
    classDef ml fill:#3B1E54,stroke:#A855F7,color:#F3E8FF
    classDef infra fill:#1E3A5F,stroke:#3B82F6,color:#E0EDFF
    classDef src fill:#262626,stroke:#525252,color:#D4D4D4
    class SRC src
    class LP,HS data
    class MS,RA ml
    class EKS infra
```

Data lands and is made trustworthy on the left, models and retrieval sit in the
middle, everything runs on the right.

</details>

### How I build

**Fail at startup, not on the first request.** A contract mismatch that surfaces under traffic is already serving users.

**Reject unexpected values, do not default them.** Defaulting an unknown currency to EUR turns a visible failure into a silent one.

**Write down the decision, not the behaviour.** Every README here says why a threshold sits where it does.
