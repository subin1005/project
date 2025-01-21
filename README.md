# project
프로젝트 코드 정리하는 곳

DACON
- 고객 대출등급 분류 AI 해커톤
  - 대회링크 : https://dacon.io/competitions/official/236214/overview/description
  - 대회기간 : 2024년 1월 - 2월
  - 대회주제 : 대출 고객과 관련된 데이터 분석을 통해 고객의 대출등급(A-G)을 예측하는 AI 모델 개발
  - 대회결과 : **Public 6/559 (TOP 1.07%), Private 9/519 (TOP 1.73%)**
  - 참여인원 : 1명
  - 활용모델 : Voting Classifier (RandomForest, GradientBoosting, DecisionTree)
  - 분석방법 : 변수선택과 파생변수 생성이 점수에 큰 영향을 미치는 것 같아, 여러 조합으로 변수를 선택해보고 다양한 파생변수를 생성하는 등의 전처리 수행. 모델링의 경우, 학습한 모델 중 가장 점수가 높았던 RandomForest, GradientBoosting, DecisionTree 모델을 사용하여 앙상블 모델 생성.
  - 대회후기 : 잘 만든 파생변수가 가장 중요한 변수 역할을 할 때 뿌듯했다. 대출등급에 영향을 미치는 요소가 뭘까 조사해보고 유의미할 것 같은 파생변수를 생성했다. 변수에 대한 충분한 이해와 고민이 중요하다는 것을 느꼈다.
  - > 시도정리 :
1. 전처리 거의 안 한 데이터로 모델 학습 => macro f1 : 0.78
2. 파생변수 생성 (대출금액_대비_총상환원금_비율, 대출금액_대비_총상환이자_비율, 그 외 여러 파생변수 생성 시도) => 0.91 (크게 오름)
3. 중요도 높았던 변수만 선택 (대출기간, 대출금액_대비_총상환원금_비율, 대출금액_대비_총상환이자_비율)=> 0.949
4. 성능이 가장 좋았던 세가지 모델을 (rf, dt, gbc) 모델별 가중치 다르게 설정하고 votingclassifier 모델 학습 => 0.9549
5. 최종 public macro f1 : 0.9549
그 외, 이상치제거, 정규화/표준화, 대출금액 변수 구간화, 오버샘플링, 여러가지 파생변수 생성 등을 시도했으나 점수에 큰 효과는 없었습니다.
    

- 건설기계 오일 상태 분류 AI 경진대회
  - 대회링크 : https://dacon.io/competitions/official/236013/overview/description
  - 대회기간 : 2022년 11월 - 12월
  - 대회주제 : 건설장비에서 작동오일의 상태를 실시간으로 모니터링하기 위한 오일 상태 판단 모델 개발 (정상, 이상의 이진분류)
  - 대회결과 : **Public  83/619 (TOP 13.4%), Private 61/517 (TOP 11.8%)**
  - 참여인원 : 2명
  - 활용모델 : XGBoost, RandomForest
  - 분석방법 : 학습데이터의 피쳐 개수가 테스트 데이터의 피쳐 개수보다 많아서 **지식증류**를 사용하였다. Teacher Moderl과 Student Model을 각각 XGBoost, RandomForest 모델을 선택하여 학습했다.
  - 2가지 버전 코드
      - Classifer_Regressor : 테스트 데이터셋에 없는 변수를 활용하여 분류모델을 학습하고, 그 학습 결과(predict_proba)를 테스트 데이터셋의 변수를 활용하여 회귀모델로 예측하는 방법
      - tensorflow : 신경망 모델을 사용하여 지식증류를 수행함.  대회가 끝난 뒤 신경망 모델에 대해 공부하고 시도해본 코드
  - 대회후기 : 데이콘에서 공유한 베이스라인은 신경망 모델을 활용한 분석이었다. 당시에 tensorflow에 대해 무지한 상태라 이해가 어려웠다. 그래서 지식 증류에 대한 개념을 공부하고 직관적으로 분류모델과 회귀모델을 만들어서 지식 증류를 수행했다.    


ETC
- 제 2회 세종 빅데이터 아이디어 공모전
  - 대회기간 : 2021년 8월 - 11월
  - 대회주제 : 데이터(공공, 민간 불문)를 활용하여 도시문제 해결, 기존 정책 또는 스마트 서비스를 발굴할 수 있는 아이디어 제안
  - 선정주제 : 세종시 문화시설을 고려한 버스 정류장 추가 설치 지역 선정
    (세종시에 거주하던 친구와 함께 참가한 공모전이며 그 친구에게 실제 거주하며 느낀 불편함을 물었을 때 '인프라의 부족'이라는 대답을 들었다. 인프라를 구축하기 위해서 선행되어야 할 것이 교통이라고 생각하여 교통이 좋지 않은 읍면동에 버스정류장 설치를 제안했다.)
  - 대회결과 : **장려상** 수상
  - 참여인원 : 2명
  - 분석방법 : 계층적 군집분석
  - 대회후기 : 첫 공모전이라 미흡했던 부분이 많았다. 빅데이터 공모전이었으나, 충분한 크기의 데이터를 사용하지 못했던 점이 아쉬웠다. 


- 공공데이터_활용_공모전(2023)
  - 대회기간 : 2023년 6월 - 7월
  - 대회주제 : 5분 단위의 전력량 데이터를 포함한 공공데이터를 이용하여 6시간 뒤의 전력량을 예측하는 모델을 만들고, 그 모델을 활용하는 방안 제시.
  - 대회결과 : 수상 X
  - 참여인원 : 2명
  - 활용모델 : LightGBM
  - 분석방법 : 현재 전력수요량을 포함한 12개의 변수를 독립변수, 향후 6시간까지의  5분 단위 전력수요량(총 72개 전력수요량)을 종속변수로 두고 분석을 수행하였다. LightGBM 모델은 1시점(5분) 뒤의 전력수요량만을 예측하기 때문에 총 72개의 모델을 활용하여 5분 뒤부터  6시간 뒤의 전력량까지 예측하였다.
   - 제시한 활용방안 : 전력량이 문제가 발생될 것으로 예상될 때, 알림을 보내주는 어플 제안.
   - 대회후기 : 많은 양의 데이터를 가지고 진행했던 분석으로, 효율적인 코드에 대한 중요성을 깨달았다. 데이터의 크기가 커서 단순 작업도 시간이 오래 걸렸다. 이에 최대한 시간이 적게 걸리는 코드를 짜기 위해 고민하며 수정했던 기억이 있다. 그 과정에서 코드를 더 깔끔하게 정리하는 방법에 대해 배웠다.
 
 
     
