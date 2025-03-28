# ☸️ Kubernetes 기반 Java 애플리케이션 배포

## 📖 프로젝트 소개

이 프로젝트는 **Java 애플리케이션 이미지**를 생성하고 **Docker Hub**에 업로드 후 **Kubernetes** 환경에서 배포하고 관리하는 실습을 수행합니다. 

**Minikube** 환경에서 **Deployment** 및 **LoadBalancer 서비스**, **NodePort 서비스**를 이용하여 컨테이너화된 애플리케이션을 외부에서 접근할 수 있도록 구성합니다.


## 🛠️ 프로젝트 목적

✔ **Docker Hub**와 연동하여 이미지를 **push & pull & deploy**하는 실습
  
✔ **Docker + Kubernetes**를 활용한 **애플리케이션 배포 자동화** 경험
  
✔ **NodePort 서비스**를 활용한 직접적인 노드 접근 방식 학습
  
✔ **LoadBalancer 서비스**를 통한 외부 트래픽 처리 방식 이해

## 📘 개발환경


![Java](https://img.shields.io/badge/Java-FF7800?style=for-the-badge&logo=Java&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=Spring-Boot&logoColor=white) ![VMWare](https://img.shields.io/badge/VMWare-607078?style=for-the-badge&logo=VMware&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=Kubernetes&logoColor=white)

## 🛠 구현
### 1. JAVA 애플리케이션 이미지화


✔jar 파일 생성


![image](https://github.com/user-attachments/assets/9bbae317-b551-46d1-a349-edce739d76d6)
![image](https://github.com/user-attachments/assets/4d1a89dc-fc72-4b8e-92c9-986146932d8f)


✔dockerfile 생성 후 이미지화


![image](https://github.com/user-attachments/assets/b5c85ce7-2f2c-4501-a94e-e40b0068571e)
![image](https://github.com/user-attachments/assets/fa15deb9-e183-4b43-bea1-21011ec232a1)


### 2. docker hub 푸쉬


![image](https://github.com/user-attachments/assets/ddf11213-c63b-4780-8768-ec7a6bcf2ee7)
![image](https://github.com/user-attachments/assets/e85617a6-11c7-49c2-9208-54fe029f4d65)


### 3. NodePort 서비스 배포


✔nodeport.yaml 생성 및 배포


![image](https://github.com/user-attachments/assets/f8ec6fe3-d699-473a-b83e-934b1560e6db)
![image](https://github.com/user-attachments/assets/0e1d6b1f-dbe5-4faa-b3de-4e5ecab843a6)


✔포트포워딩 후 JAVA APP 정상 접속 확인


![image](https://github.com/user-attachments/assets/b111964d-42e6-4cda-91ed-aca359ccfb32)


### 4. LoadBalancer 서비스 배포


✔loadbalancer.yaml 생성 및 배포


![image](https://github.com/user-attachments/assets/a9e438b2-1363-4f09-973a-92c1e6b8a056)
![image](https://github.com/user-attachments/assets/3b711be0-6176-4ddc-80df-50c498d5aa35)


✔원활한 서비스 위해 터널링 진행


![image](https://github.com/user-attachments/assets/b79d2d6e-21db-409e-8666-5e37cc0f55b9)
![image](https://github.com/user-attachments/assets/265dc553-30d8-447e-81a1-3185423c7d0b)


✔포트포워딩 후 JAVA APP 정상 접속 확인


![image](https://github.com/user-attachments/assets/2008918f-5346-478e-aa4f-628edeb4680a)


✔로드밸런싱 확인


  -브라우저 접속 시, 요청이 여러 pod에 분산되어 트래픽이 발생

  
  -크롬 접속 시 왼쪽 pod 트래픽 발생

  
  ![image](https://github.com/user-attachments/assets/a5243382-50cf-4744-9f94-801f7bc6b627)

  
  -엣지 접속 시 오른쪽 pod 트래픽 발생

  
  ![image](https://github.com/user-attachments/assets/17242536-d577-4ba3-aa85-8177aa3a8320)






  
