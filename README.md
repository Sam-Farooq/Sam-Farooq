## Ahtisham Farooq

Senior software engineer based in France. I work on the back half of systems:
retrieval pipelines, streaming data, and the infrastructure both run on.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)

---

### Projects

**[rag-agent](https://github.com/Sam-Farooq/rag-agent)** · LangGraph · Qdrant · Langfuse
> RAG systems answer confidently from the model's own memory the moment
> retrieval comes back thin. This one grades retrieval and grounding as two
> separate gates, retries with a rewritten query, and refuses outright when
> both stay weak. Refusal is a terminal state, not an error path.

**[lakehouse-pipeline](https://github.com/Sam-Farooq/lakehouse-pipeline)** · Kafka · PySpark · Delta Lake · dbt
> Kafka is at-least-once, so the same transaction arrives twice whenever a
> consumer rebalances, and a duplicated payment in a daily total gets noticed
> by someone outside engineering. Bronze keeps everything for replay, silver
> deduplicates inside a watermark, gold aggregates one partition at a time.

**[model-serving](https://github.com/Sam-Farooq/model-serving)** · PyTorch · MLflow · Celery
> Input distributions drift long before there are labels to measure accuracy
> against. This tracks PSI on the served score distribution instead, and
> refuses to start if the feature order recorded in the model artifact
> disagrees with the serving schema, because that failure is otherwise silent.

**[hybrid-search](https://github.com/Sam-Farooq/hybrid-search)** · Elasticsearch · Qdrant
> Dense retrieval collapses on identifiers, because an embedding of a
> reference number sits close to every other reference number. BM25 and vector
> search fused with reciprocal rank fusion, which reads only the ranks, so
> there is nothing to normalise and nothing to retune per corpus.

**[eks-infra](https://github.com/Sam-Farooq/eks-infra)** · Terraform · EKS · Helm
> The cluster the rest of it deploys onto. NAT per AZ in prod and one shared
> in staging, spot for Spark executors behind a taint, and node updates capped
> at one unavailable so a rolling upgrade cannot drain a third of the capacity.

---

### How I tend to build

- Fail at startup, not on the first request. A contract mismatch that only
  shows up under traffic is already in a load balancer rotation.
- Reject unexpected values rather than defaulting them. Defaulting an unknown
  currency to EUR turns a visible failure into a silent one.
- Write down the decision, not the behaviour. Every README here explains why a
  threshold is where it is, because that is the part nobody can read off the code.

### Elsewhere

[LinkedIn](https://linkedin.com/in/ahtisham-farooq-3a449b356) · ahtishamm.farooq@gmail.com
