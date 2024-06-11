# project
공모전 코드 정리하는 곳

DACON
- 고객 대출등급 분류 AI 해커톤
  - 대회기간 : 2024년 1월
  - 대회주제 : 대출 고객과 관련된 데이터 분석을 통해 고객의 대출등급 예측하는 AI 모델 개발
  - 대회결과 : Public 6/559 (TOP 1.07%) , Private 9/519 (TOP 1.73%)
  - 활용모델 : Voting Classifier (RandomForest, GradientBoosting, DecisionTree)
  - 분석방법 : 변수선택이나 파생변수 생성이 점수에 큰 영향을 미치는 것 같아, 여러 조합으로 변수를 선택해보고 다양한 파생변수를 생성하는 등의 전처리를 신경써서 했다. 모델링의 경우, 분류모델 중 가장 점수가 높았던 RandomForest, GradientBoosting, DecisionTree 모델을 사용하여 앙상블 모델을 생성했다.
  - 대회후기 : Public 점수가 후반에 2위까지 오르면서 수상을 기대했지만 그러지 못해서 아쉬움이 남았다. 하지만 VotingClassifier 모델 사용은 처음이었고, 가중치를 다르게 두면서 모델을 학습하는 과정이 흥미로웠고, 재밌었던 공모전이었다. 코드를 정리하면서 하이퍼 파라미터에 집중했더니 Private 7위 점수까지 모델 성능이 향상되었다. 앞으로 하이퍼 파라미터 조정에 조금 더 신경써야 겠다는 생각이 들었다.
  
ETC
- 제 2회 세종 빅데이터 아이디어 공모전
