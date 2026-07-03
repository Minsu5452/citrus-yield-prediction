# 감귤 착과량 예측 경진대회

[![Python](https://img.shields.io/badge/python-3.10-3776AB?logo=python&logoColor=white)](https://www.python.org) [![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

제주 감귤나무의 생육 데이터로 착과량을 예측했습니다. 48시간짜리 짧은 대회 안에서 피처 구성, 모델 비교, multi K-fold 앙상블을 빠르게 돌려 상위 6.6%를 기록했습니다.

## 개요

| 항목 | 내용 |
| --- | --- |
| 대회 | 감귤 착과량 예측 AI 경진대회 |
| 기간 | 2022.12.12 – 2022.12.14 |
| 주최 / 주관 | 제주테크노파크 / 데이콘 |
| 평가지표 | NMAE |
| 결과 | 상위 6.6% |
| 과제 | 감귤나무 생육 데이터 기반 착과량 회귀 |

## 접근

- 생육 정보에서 착과량 예측에 쓸 파생 변수를 만들었습니다.
- 피처 스케일링과 선택 실험을 분리해 입력 피처의 품질을 비교했습니다.
- XGBoost, LightGBM, CatBoost 회귀 모델을 학습했습니다.
- seed와 fold를 달리한 multi K-fold 앙상블로 예측을 안정시켰습니다.

## 저장소 구성

```text
.
├── notebooks/
│   ├── 01_feature_engineering.ipynb
│   ├── 02_feature_scaling.ipynb
│   ├── 03_feature_selection.ipynb
│   ├── 04_multi_kfold_experiment.ipynb
│   └── 05_final_ensemble_solution.ipynb
├── reports/
│   └── citrus_yield_prediction_solution.pdf
└── requirements.txt
```

## 발표 자료

- 최종 솔루션 발표자료: [`reports/citrus_yield_prediction_solution.pdf`](reports/citrus_yield_prediction_solution.pdf)

## 공개 범위

대회 원본 데이터와 제출 파일은 포함하지 않았습니다. 데이터는 대회 참가자에게만 제공되어 그대로 재현하기는 어렵고, 저장소에는 접근 방식을 담은 노트북과 발표자료만 남겼습니다.

## 링크

- [대회 페이지](https://dacon.io/competitions/official/236038/overview/description)
- [최종 리더보드](https://dacon.io/competitions/official/236038/leaderboard)
- [코드 공유](https://dacon.io/competitions/official/236038/codeshare/7302)

## 라이선스

Apache License 2.0. 자세한 내용은 [LICENSE](LICENSE)에 있습니다.
