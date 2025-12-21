# langchain_basic_class_7th

# 가상환경 만들고, 활성화
```
- 가상환경 만들기
conda crate -n lc_env Python = 3.12

- 가상환경 활성화
conda activate lc_env

pip install ipykernel
python -m ipykernel install --user --name lc_env
```

# 설치 라이브러리
```
pip install -Uq python-dotenv
pip install -Uq langchain

# langchain for opeain 
pip install -Uq langchain-openai 

# langchain of google genai
pip install langchain-google-genai

# 마크다운 출력
pip install rich
```
# API 키 발급
- openai api key  https://platform.openai.com/
- gemini api key  https://aistudio.google.com/api-keys


# LangSmith로 llm 사용 모니터링하기
## .env에 다음 설정값 정의
### openai gpt 모델인 경우
```
OPENAI_API_KEY=your-openai-api-key                  # 본인의 openai key 넣기
LANGCHAIN_TRACING_V2=true
LANGCHAIN_API_KEY=lsv2_pt_your-langsmith-api-key    # 본인 langsmith key 넣기
LANGCHAIN_PROJECT=gpt-travel-planner                # 프로젝트 이름 (원하는 대로)
```
### google gemini 모델인 경우
```
GOOGLE_API_KEY=your-google-api-key        # 본인의 google studio 넣기
LANGCHAIN_TRACING_V2=true
LANGCHAIN_API_KEY=your-langsmith-api-key  # 본인의 langsmith key 넣기
LANGCHAIN_PROJECT=gemini-travel-planner   # 프로젝트 이름 (원하는 대로)
```
## LLM 수행하는 코드 위쪽에 추가할 코드
```
import os
from dotenv import load_dotenv

# 환경변수 로드
load_dotenv(override=True)
```
