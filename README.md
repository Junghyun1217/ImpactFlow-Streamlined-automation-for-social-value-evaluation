📊 Impact-Insight-AI: Social Value & ESG Report Automation
본 프로젝트는 기업의 비즈니스 문서를 분석하여 사회적 가치(Social Value)를 요약하고, SDGs(지속가능발전목표) 및 GRI(Global Reporting Initiative) 가이드라인에 맞춘 리포트를 자동 생성하는 파이프라인입니다.

단순한 텍스트 분석을 넘어, AI 에이전트가 사실 여부를 검증하고 **데이터 시각화(Chart Generation)**까지 수행하는 통합 솔루션을 지향합니다.

✨ 주요 기능 (Key Features)
다양한 문서 파싱 (Multi-format Parsing): LlamaParse를 활용하여 PDF, PPTX, DOCX 뿐만 아니라 HWP/HWPX 문서의 텍스트를 정밀하게 추출합니다.

SDGs & GRI 자동 매칭 (Intelligent Mapping): * 기업 요약문을 기반으로 관련 SDGs 대제목과 세부 목표(Sub-goals)를 자동 판별합니다.

RAG (Retrieval-Augmented Generation): FAISS 벡터 스토어를 활용해 기업 활동과 가장 밀접한 GRI 표준 항목을 검색 및 매칭합니다.

AI 에이전트 기반 검증 (Verification Agent): LangGraph 기반 에이전트가 ESG 성과 문단의 사실 여부를 검토하고, 대중이 이해하기 쉬운 **직관적인 비유(AI 해설)**를 추가합니다.

데이터 시각화 (Automated Charting): 텍스트 내 정량 데이터를 추출하여 시계열 변화(절대/상대/점진적 목표)를 보여주는 막대 그래프를 자동 생성합니다.

병렬 처리 (Parallel Processing): ThreadPoolExecutor를 적용하여 대량의 데이터 처리 및 분석 속도를 최적화했습니다.

🛠 기술 스택 (Tech Stack)
Language: Python

LLM Framework: LangChain, LangGraph, LlamaIndex

Model: OpenAI GPT-4o-mini

Vector DB: FAISS

Parsing: LlamaParse

Visualization: Matplotlib, Seaborn

📂 프로젝트 구조 (Structure)
Section A: SDGs 분석 및 사회적 가치 보고서(WHAT, WHO, HOW MUCH, RISK) 생성 로직

Section B: GRI 표준 정의 기반의 상위/세부 항목 RAG 매칭 시스템

Section C: 성과 지표(KPI) 추출 및 맞춤형 그래프 시각화 엔진

🚀 실행 방법
.env 파일에 OPENAI_API_KEY와 LLAMA_CLOUD_API_KEY를 설정합니다.

docs/ 디렉토리에 분석할 기업 문서를 넣습니다.

main_v4_graph.py를 실행하면 result/ 폴더에 최종 JSON 보고서와 그래프 이미지가 생성됩니다.
