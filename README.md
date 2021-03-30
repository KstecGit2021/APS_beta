# APS_beta
 


## 목적
강화 학습을 이용하여, 납기일 준수 및 셋업최소화를 위한 공정 스케줄링 최적화

## reference
논문 : <https://scienceon.kisti.re.kr/srch/selectPORSrchArticle.do?cn=JAKO201925462479137&dbt=NART>
자료 : <https://hwk0702.github.io/projects/2019/11/08/Scheduler/>

## Create dataset for training
  1. dataset/data_create.ipynb open
  2. Hyper parameter setting(number of job types, number of orders, min process_time, max process_time, max due_date)
  3. Implementing data_create.ipynb

## Training

### environment_v1.ipynb
 - machine 마다 state 를 표현하기 위해 job_types의 변화유무와 납기일이 초과되었는지를 명시
 - reward = 50 + (-50*job_change) + (-5*violation_due_date) (job_change : job_type이 변화했는지의 유무, violation_due_date : 얼마나 납기일을 여겼는지의 int 형 변수)
 - train loss
 
 
 ![image](https://user-images.githubusercontent.com/78070883/112932087-483c6800-9158-11eb-8fc4-a7fdae107daf.png)



 - 


KSETEC 홈페이지: <http://kstec.co.kr/>   
   
      
     
     

Author: KSTEC 연구원 박재완, 조현우     
Last edited: 30-03-2021
