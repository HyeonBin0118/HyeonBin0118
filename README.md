# Hi, I'm HyeonBin 👋

AI/백엔드 개발자를 목표로 프로젝트를 설계하고 있습니다.
기능 구현에 그치지 않고 가설을 세우고 데이터로 검증하는 방식으로 개발합니다.
RAG 성능 평가, 부하 테스트 기반 성능 개선, QLoRA 파인튜닝 실험 등 수치로 결과를 기록합니다.

---

## 🟡 AI Coding Test Assistant

코딩 테스트 풀이 중 위젯 형태로 화면에 플로팅 되어있다가 문제를 자동 인식하고 힌트·접근법·정답을 제공하는 데스크톱 어시스턴트. 유료 API 의존도를 낮추기 위해 직접 모델을 파인튜닝 시도.

- **[ai-coding-test-assistant](https://github.com/HyeonBin0118/ai-coding-test-assistant)** — 메인 어시스턴트
  `FastAPI` `PyQt6` `Playwright` `OpenAI` `pywinauto` `SSE` · [🎬 영상](https://youtu.be/qTPpKzS6hcg)
  - ↳ **[coder-llm-finetune](https://github.com/HyeonBin0118/coder-llm-finetune)** — GPT-4o-mini를 7B 오픈소스 모델로 대체하기 위한 QLoRA 파인튜닝 실험
    `Qwen2.5-Coder-7B` `QLoRA` `PEFT` `bitsandbytes` `Transformers` `sentence-transformers`
    · v1→v4 반복 실험으로 val loss 63% 감소 (0.552→0.203) · 파라미터 정확도 100% 달성
    · 논문(arXiv:2504.12687) 기반 Evol-Instruct 데이터 확장(681→3,848) + IFD+K-Means 40% 선별 적용
    · v5: 코드 완전 정답 0→3개, 파라미터 정확도 8/10→10/10 달성
    · DPO 학습 완료 (rewards/accuracies 92.5%) · SFT→DPO 파이프라인 직접 구축

---

## 🟠 AI Personal Assistant

자연어로 일상을 입력하면 일정·지출·투두로 분류해 계정별로 저장하는 개인 비서 SaaS 서버.
다중 사용자 동시 접속 환경에서 병목을 측정하고, 캐싱 전략 3단계와 RAG 파이프라인 최적화까지 구현했다.

- **[ai-personal-assistant](https://github.com/HyeonBin0118/ai-personal-assistant)**
  `FastAPI` `PostgreSQL` `pgvector` `Redis` `APScheduler` `Locust` `GPT-4o-mini` `Docker`
  · 실제 LLM 포함 50명 동시 부하 측정 → `/input` p50 1,500ms 병목 확인
  · 완전 일치 캐싱(Redis) 히트율 11.5% → Redis 전체 스캔 O(N) 문제 발견 → pgvector 인덱스 검색으로 교체
  · pgvector 임베딩 캐싱 히트율 18.2%, 응답시간 no_cache 수준으로 안정화
  · pgvector 기반 RAG 파이프라인 구축 — 자연어 질문으로 개인 데이터 질의응답
  · LLM 의도 분류 → 키워드 기반으로 교체로 에러율 22.9% → 1.9% 개선
  · JWT 인증 + 계정별 데이터 격리 + 백그라운드 스케줄러 기반 알림 + pytest 5개 통과

---

## 🟢 AI Career Assistant

자소서 생성 → 면접 연습 → 음성 대화형 면접 → 평가 리포트 올인원 플랫폼

- **[ai-career-assistant](https://github.com/HyeonBin0118/ai-career-assistant)** — 자소서 생성 → 면접 연습 → 음성 대화형 면접 → 평가 리포트 올인원 플랫폼
  `FastAPI` `PostgreSQL` `Redis` `Celery` `Docker` `Whisper` `Edge-TTS` `GPT-4o-mini`
  · Redis 캐싱 25% · 비동기 처리 93% 단축 · [🎬 영상](https://youtu.be/gNBGeOUz5qk)
  - ↳ **[mock-interview-ai](https://github.com/HyeonBin0118/mock-interview-ai)** — 음성 답변 기반 AI 모의 면접 파이프라인
    `FastAPI` `PostgreSQL` `Redis` `Docker` `Whisper` · [🎬 영상](https://youtu.be/cCh4mFKcWrI)
  - ↳ **[job-agent-v3](https://github.com/HyeonBin0118/job-agent-v3)** — 채용공고 분석 + 자소서 생성 + 가설 검증
    `GPT-4o-mini` `Streamlit` · [🚀 Demo](https://job-agent-v3-yzhg5h4dlyceriez67kudz.streamlit.app/)
    - ↳ **[job-agent-v2](https://github.com/HyeonBin0118/job-agent-v2)** — 사이드바 UX + 자소서 커스터마이징 + AI 상담
      `LangGraph` `Streamlit` · [🚀 Demo](https://job-agent-v2-24afclwhripefpk3gmqnr9.streamlit.app/)
      - ↳ **[job-agent](https://github.com/HyeonBin0118/job-agent)** — v1, LangGraph 기반 파이프라인 설계
        `LangGraph` `FastAPI` `Streamlit` · [🚀 Demo](https://job-agent-fiyd3jcmzx92at9t7p7zq2.streamlit.app/)


---

## 🔵 ShopAI

FAQ + 상품 + 리뷰 기반 RAG 챗봇, 이미지 검색, RAGAs 정량 평가까지 단계적으로 발전시킨 시리즈

- **[shopping-rag-final](https://github.com/HyeonBin0118/shopping-rag-final)** — 최종 완성판, 챗봇 + 이미지 검색 + RAGAs 대시보드 통합
  `GPT-4o Vision` `Cohere Rerank` `RAGAs` · [🚀 Demo](https://shopping-rag-final-2uvz8tccm5pucljl8spjrc.streamlit.app/) · [🎬 영상](https://youtu.be/AAxJZN74ZiU)
  - ↳ **[shopping-rag-v4](https://github.com/HyeonBin0118/shopping-rag-v4)** — RAGAs + Hit@K 평가 + 결과 시각화
    `RAGAs` `Matplotlib` · Faithfulness 0.85 / Hit@K 71.4%
    - ↳ **[shopping-rag-v3](https://github.com/HyeonBin0118/shopping-rag-v3)** — GPT-4o Vision 이미지 검색 + 카테고리 필터링
      `GPT-4o Vision` `Cohere Rerank` · [🚀 Demo](https://shopping-rag-v3-ndnwefdv24yp6vsfqxnmzq.streamlit.app/)
      - ↳ **[shopping-rag-v2](https://github.com/HyeonBin0118/shopping-rag-v2)** — 리뷰 한국어 번역 + Cohere Re-ranking + 배포
        `Cohere Rerank` · [🚀 Demo](https://shopping-rag-v2-db2ox3udz3gbsunb7m8jbq.streamlit.app/)
        - ↳ **[shopping-faq-rag](https://github.com/HyeonBin0118/shopping-faq-rag)** — v1, FAQ + 상품 + 리뷰 RAG 챗봇, Ollama vs OpenAI 비교
          `LangChain` `ChromaDB` `Streamlit`

---

## 🔴 Computer Vision

- **[yolov5-license-plate-recognition](https://github.com/HyeonBin0118/yolov5-license-plate-recognition)** — YOLOv5 기반 실시간 번호판 탐지 + PaddleOCR 한글 인식
  `YOLOv5` `PaddleOCR` `OpenCV` `PyTorch`

---

## 🟣 Desktop Utility

- **[BTBatteryWidget](https://github.com/HyeonBin0118/BTBatteryWidget)** — 페어링된 블루투스 장치의 배터리 잔량을 화면에 띄우는 윈도우용 플로팅 위젯
  `PyQt6` `SetupAPI` `ctypes` `winreg` `PyInstaller` `Inno Setup`
  · PowerShell(800ms) → SetupAPI ctypes 직접 호출(5ms)로 전환

---

## 🛠️ Tech Stack

<table>
  <tr>
    <td><b>Language</b></td>
    <td>Python</td>
  </tr>
  <tr>
    <td><b>AI/ML</b></td>
    <td>PyTorch · Transformers · PEFT · QLoRA · bitsandbytes · sentence-transformers · LangChain · LangGraph · ChromaDB · OpenAI API · Cohere · Whisper</td>
  </tr>
  <tr>
    <td><b>Backend</b></td>
    <td>FastAPI · SQLAlchemy · PostgreSQL · Redis · Celery · APScheduler</td>
  </tr>
  <tr>
    <td><b>Frontend</b></td>
    <td>Streamlit · PyQt6 · Vanilla JS</td>
  </tr>
  <tr>
    <td><b>Infra</b></td>
    <td>Docker · Docker Compose · GitHub Actions · PyInstaller</td>
  </tr>
  <tr>
    <td><b>Load Testing</b></td>
    <td>Locust</td>
  </tr>
  <tr>
    <td><b>CV</b></td>
    <td>YOLOv5 · OpenCV · PaddleOCR</td>
  </tr>
</table>
