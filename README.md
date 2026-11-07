<div align="center">

# G. Achuth

**I build LLM systems, then measure whether they deserve to be trusted.**

Data Science @ AB InBev GCC · B.Tech CSE, VIT Chennai<br>
[achuthfolio.vercel.app](https://achuthfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/achuth-g-69104a251) · [achuthganesh09@gmail.com](mailto:achuthganesh09@gmail.com)

</div>

---

> **Abstract.** I work on data science at AB InBev GCC and on agentic AI after hours: retrieval pipelines,
> multi-step agents, and the evaluation work that tells you whether either one is any good. I'd rather know *why*
> a model works than only that it does, so most of my side projects end up as experiments. Right now that means
> checking whether LLM fact-verifiers are **calibrated**, not just accurate.
>
> **Keywords:** agentic systems · retrieval · calibration · evaluation · deep learning from first principles

&nbsp;

### 1 &nbsp;Current work

A verifier that says *0.9* should be right about 90% of the time:

$$\Pr\big(Y = 1 \mid \hat{p} = p\big) = p$$

Most LLM pipelines never check this. **Jev-Arbiter** (research code, not public yet) does, claim by claim:

- Scores atomic claims against retrieved evidence on [LLM-AggreFact](https://llm-aggrefact.github.io/) (11 datasets, 2,200 test claims)
- Thresholds were **pre-registered and committed before the test split was touched**, and the test split was scored once
- Every headline number comes with a 95% cluster-bootstrap CI
- Result: AUROC **0.877** [0.859, 0.892], ECE **0.036** after recalibration. It **missed** its pre-registered Brier
  target (0.138 vs 0.12), and the write-up reports that miss as it is

&nbsp;

### 2 &nbsp;Selected work

| Project | What it is | Built with |
|:--|:--|:--|
| **Healthcare Symptom Checker** <br> [backend](https://github.com/Achuth-0908/healthcare_symptom_checker-backend) · [frontend](https://github.com/Achuth-0908/RAG-based-Healthcare-Symptom-Checker) | RAG over medical sources with a real-time chat UI | FastAPI, Jina embeddings, ChromaDB, Gemini + Groq, Next.js |
| **JobIntel AI** <br> [backend](https://github.com/Achuth-0908/jobintel-ai-backend) · [frontend](https://github.com/Achuth-0908/JobIntel-AI) | Matches résumés to jobs and pulls out skill gaps | Flask, NLP pipeline, TypeScript |
| **AnomalyGuard** <br> [repo](https://github.com/Achuth-0908/anomalyguard-ai-powered-anomaly-detection) · [live demo](https://anomalyguard-ai.streamlit.app/) | Interactive anomaly detection you can try in the browser | scikit-learn, Streamlit |
| **Shopify Analytics** <br> [backend](https://github.com/Achuth-0908/shopify_analytics_backend) · [frontend](https://github.com/Achuth-0908/shopify_analytics_frontend) | Multi-tenant ingestion and metrics dashboard | Express, PostgreSQL, Next.js |

&nbsp;

### 3 &nbsp;Methods

<p>
  <img src="https://skillicons.dev/icons?i=py,pytorch,sklearn,fastapi,postgres,ts,nextjs,tailwind,docker,aws&theme=dark" alt="Python, PyTorch, scikit-learn, FastAPI, PostgreSQL, TypeScript, Next.js, Tailwind, Docker, AWS" />
</p>

| | |
|:--|:--|
| **Models & agents** | PyTorch · LangGraph · LangChain · Hugging Face Transformers · Pydantic |
| **Retrieval & eval** | FAISS · ChromaDB · Qdrant · pgvector · BM25 · RAGAS · Langfuse |
| **Serving & product** | FastAPI · Flask · Next.js · React · Tailwind |
| **Data & infra** | PostgreSQL · MongoDB · AWS · Docker · GitHub Actions |

&nbsp;

### 4 &nbsp;Open questions

Things I keep returning to. If you have a good answer, I'd like to hear it.

1. Why do overparameterised networks generalise when classical theory says they shouldn't?
2. Five LLM judges that agree with each other: how many *independent* votes is that, really?
3. What does "calibrated" mean for an agent that acts, rather than one that only predicts?

&nbsp;

---

<div align="center">
<sub><i>"The purpose of computing is insight, not numbers."</i> · Richard Hamming</sub>
</div>
