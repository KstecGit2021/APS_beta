# APS_beta
 


## 목적
강화 학습을 이용하여, 납기일 준수 및 셋업최소화를 위한 공정 스케줄링 최적화

## reference
 - 논문 : <https://scienceon.kisti.re.kr/srch/selectPORSrchArticle.do?cn=JAKO201925462479137&dbt=NART>
 - 자료 : <https://hwk0702.github.io/projects/2019/11/08/Scheduler/>

## Create dataset for training
  1. dataset/data_create.ipynb open
  2. Hyper parameter setting(number of job types, number of orders, min process_time, max process_time, max due_date)
  3. Implementing data_create.ipynb



## Training
 - environment_v1.ipynb, environment_v2.ipynb 두개의 파일에서 서로다른 방식의 학습을 수행
 - DQN model의 경우 environment_v1.ipynb, environment_v2.ipynb 두 파일 모두 동일
 - 학습 데이터 전처리, DQN class, DQN 학습 및 모델 저장, 학습과정 시각화(train loss) 로 코드진행

### environment_v1.ipynb
 - point 1) 다수의 데이터셋 활용해서 모델학습
 - point 2) machine state 전체를 binary 값으로 설정
 - Train loss
 ![image](https://user-images.githubusercontent.com/78070883/112932087-483c6800-9158-11eb-8fc4-a7fdae107daf.png)

### environment_v2.ipynb
 - point 1) 단일 데이터셋의 반복적 모델학습
 - point 2) machine state를 binary or int 값으로 설정
 - Train loss
 ![image](https://user-images.githubusercontent.com/78070883/112933744-66579780-915b-11eb-884a-3fda1051ee35.png)





## Model test
 - model.h5 : 이전의 학습을 통해서 생성된 모델 저장파일
 - model_test.ipynb : 이전의 학습된 모델을 불러와서, 해당 모델을 기반으로 test 데이터셋에 대해서 최적배치 예측
 

## 기타 자세한 사항들
 - APS_Beta_Report(03-05).pptx 첨부
  
  
KSETEC 홈페이지: <http://kstec.co.kr/>   
   
 
      
Author: KSTEC 연구원 박재완, 조현우     
Last edited: 30-03-2021
