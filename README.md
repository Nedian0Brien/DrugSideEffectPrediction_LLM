<div align="center">

# DrugSideEffectPrediction_LLM

**약물·부작용 임베딩 유사도로 실제 사례를 검증하는 연구 노트북 저장소**

![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Embeddings](https://img.shields.io/badge/Embeddings-0EA5E9?style=flat-square) ![Research](https://img.shields.io/badge/Research-111827?style=flat-square)

[English](./README.en.md)

</div>

---

## 소개

이 저장소는 약물과 부작용 표현을 임베딩 벡터로 다루고, 코사인 유사도와 실제 사례 검증을 통해 약물-부작용 관계를 탐색한 연구 노트북 모음입니다.

현재는 패키지형 프로젝트가 아니라 Jupyter Notebook 중심의 실험 기록입니다. 재현 시에는 노트북 실행 환경과 데이터 파일 경로를 먼저 확인해야 합니다.

핵심 흐름은 먼저 약물명과 부작용 텍스트를 벡터 공간에 올리고, 유사도 기준으로 후보 관계를 뽑은 뒤, 실제 사례 확인 노트북에서 결과를 다시 점검하는 방식입니다. 모델 학습 파이프라인을 완성해 둔 저장소라기보다는, 탐색 과정과 중간 결과를 notebook 단위로 남긴 연구 기록에 가깝습니다.

## 주요 기능

| 기능 | 설명 |
|---|---|
| 모델 결과 도출 | `모델 결과 도출.ipynb`에서 코사인 유사도 기반 결과를 계산합니다. |
| 실제 사례 검증 | `실제사례검증.ipynb`에서 유사도 조회와 사례 확인 흐름을 다룹니다. |
| 임베딩 시각화 | `임베딩벡터시각화.ipynb`에서 벡터 비교와 시각화 실험을 다룹니다. |
| 연구 재점검 출발점 | 각 notebook의 셀과 출력값을 따라가며 데이터 경로, 모델, 유사도 계산 기준을 다시 확인할 수 있습니다. |

## 저장소 구조

| 경로 | 역할 |
|---|---|
| 모델 결과 도출.ipynb | Cosine similarity result generation |
| 실제사례검증.ipynb | Similarity lookup and case validation |
| 임베딩벡터시각화.ipynb | Embedding vector comparison and visualization |

## 읽는 순서

1. `모델 결과 도출.ipynb`에서 어떤 임베딩 결과를 만들었는지 확인합니다.
2. `실제사례검증.ipynb`에서 유사도 결과가 실제 사례 검토로 어떻게 이어지는지 봅니다.
3. `임베딩벡터시각화.ipynb`에서 벡터 간 거리와 분포를 시각적으로 점검합니다.

노트북을 실행하기 전에는 원본 데이터 위치와 설치된 라이브러리 버전을 먼저 맞추는 것이 좋습니다. 오래된 로컬 경로가 남아 있다면 셀을 바로 실행하기보다 입력 파일 경로를 현재 환경에 맞게 조정하세요.

## 빠른 시작

### Jupyter 실행

```bash
jupyter lab
```

### 노트북 목록 확인

```bash
find . -maxdepth 2 -name "*.ipynb"
```

### 권장 실행 순서

모델 결과 도출.ipynb -> 실제사례검증.ipynb -> 임베딩벡터시각화.ipynb

## 검증

| 항목 | 명령 |
|---|---|
| Notebook presence | `find . -name "*.ipynb" | wc -l` |

## 운영 메모

- 대용량 데이터나 개인 경로가 notebook 안에 남아 있을 수 있으므로, 실행 전 경로를 점검합니다.
- 연구 결과를 재사용하려면 입력 데이터, 모델, embedding 생성 방법을 별도 문서로 고정하는 것이 좋습니다.
- 후속 연구로 이어가려면 데이터 출처, 전처리 기준, 임베딩 모델 이름, cosine similarity threshold를 README나 별도 실험 로그에 함께 남기는 편이 좋습니다.

## 문서 작성 근거

이 README는 저장소 안의 다음 파일과 문서를 기준으로 작성했습니다.

- `모델 결과 도출.ipynb`
- `실제사례검증.ipynb`
- `임베딩벡터시각화.ipynb`
