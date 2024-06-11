# YOLOv8를 사용한 Traffic_sign_recognition(교통 표지판 탐지 및 인식)
---


## **CONTENST**


## 공통으로 들어가야 하는 사항 


* **프로젝트 제목** : 프로젝트의 간략한 이름 및 설명

  
* **프로젝트 개요** : 프로젝트에 대한 전반적인 설명(내가 겪은 여려움을 어떻게 해결했는가?)

  
* **필요한 라이브러리 또는 프로젝트 한계점 설명**

  
* **추후 개선 사항** : 추가로 개선해야 하는 사항에 대한 정리 및 한계점 설명
---


## 머신러닝 & 딥러닝 파트


* **데이터 세트** : 데이터셋에 대한 설명 및 출처

  
* **모델 설명** : 사용한 머신러닝 / 딥러닝 모델의 종류 및 선택 이유

  
* **실험 결과** : 모델 평가에 사용된 지표와 결과(표 또는 그래프)
---


## 프로젝트 제목 : Korea_Traffic_Sign_Recognition


자율주행에서 CV를 통한 대표적 기술

자동차에 장착된 카메라가 교통 신호판 정보를 수집하고 신호의 종류와 위치 등을 인식,
 
교통 신호 정보를 파악하며, 교통 상황 등을 경보음과 같은 방식으로 운전자에게 정보를 전달하는

정밀함을 달성하기 위해, 자동차는 도로 표시를 이해하고 적절한 결정을 내려야 함.

이 기술의 중요성을 분석하면서 교통 표지판 분류 프로젝트를 시도한다.
![image](https://github.com/dbeodud147/traffic-sign-reconition/assets/163965664/0642fd32-78f5-4941-963b-b24a9bdd5718)

---
## **프로젝트 개요**


**1. 영상의 교통 표지판 객체 탐지**


![2024-06-11 21 03 04 (1)](https://github.com/dbeodud147/traffic-sign-reconition/assets/163965664/e58f4162-5c3c-4cfb-b5b9-5fb2bf1fb957)
![2024-06-11 21 04 52 (1)](https://github.com/dbeodud147/traffic-sign-reconition/assets/163965664/f1a5681e-5af1-4739-9c6d-b02ea26b4505)

---


**2. 프로젝트를 진행하면서 발견한 다양한 문제점**


1. 한국 교통 표지판의 데이터 셋 부족
2. 어렵게 구한 데이터 셋마저 좋은 데이터 셋이라고 판단할 수 없었음(Yolo에서 사용하는 data.yaml 파일 오류)
3. 한국 교통 표지판 데이터 셋이 없는 만큼 영상에서 필요한 동적인 객체(표지판)이 부족


![image](https://github.com/dbeodud147/traffic-sign-reconition/assets/163965664/1bc056c2-c5ee-4904-941f-d7e3927bab6a)





**3. 발견한 문제점에 대한 해결 방법**

https://universe.roboflow.com/project-x9thl/trafficsign2-dtlim

다른 데이터 셋에서 각 클래스 별 데이터 추출하기 


https://universe.roboflow.com/pbl2-nsmxa/pbl2-jtrh3


https://universe.roboflow.com/search?q=right%2520sign%2520left%2520sign&p=1


https://universe.roboflow.com/search?q=korea%2520wheelbarrow%2520sign&p=1


https://universe.roboflow.com/search?q=korea%2520wheelbarrow%2520sign&p=3


등 다양한 로보플로우 무료로 제공하는 다양한 데이터 셋을 사용함

1. 데이터 셋의 가장 큰 문제인 data.yaml의 클래스 수정(추가, 삭제, 변경)
2. 로보플로우에서 다른 한국 교통 표지판의 다양한 데이터 셋에서 각 객체에 필요한 클래스를 추출 
3. 위 출처에서 부족한 데이터 셋을 구하기 + 데이터 셋의 인스턴스 평균 맞추기
4. 3번을 수행한 후 각 클래스의 라벨을 재수정
5. 다양한 데이터 셋을 모아 하나의 새로운 데이터 셋 구축


## **필요한 라이브러리 또는 프로젝트 한계점 설명**


## **추후 개선 사항**


##  **데이터 세트**


## **모델 설명**


##  **실험 결과**
