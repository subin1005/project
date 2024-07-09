# project
프로젝트 코드 정리하는 곳

DACON
- 고객 대출등급 분류 AI 해커톤
  - 대회링크 : https://dacon.io/competitions/official/236214/overview/description
  - 대회기간 : 2024년 1월
  - 대회주제 : 대출 고객과 관련된 데이터 분석을 통해 고객의 대출등급(A-G)을 예측하는 AI 모델 개발
  - 대회결과 : **Public 6/559 (TOP 1.07%), Private 9/519 (TOP 1.73%)**
  - 활용모델 : Voting Classifier (RandomForest, GradientBoosting, DecisionTree)
  - 분석방법 : 변수선택과 파생변수 생성이 점수에 큰 영향을 미치는 것 같아, 여러 조합으로 변수를 선택해보고 다양한 파생변수를 생성하는 등의 전처리 수행. 모델링의 경우, 학습한 모델 중 가장 점수가 높았던 RandomForest, GradientBoosting, DecisionTree 모델을 사용하여 앙상블 모델 생성.

- 건설기계 오일 상태 분류 AI 경진대회
  - 대회링크 : https://dacon.io/competitions/official/236013/overview/description
  - 대회기간 : 2022년 11월 - 12월
  - 대회주제 : 건설장비에서 작동오일의 상태를 실시간으로 모니터링하기 위한 오일 상태 판단 모델 개발 (정상, 이상의 이진분류)
  - 대회결과 : **Public  83/619 (TOP 13.4%), Private 61/517 (TOP 11.8%)**
  - 활용모델 : XGBoost, RandomForest
  - 분석방법 : 학습데이터의 피쳐 개수가 테스트 데이터의 피쳐 개수보다 많아서 **지식증류**를 사용하였다. Teacher Moderl과 Student Model을 각각 XGBoost, RandomForest 모델을 선택하여 학습했다.
  - 2가지 버전 코드
      - Classifer_Regressor : 테스트 데이터셋에 없는 변수를 활용하여 분류모델을 학습하고, 그 학습 결과(predict_proba)를 테스트 데이터셋의 변수를 활용하여 회귀모델로 예측하는 방법
      - tensorflow : 신경망 모델을 사용하여 지식증류를 수행함. 대회 당시에 신경망 모델에 대한 이해가 부족하여 위의 방법으로 결과를 제출하였고, 대회가 끝난 뒤 신경망 모델에 대해 공부하고 시도해본 코드
    


ETC
- 제 2회 세종 빅데이터 아이디어 공모전
  - 대회기간 : 2021년
  - 대회주제 :
  - 대회결과 : 장려상 수상
  - 분석방법 : 군집분석
  - 대회후기 : 첫 공모전이라 미흡했던 부분이 많았다. 빅데이터 공모전이었으나, 충분한 크기의 데이터를 사용하지 못함. 
   
