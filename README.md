# Connect AI Colab Runner

Connect AI 장기기억 학습용 **공개 실행기** 저장소입니다.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Willseungmin/connect-ai-colab-runner/blob/main/train-sft.ipynb)

## 역할

- 공개 GitHub에서 Colab 노트북을 안정적으로 엽니다.
- 실행 시 비공개 Hugging Face 데이터셋 `willseungmin/connect-ai-brain`을 로그인 후 읽습니다.
- 학습 결과를 Hugging Face 모델 `willseungmin/my-brain-v1`에 업로드합니다.
- 실제 뽀득·로칼 지식 원문, 고객 데이터, API 키, 토큰은 이 저장소에 저장하지 않습니다.

## 실행 방법

1. 위 **Open in Colab** 버튼을 누릅니다.
2. `런타임 → 런타임 유형 변경 → T4 GPU`를 선택합니다.
3. `런타임 → 모두 실행`을 누릅니다.
4. Hugging Face **Write 토큰**으로 로그인합니다.
5. 학습과 GGUF 업로드가 완료될 때까지 기다립니다.

## 데이터 흐름

```text
Connect AI
  → Private GitHub: connect-ai-knowledge-hub
  → Private Hugging Face Dataset: willseungmin/connect-ai-brain
  → Public Colab Runner: 이 저장소의 train-sft.ipynb
  → Private Hugging Face Model: willseungmin/my-brain-v1
```

## 보안

이 저장소는 공개이므로 다음 내용을 커밋하지 않습니다.

- `hf_` 또는 `github_pat_` 토큰
- 고객 이름·전화번호·주소
- 뽀득·로칼 원천 데이터
- Connect AI 지식 원문 또는 임베디드 base64 데이터
