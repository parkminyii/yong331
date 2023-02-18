# SK Shieldus Rookies 모듈 프로젝트 2  
### [4조] 현동엽, 박민이, 박수빈, 이용희

### 목적
- Kaggle의 Playground 대회 참가를 통해 수업시간에 배웠던 머신러닝 분류, 회귀 문제 복습 및 실력을 향상시킬 수 있다.
- 데이터 전처리, 인코딩을 통해 머신러닝의 목적에 맞게 처리하고 EDA 분석을 통해 데이터를 다양한 각도에서 관찰하고 깊게 이해할 수 있다.

### 기대효과 
- 대회를 진행하면서, 데이터 정제 및 관리, 협업 관리, 프로젝트 실전 테크닉을 얻을 수 있다.
- 다양한 머신러닝 모델을 사용해봄으로써 정확도와 예측율을 상승시킬 수 있다.

## Playground Series - Season 3, Episode 2
### Outline

- 출처
  - 원본 데이터 셋
    - [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
  - 경진 대회 데이터 셋
    - [Stroke Prediction](https://www.kaggle.com/competitions/playground-series-s3e6/overview)
- 개요
  - 세계보건기구(WHO)에 따르면 뇌졸중은 전체 사망자의 약 11%를 차지하는 세계 2위의 사망 원인
  - 이 데이터 세트는 성별, 나이, 다양한 질병 및 흡연 상태와 같은 입력 매개 변수를 기반으로 환자가 뇌졸중에 걸릴 가능성이 있는지 예측
  - 각 행은 환자에 대한 관련 정보를 제공
- 평가지표 : ROC Curve
- 타임라인 : 2023.1.10 ~ 2023.1.16
  
### 각 열에 대한 정보 확인

|컬럼명|내용|해석|
|------|---|---|
|id|고유 id|인덱스와 같은 의미(제거 가능)
|gender|성별|범주형(명목형) : Male, Female, other
|age|나이|수치형
|hypertension|고혈압 유무|이진형 : 0,1
|heart_disease|심장질환 유무|이진형 : 0,1
|ever_married|결혼 유무|이진형 : Y, N
|work_type|업무형태|범주형(명목형) : Private, children, Govt_job, Self-employed, Never_worked
|Residence_type|거주지 유형|이진형 : Urban, Rural
|avg_glucose_level|평균 당 수치|수치형(연속형) 
|bmi|비만도|수치형(연속형)
|smoking_status|흡연상태|범주형(명목형) : never smoked, formerly smoked, Unknown, smokes
|stroke|뇌졸중 유무|정답(target) : 0, 1 

### 참고 문헌
- [sklearn.ensemble.GradientBoostingClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html)
- [Using Optuna to Optimize XGBoost Hyperparameters](https://medium.com/optuna/using-optuna-to-optimize-xgboost-hyperparameters-63bfcdfd3407)
- [AutoML? 야 너도 만들 수 있..을걸?](https://velog.io/@lazy_learner/AutoML-%EC%95%BC-%EB%84%88%EB%8F%84-%EB%A7%8C%EB%93%A4-%EC%88%98-%EC%9E%88%EC%96%B4#hyperparameters-optimization)
- [BMI Prime Calculator](https://captaincalculator.com/health/weight/bmi-prime-calculator/)
- [5th Place Solution](https://www.kaggle.com/competitions/playground-series-s3e2/discussion/378780)


## Playground Series - Season 3, Episode 6
### Outline

- 출처
  - 원본 데이터 셋
    - [Paris Housing Price Prediction](https://www.kaggle.com/datasets/mssmartypants/paris-housing-price-prediction)
  - 경진 대회 데이터 셋
    - [Paris Housing Price](https://www.kaggle.com/competitions/playground-series-s3e6/overview) 
- 내용 : 교육 목적, 실습 및 필요한 지식 습득을 위한 파리의 가상 집값 데이터에서 생성된 데이터 셋
- 평가지표 : RMSE 
- 타임라인 : 2023.2.7 ~ 2023.2.20

### 각 열에 대한 정보 확인

|컬럼명|내용|해석|
|------|---|---|
|id|고유 id|인덱스와 같은 의미(제거 가능)
|squareMeters|방 면적 넓이|수치형(연속형)
|numberOfRooms|방 개수|수치형(이산형)
|hasYard|마당 존재 여부| 이진형 : 0,1
|hasPool|수영장 존재 여부|이진형 : 0,1
|floors|층 수|수치형(이산형)
|cityCode|건물 구별 고유 코드 (우편번호)|범주형
|cityPartRange|지역구|범주형 : 1 ~ 10 
|numPrevOwners|이전 집 소유자 거친 횟수(매매 횟수)|수치형(이산형)
|made|제작연도|범주형
|isNewBuilt|리빌딩(신축 건물) 여부|이진형 : 0,1 
|hasStormProtector|태풍 보호기 설치 여부|이진형 : 0,1
|basement|지하실 면적넓이|수치형(연속형)
|attic|다락방 면적넓이|수치형(연속형)
|garage|주차장 면적넓이|수치형(연속형)
|hasStorageRoom|창고 여부|이진형 : 0,1
|hasGuestRoom|게스트 룸 개수|수치형(이산형)
|price|가격|종속변수(Target), 시세 예측값

### 참고 문헌
- [캘리포니아 집값 예측](https://didalsgur.tistory.com/entry/%EC%BA%98%EB%A6%AC%ED%8F%AC%EB%8B%88%EC%95%84-%EC%A3%BC%ED%83%9D-%EA%B0%80%EA%B2%A9-%EC%98%88%EC%B8%A1-Dataset-California-Housing-Prices-Kaggle)
- [핸드온 머신러닝](https://data-analysis-expertise.tistory.com/112)
- [Boston 예측](https://velog.io/@wltn39/보스턴-주택가격-예측)
- [AUTOKHAJI- 집값 예측 Stage1 : 데이터 전처리](https://dacon.io/codeshare/7477?dtype=recent)
- [일반화선형회귀 : boston housing 집값 예측하기](http://docs.iris.tools/manual/IRIS-Usecase/ml/ML_boston_housing.html)
- [LightGBM + Optuna로 top 10안에 들어봅시다.](https://dacon.io/en/codeshare/2876)
- [Private_3위 Xgboost + Optuna](https://dacon.io/en/competitions/official/235986/codeshare/6991)
- [XGBoost Parameters 공식문서](https://xgboost.readthedocs.io/en/stable/parameter.html)
- [XGBoost 개념 이해](https://wooono.tistory.com/97)
- [XGBoost 주요 파라미터](https://zzinnam.tistory.com/entry/XGboost-%EC%A3%BC%EC%9A%94-%ED%95%98%EC%9D%B4%ED%8D%BC%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0-with-%ED%8C%8C%EC%9D%B4%EC%8D%AC)
- [XGBoost와 LightGBM 하이퍼파라미터 튜닝 가이드](https://psystat.tistory.com/131)
- [cityCode is Fake!](https://www.kaggle.com/competitions/playground-series-s3e6/discussion/384676)
- [런던·파리·뉴욕… 세계도 건물 높이 규제](https://www.seouland.com/arti/society/society_general/1609.html)
- [면적순 나라 목록](https://ko.wikipedia.org/wiki/%EB%A9%B4%EC%A0%81%EC%88%9C_%EB%82%98%EB%9D%BC_%EB%AA%A9%EB%A1%9D)
- [IQR을 이용하여 이상치를 탐색하고 처리하기](https://hong-yp-ml-records.tistory.com/15)
- [기초 통계 이해](https://m.blog.naver.com/dairum_enc/221409597367)
- [범주형,수치형,이상형,연속형,명목형,순서형 정리 - Unique Life](https://horae.tistory.com/entry/%EB%B2%94%EC%A3%BC%ED%98%95%EC%88%98%EC%B9%98%ED%98%95%EC%9D%B4%EC%83%81%ED%98%95%EC%97%B0%EC%86%8D%ED%98%95%EB%AA%85%EB%AA%A9%ED%98%95%EC%88%9C%EC%84%9C%ED%98%95-%EC%A0%95%EB%A6%AC)
