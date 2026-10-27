# 타이타닉 생존 예측과 패턴인식 실습

타이타닉 승객의 특성을 탐색하고 여러 분류 모델로 생존 여부를 예측하는 노트북 프로젝트다. 데이터 전처리와 시각화, 모델 비교, 예측 결과 저장 과정을 한 노트북에서 확인할 수 있다.

## 주요 내용

- 승객 데이터 분포와 결측치 탐색
- 생존 여부와 입력 특성의 관계 시각화
- 분류 모델의 교차검증
- KNN, 결정트리, 랜덤 포레스트 등 분류 실험
- 제출 형식의 예측 CSV 생성

## 저장소 구성

| 파일 | 역할 |
|---|---|
| `Titanic_Survival_Prediction.ipynb` | 데이터 탐색·전처리·분류 및 결과 저장 |
| `패턴인식_연구제안_이경준.pdf` | 연구 제안 문서 |
| `패턴인식_연구제안_이경준.pptx` | 연구 제안 발표 자료 |

## 데이터 준비

노트북이 읽는 원본 CSV는 저장소에 포함되어 있지 않다. Kaggle의 Titanic 대회 데이터에서 다음 파일을 받아 저장소 루트의 `titanic` 폴더에 둔다.

```text
titanic/
  train.csv
  test.csv
  gender_submission.csv
```

`train.csv`의 `Survived`가 학습 목표이며, `gender_submission.csv`는 출력 형식을 맞추기 위해 사용한다. 데이터 제공 조건은 원본 배포처에서 확인한다.

## 실행 방법

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install notebook pandas numpy matplotlib seaborn scikit-learn missingno
.\.venv\Scripts\python.exe -m notebook Titanic_Survival_Prediction.ipynb
```

저장소 루트에서 실행하고 노트북 셀을 위에서부터 순서대로 실행한다. 폰트 설정은 실행 OS에 설치된 한글 폰트에 맞춘다. 위 패키지 목록은 노트북의 import를 기준으로 정리했으며 별도 고정 환경 파일은 없다.

## 결과 확인

탐색 그래프와 교차검증 결과를 노트북에서 확인하고 `submission_result.csv`를 생성한다. 노트북을 열어 저장된 출력물을 보는 것과 현재 환경에서 전체 셀을 재실행하는 것은 구분해야 한다. Kaggle 제출 점수나 새로운 실행의 정확도를 별도로 보장하지 않는다.

---

[GitHub 저장소](https://github.com/pranpreten/pattern-recognition) · [문서 작성 기준 코드](https://github.com/pranpreten/pattern-recognition/tree/1445fe0e8d9aea72088102038cb4c890bc6fec8b)
