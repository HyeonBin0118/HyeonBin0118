# Hi, I'm HyeonBin 👋
AI/백엔드 개발자를 목표로 프로젝트를 설계하고 있습니다.
기능 구현에 그치지 않고 가설을 세우고 데이터로 검증하는 방식으로 개발합니다.
RAG 성능 평가, 캐싱 효과 측정, 비동기 처리 개선 등 수치로 결과를 기록합니다.

---

## 🔍 NLP / RAG
- **[shopping-faq-rag](https://github.com/HyeonBin0118/shopping-faq-rag)** — 쇼핑몰 FAQ + 상품 + 리뷰 기반 RAG 챗봇, Ollama vs OpenAI RAGAs 비교
  `LangChain` `ChromaDB` `GPT-4o-mini` `Streamlit`
- **[shopping-rag-v2](https://github.com/HyeonBin0118/shopping-rag-v2)** — v1 개선, 리뷰 한국어 번역 + Cohere Re-ranking + Streamlit Cloud 배포
  `Cohere Rerank` `GPT-4o-mini` · [🚀 Demo](https://shopping-rag-v2-db2ox3udz3gbsunb7m8jbq.streamlit.app)
- **[shopping-rag-v3](https://github.com/HyeonBin0118/shopping-rag-v3)** — v2 개선, GPT-4o Vision 이미지 검색 + 카테고리 필터링 + 합성 데이터 생성
  `GPT-4o Vision` `Cohere Rerank` `GPT-4o-mini` · [🚀 Demo](https://shopping-rag-v3-ndnwefdv24yp6vsfqxnmzq.streamlit.app)
- **[shopping-rag-v4](https://github.com/HyeonBin0118/shopping-rag-v4)** — v3 성능 정량 평가, RAGAs 텍스트 평가 + 이미지 검색 Hit@K 평가 + 결과 시각화
  `RAGAs` `Matplotlib` · Faithfulness 0.85 / Hit@K 71.4%
- **[shopping-rag-final](https://github.com/HyeonBin0118/shopping-rag-final)** — ShopAI 최종 완성판, 챗봇 + 이미지 검색 + RAGAs 성능 대시보드 통합
  `GPT-4o Vision` `Cohere Rerank` `RAGAs` · [🚀 Demo](https://shopping-rag-final-2uvz8tccm5pucljl8spjrc.streamlit.app) · [🎬 영상](https://youtu.be/AAxJZN74ZiU)

---

## 🤖 LLM Agent
- **[job-agent](https://github.com/HyeonBin0118/job-agent)** — 채용공고 분석 Agent v1, FastAPI + LangGraph 기반 파이프라인 설계
  `LangGraph` `FastAPI` `GPT-4o-mini` `Streamlit` · [🚀 Demo](https://job-agent-fiyd3jcmzx92at9t7p7zq2.streamlit.app)
- **[job-agent-v2](https://github.com/HyeonBin0118/job-agent-v2)** — v1 개선, 사이드바 UX + 자소서 길이/포맷 커스터마이징 + AI 상담 채팅
  `LangGraph` `GPT-4o-mini` `Streamlit` · [🚀 Demo](https://job-agent-v2-24afclwhripefpk3gmqnr9.streamlit.app)
- **[job-agent-v3](https://github.com/HyeonBin0118/job-agent-v3)** — v2 개선, 텍스트 전처리 강화 + 정량 평가 + 자소서 품질 자동 평가 + 다중 공고 비교 + 면접 준비 (가설 검증 포함)
  `GPT-4o-mini` `Streamlit` · [🚀 Demo](https://job-agent-v3-yzhg5h4dlyceriez67kudz.streamlit.app)

---

## 🛠️ LLM Applications
- **[mock-interview-ai](https://github.com/HyeonBin0118/mock-interview-ai)** — 음성 답변 기반 AI 모의 면접, FastAPI + PostgreSQL + Redis + Docker Compose
  `FastAPI` `PostgreSQL` `Redis` `Docker` `Whisper` `GPT-4o-mini` · [🎬 영상](https://youtu.be/cCh4mFKcWrI)
- **[ai-career-assistant](https://github.com/HyeonBin0118/ai-career-assistant)** — Job Agent + Mock Interview AI 통합, 자소서 생성 → 면접 연습 → 리포트 올인원 플랫폼
  `FastAPI` `PostgreSQL` `Redis` `Celery` `Docker` `Whisper` `GPT-4o-mini` · Redis 캐싱 25% · 비동기 처리 93% 단축
- **[ai-coding-test-assistant](https://github.com/HyeonBin0118/ai-coding-test-assistant)** — 코딩 테스트 풀이 중 문제를 자동 인식하고 힌트·접근법·정답을 제공하는 데스크톱 플로팅 어시스턴트
  `FastAPI` `PyQt6` `Playwright` `OpenAI` `pywinauto` `SSE`

---

## 👁️ Computer Vision
- **[yolov5-license-plate-recognition](https://github.com/HyeonBin0118/yolov5-license-plate-recognition)** — YOLOv5 기반 실시간 번호판 탐지 + PaddleOCR 한글 인식
  `YOLOv5` `PaddleOCR` `OpenCV` `PyTorch`

---

## 🛠️ Tech Stack
`Python` `PyTorch` `LangChain` `LangGraph` `ChromaDB` `OpenAI API` `Cohere` `FastAPI` `PostgreSQL` `Redis` `Docker` `Streamlit` `PyQt6` `Playwright` `pywinauto` `YOLOv5` `OpenCV` `Celery`
