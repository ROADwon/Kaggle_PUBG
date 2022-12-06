## Kaggle_PUBG


### 01. 나의 첫 모델 (RandomForestClassifier)
 * 내용 
   * 01. 데이터 불러오기, 데이터 전처리
      * feature label encoding : matchType (object)형식 -> (int)형식
      > 매치타입별 플레이 난이도가 승률에 지대한 영향이 있기때문에 테스트 데이터에 필요하다고 판단함.
   * 02. 최적 모델 적용하기
     > RandomForestClassifier,DecisionClassifier,KNeighborNearest
 * 코드 [Link](./20221206-baseline.ipynb)

### 02. 최적화된 모델 선정 및 학습 (LightGBM)
 * 내용 
   * 01. 데이터 불러오기, 데이터 전처리
      * feature label encoding : matchType (object)형식 -> (int)형식
      > 매치타입별 플레이 난이도가 승률에 지대한 영향이 있기때문에 테스트 데이터에 필요하다고 판단함.
      * 9개 피처 선정 이유 - 개인 판단으로 생존에 필요한 변수로 생각함. 
         * 'assists','kills','killPoints','DBNOs','killStreaks','boosts','revives','heals','matchType'
      
   * 02. 최적 모델 적용하기
     > lightGBM의 MAE값이 가장 좋았음.
 * 코드 [Link](./20221206-baseline.ipynb)
 
### 03. lightGBM 회귀모델 적용
 * 코드 [Link](./20221206-baseline.ipynb)
 
### 04. gridresearchCV, crossValdation
 * 코드 [Link](./20221206-baseline.ipynb)
