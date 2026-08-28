<div align="center">
  <img src="./assets/banner.svg" alt="Amritanshu Jha — Senior Software Engineer, Distributed Architecture, Backend Systems and Data platforms" width="100%" />
</div>

<br />

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3500&pause=900&color=58A6FF&center=true&vCenter=true&width=820&height=46&lines=Building+systems+that+hold+up+under+real+load;Spark+on+Kubernetes+%C2%B7+Iceberg+lakehouses+%C2%B7+low-latency+APIs;Go+%C2%B7+Java+%C2%B7+C%2B%2B+%C2%B7+Python" alt="Typing headline" />
</div>

<div align="center">
  <a href="https://github.com/amritanshuj"><img src="https://img.shields.io/badge/GitHub-amritanshuj-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://linkedin.com/in/amritanshu-jha"><img src="https://img.shields.io/badge/LinkedIn-amritanshu--jha-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:amritanshu.jha10@gmail.com"><img src="https://img.shields.io/badge/Email-amritanshu.jha10%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Based_in-Bengaluru-238636?style=for-the-badge" alt="Bengaluru" />
</div>

---

I write backends for the moments when traffic spikes, datasets stop fitting in memory, and “it worked in staging” is no longer an argument.

Right now that’s **Salesforce’s Security Data Platform** — Spark on Kubernetes, Iceberg/S3 lakehouses, Go APIs, and the kind of caching, incremental processing, and rollout machinery you only bother building after you’ve been paged for it.

Previously: **Swiggy Delivery Platform** (Java/Go microservices, gRPC, DynamoDB, Kafka) and **OYO Payments**.

```bash
$ cat ~/.gitconfig | grep -A6 '\[user\]'
name  = Amritanshu Jha
role  = Senior Software Engineer
now   = distributed systems, data platforms, reliability
stack = go, java, cpp, python, spark, iceberg, k8s, aws
from  = Salesforce · ex-Swiggy · ex-OYO
```

## now playing

- Leading **Glue → Spark-on-Kubernetes** for multi-TB security ETL: 34 pipelines, 210+ jobs, shared K8s/EC2, no Glue bookmarks to hide behind.
- Rebuilding query paths on **Iceberg + ElastiCache** so security APIs stay in the millisecond club instead of the “please refresh” club.
- Contract-driven **SLA monitoring** (freshness, availability, latency) with Grafana + PagerDuty — because dashboards nobody pages on are just wallpaper.
- Rolling production upgrades (Splunk 8 → 9 on a **252 TB/day** cluster) with the boring kind of success: nobody noticed.

<details>
<summary><strong>a few numbers, if you like receipts</strong></summary>

<br />

| signal | what actually happened |
| --- | --- |
| compute | **73%** lower annual Spark spend (**$1.74M**) after leaving Glue |
| jobs | **42%** faster average runtime on the same security ETL estate |
| APIs | p95 **1.2s → 115ms** on Vulnerability Data API (~**90%**), **77%** cache hit ratio |
| delivery | Swiggy **MVP FY21–22** — New Year peak at **10k+ orders/min** without SLA burn |
| traffic | Delivery path held **300k+ req/min** after monolith → Java/Go + gRPC + DynamoDB |

</details>

## toolbox

<div align="center">
  <img src="https://skillicons.dev/icons?i=cpp,java,go,python,spring,kafka,redis,postgres,aws,kubernetes,docker,linux,grafana,prometheus,git,githubactions" alt="Core stack icons" />
</div>

<br />

<div align="center">

![Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Iceberg](https://img.shields.io/badge/Apache_Iceberg-1E2E3C?style=for-the-badge&logo=apache&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=for-the-badge&logo=amazondynamodb&logoColor=white)
![S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![EKS](https://img.shields.io/badge/Amazon_EKS-FF9900?style=for-the-badge&logo=amazoneks&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=for-the-badge&logo=grpc&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![PagerDuty](https://img.shields.io/badge/PagerDuty-06AC38?style=for-the-badge&logo=pagerduty&logoColor=white)

</div>

**Languages** — C++, Java (Spring Boot), Go, Python (Flask / FastAPI), SQL  
**Data plane** — Spark, Iceberg, Parquet, Glue, Airflow, DynamoDB, PostgreSQL, Redis / ElastiCache, S3  
**Control plane** — EKS, EC2, Docker, Helm, Argo Rollouts (blue/green), IAM, KMS, Vault, mTLS  
**Messaging** — Kafka, SNS / SQS, EventBridge, gRPC, REST  
**Reliability** — Prometheus, Grafana, Splunk, New Relic, PagerDuty, CI/CD that can actually roll back  
**GenAI, when it earns its keep** — LangChain, RAG, vector stores, Hugging Face, MCP

## how I think about systems

```mermaid
flowchart LR
  A[Events and objects] --> B[Ingest]
  B --> C[Incremental state]
  C --> D[Spark on K8s]
  D --> E[Iceberg / S3]
  E --> F[Go APIs]
  F --> G[Redis]
  G --> H[Dashboards &amp; automations]
  D --> I[SLAs]
  I --> J[Grafana]
  I --> K[PagerDuty]
```

If a pipeline can’t prove freshness, an API can’t survive a stampede, or a deploy can’t roll back in minutes, it isn’t done.

## public repos

Most of the interesting production code lives behind work walls. What’s out here is the public trail — side systems, product experiments, and the stuff I still like opening.

<div align="center">
  <a href="https://github.com/amritanshuj/SmartLink-URL-Shortener">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=amritanshuj&repo=SmartLink-URL-Shortener&theme=github_dark&hide_border=true" alt="SmartLink URL Shortener" />
  </a>
  <a href="https://github.com/amritanshuj/QuickShare">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=amritanshuj&repo=QuickShare&theme=github_dark&hide_border=true" alt="QuickShare" />
  </a>
</div>
<div align="center">
  <a href="https://github.com/amritanshuj/SocialPal">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=amritanshuj&repo=SocialPal&theme=github_dark&hide_border=true" alt="SocialPal" />
  </a>
  <a href="https://github.com/amritanshuj/Voice-Assistant">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=amritanshuj&repo=Voice-Assistant&theme=github_dark&hide_border=true" alt="Voice Assistant" />
  </a>
</div>

## telemetry

<div align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=amritanshuj&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=amritanshuj&layout=compact&theme=github_dark&hide_border=true&langs_count=8" alt="Top languages" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com?user=amritanshuj&theme=github-dark-blue&hide_border=true" alt="GitHub streak" />
</div>

## elsewhere

<div align="center">

**[github.com/amritanshuj](https://github.com/amritanshuj)** · **[linkedin.com/in/amritanshu-jha](https://linkedin.com/in/amritanshu-jha)** · **[amritanshu.jha10@gmail.com](mailto:amritanshu.jha10@gmail.com)**

<br />

<img src="https://komarev.com/ghpvc/?username=amritanshuj&label=profile%20views&color=58a6ff&style=flat-square" alt="Profile views" />

</div>
