## 뉴스 토픽 분류

- 뉴스 헤드라인을 보고 해당 뉴스의 토픽을 분류하는 알고리즘 개발 후 웹으로 서비스
- 맡은 역할
  - 데이터 전처리 
  - KLUE-RoBERTa-large, yobi/klue-roberta-base-ynat 모델 학습
  - 모델 성능 결과 분석
  - ppt 제작 및 프로젝트 발표



## 과정

1. 데이터 :
   - 뉴스 헤드라인과 토픽(정치, 경제, 사회 등 총 7개)으로 구성
   - KLUE topic classification의 약 45000개 + 네이버 뉴스에서 직접 크롤링한 데이터 약 95000개
     총 140773개의 데이터
2. 전처리
   - 중복 제거
   - 자주 등장하는 한자 및 영문자
   - 특수문자, 숫자 및 기호는 공백(" ")문자로 대체
   - 다운샘플링으로 토픽 분포 균일화
3. 모델 훈련

     - Huggingface를 이용해 여러 BERT 사전학습 모델들을 파인튜닝 한 뒤 가장 좋았던 모델로 분류기 구현

     - 전처리가 유효했는지 데이터 전처리 유무를 전 후 데이터로 각각 훈련시켜서 정확도 비교

     - KLUE-BERT-base
       KLUE-RoBERTa-base
       SKT/KoGPT2
       XLM-RoBERTa-large
       yobi/klue-roberta-base-ynat
       BERT 앙상블

4. 모델 성능 분석





