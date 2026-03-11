# RAG Observability Platform — Task Tracker

## Legend
- [ ] Pending
- [~] In Progress
- [x] Completed

---

## Milestone 1 — Project Foundation

- [x] **Task 1.1** — Create repository and folder structure
- [x] **Task 1.2** — Create `requirements.txt` with all dependencies
- [x] **Task 1.3** — Create `.env.example` with required environment variables
- [x] **Task 1.4** — Create `docker-compose.yml` for Langfuse + Postgres
- [x] **Task 1.5** — Verify Langfuse starts and UI is accessible

---

## Milestone 2 — RAG Pipeline (Core)

- [ ] **Task 2.1** — Build `retriever.py` — embed query + ChromaDB search
- [ ] **Task 2.2** — Build `prompt_builder.py` — assemble context + system prompt
- [ ] **Task 2.3** — Build `llm_client.py` — OpenAI call + token extraction
- [ ] **Task 2.4** — Build `reranker.py` — optional cross-encoder reranking
- [ ] **Task 2.5** — Build `scripts/ingest.py` — load documents into ChromaDB
- [ ] **Task 2.6** — Integration test: run full RAG pipeline end-to-end

---

## Milestone 3 — Observability Layer

- [ ] **Task 3.1** — Build `tracer.py` — Langfuse trace + span wrappers
- [ ] **Task 3.2** — Build `cost_tracker.py` — token count → USD cost
- [ ] **Task 3.3** — Build `metrics.py` — Prometheus histograms + counters
- [ ] **Task 3.4** — Instrument `retriever.py` with trace spans
- [ ] **Task 3.5** — Instrument `llm_client.py` with trace spans + cost
- [ ] **Task 3.6** — Verify traces appear in Langfuse UI end-to-end

---

## Milestone 4 — FastAPI Application

- [ ] **Task 4.1** — Build `api/main.py` — FastAPI app with lifespan
- [ ] **Task 4.2** — Build `api/routes.py` — `POST /query` endpoint
- [ ] **Task 4.3** — Add `GET /health` and `GET /metrics` endpoints
- [ ] **Task 4.4** — Test API with curl / Postman

---

## Milestone 5 — Dashboard

- [ ] **Task 5.1** — Build `dashboard/app.py` — latency trend chart
- [ ] **Task 5.2** — Add cost per request chart
- [ ] **Task 5.3** — Add citation coverage % metric
- [ ] **Task 5.4** — Add failure rate metric

---

## Milestone 6 — Evaluation + Regression Gate

- [ ] **Task 6.1** — Create `golden_dataset/dataset.jsonl` with 10 seed records
- [ ] **Task 6.2** — Build `evaluator.py` — RAGAS faithfulness + relevance
- [ ] **Task 6.3** — Build `run_rag_evaluation.py` — CI entry point with threshold checks
- [ ] **Task 6.4** — Create `.github/workflows/rag_eval.yml` — GitHub Actions CI
- [ ] **Task 6.5** — Test CI locally with `act` or push a test PR

---

## Progress Summary

| Milestone | Total | Completed | Remaining |
|-----------|-------|-----------|-----------|
| M1 — Foundation | 5 | 5 | 0 |
| M2 — RAG Pipeline | 6 | 0 | 6 |
| M3 — Observability | 6 | 0 | 6 |
| M4 — FastAPI | 4 | 0 | 4 |
| M5 — Dashboard | 4 | 0 | 4 |
| M6 — Evaluation | 5 | 0 | 5 |
| **Total** | **30** | **5** | **25** |
