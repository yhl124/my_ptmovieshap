## transformer에서 제공하는 trainer로 fine tuning해보기

### 방법

- huggingface에 있는 모델에 네이버 영화 리뷰 데이터를 fine tuning해본다.  
영화 리뷰 데이터셋(https://github.com/e9t/nsmc)  
- transformers 라이브러리에서 사용 가능한 AutoTokenizer, AutoModelForSequenceClassification, Trainer등을 사용한다.
- 3 epochs 학습한다.

### 결과

||3.bert-base-uncased(전처리 다름)|4.klue/bert-base|5.bert-base-multilingual-cased|
|----|-------------|-------------|-------------|
|acc|0.514|0.887|0.514|
|f1|0.679|0.891|0.679|
|학습 시간|1:38:42|1:01:04|1:14:08|

### 결론?

- 한국어 모델 여부의 차이가 크다.
- 3번과 5번이 모델이 다르고 전처리도 달랐는데 정확도와 f1 score가 똑같이 나온 게 뭔가 방법이 잘못된 건가 싶기도 하다.