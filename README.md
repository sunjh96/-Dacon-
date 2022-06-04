# 와인 품질 분류
## 연구 목적
와인에 들어있는 각종 화학성분들의 데이터를 사용하여 와인의 품질을 분류하거나 예측하는 모델을 생성하는 것을 목표로 한다.
## 데이터 수집
국내 데이터 경쟁 플랫폼인 데이콘(Dacon)에서 진행하는 ‘와인 품질 분류’ 대회에서 제공하는 데이터셋을 이용하였다.
## 데이터 소개
Index - 구분자 (Key)  
Quality - 품질 (Target)  
Fixed acidity - 산도  
Volatile acidity - 휘발성산  
Citric acid - 시트르산  
Chlorides - 염화물  
Free sulfur dioxide - 독립 이산화황  
Total sulfur dioxide - 총 이산화황  
Density - 밀도  
pH - 수소 이온 농도  
Sulphrates - 황산염  
Alcohol - 도수  
Type - 종류  
Residual sugar - 잔당  


총 데이터 : Train data(5497), Test data(1000)
## 데이터 전처리
1 - 결측치 확인 및 이상치 제거  
2 - 범주형 데이터 처리  
3 - MinMax 정규화
## 분석 모형
### Random Forest
Parameters : N_estimaors(500), Max_features(Auto), Max_depth(20)
Accuray : 65.82%
### Support Vector Machine
Parameters : C(10), Gamma(100)
Accuray : 62.97%
## 결론
모델 성능 평가에 있어서 다양한 척도가 있지만 이 연구에서는 가장 간단하고 이해하기 쉬운 Accuracy를 사용한다. 다양한 모델로 분석해 본 결과 Classification Model : Random Forest Accuracy – 65%, Support Vector Machine Accuracy – 63%으로 나타났다. 가장 성능이 좋았던 Random Forest에서의 각 Feature 별 중요도를 나타내본 결과 Alcohol 함량이 품질을 결정하는 데 있어 가장 높은 중요도를 가졌고 와인의 종류인 Red Wine, White Wine은 중요도가 가장 낮게 나타났다. 모델 성능이 그렇게 높게 나타나진 않았지만 예측한 값들과 실제 Test 데이터의 값들을 비교해 본 결과 정확히 맞아떨어지진 않지만 값들의 차이가 그렇게 크게 나타나진 않았다. 

### Dacon 대회 주소
https://dacon.io/competitions/official/235610/data
