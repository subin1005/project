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
  - 대회후기 : Public 점수가 후반에 2위까지 오르면서 수상을 기대했지만 그러지 못해서 아쉬움이 남았다. 하지만 VotingClassifier 모델 사용은 처음이었고, 가중치를 다르게 두면서 모델을 학습하는 과정이 흥미로웠고, 모델을 조정할 수록 점수가 올라 성취감을 느낄 수 있었던 공모전이었다. 9위로 대회를 마무리한 후, 하이퍼 파라미터 조정을 한 뒤 제출하니, Private 7위 점수까지 모델 성능이 향상되었다. 앞으로 하이퍼 파라미터 조정에 조금 더 신경써야 겠다는 생각이 들었다.

- 건설기계 오일 상태 분류 AI 경진대회
  - 대회링크 : https://dacon.io/competitions/official/236013/overview/description
  - 대회기간 : 2022년 11월 - 12월
  - 대회주제 : 건설장비에서 작동오일의 상태를 실시간으로 모니터링하기 위한 오일 상태 판단 모델 개발 (정상, 이상의 이진분류)
  - 대회결과 : **Public  83/619 (TOP 13.4%), Private 61/517 (TOP 11.8%)**
  - 활용모델 : XGBoost, LightGBM
  - 분석방법 : 학습데이터의 피쳐 개수가 테스트 데이터의 피쳐 개수보다 많아서 **지식증류**를 사용하였다. Teacher Moderl과 Student Model을 각각 XGBoost, LightGBM을 선택하여 학습했다.
  - 대회후기 : 신경망 모델을 사용하여 지식증류학습을 수행해봤다.
    


ETC
- 제 2회 세종 빅데이터 아이디어 공모전
  - 대회기간 : 2021년
  - 대회주제 :
  - 대회결과 : 장려상 수상
  - 활용모델 : 
  - 분석방법 : 군집분석
  - 대회후기 : 첫 공모전이라 미흡했던 부분이 많았다. 빅데이터 공모전이었으나, 충분한 크기의 데이터를 사용하지 못했고

-  
 
   
