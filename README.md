# Trade Comovement 기반 수출입 예측 파이프라인

무역 품목 간 공행성(comovement)을 이용해 후행 품목의 다음 달 무역량을 예측하는 **파이프라인** 

1. Stage 1: `Corr + Lag + DTW + 품질 점수` 기반 comovement pair 탐색 및 필터링
2. Stage 2: 선택된 pair를 기반으로 한 시계열 피처 엔지니어링 및 회귀 모델 학습
3. Stage 3: LGBM + XGBoost 앙상블을 통한 다음 달 `value` 예측 및 제출 파일 생성

