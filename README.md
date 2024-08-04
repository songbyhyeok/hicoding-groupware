## 하이코딩 그룹웨어
<p align="center">
  <img src="https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/6c373e92-872b-4fec-9306-0f575ebf399d" style="width:100%" alt="image6">
</p>

<div align="center">
  
  ### IT 개발 교육 플랫폼
  
</div>

공.사교육의 성장으로 이에 따른 증대된 학원들의 시스템 관리 어려움을 그룹웨어 도입으로 해소할 수 있다 판단. 또한, 4차 산업 IT 시장의 유망성을 고려하여 이를 목표로 프로젝트 도입. 해당 프로그램은 인사, 사내, 업무 기능의 시스템 중심으로 구성되어 있고, 유기적 협업 및 관리를 통해 효율적 업무 처리와 높은 생산성을 기대할 수 있다.

---

* 팀 프로젝트: (F-S 5명)
* 개발 기간: 2023.11.07 ~ 2023.12.22
* 기술스택
  * Spring, JPA, MyBatis, Restful, Dbms(Oracle, MySQL), Deploy(AWS, Ubuntu), React  
    Git/Github, PostMan, DA#Modeler, SQL Developer, MySQL Workbench, Slack, Figma
* Teamwork
  * github: [Link](https://github.com/Hicoding-Groupware/hicoding-back)
  * notion: [Link](https://www.notion.so/songbyhyeok/hook-7911c64b8d394009b49804a39a0d302c?pvs=4)
    
---

## 담당 역할
<p align="center">
  <img src="https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/1bfb1b41-9b76-4bc4-9a34-48876d1b6ae5" style="width:70%; height:70%;" alt="image6">
</p>

**직원관리(사원 생성, 사원조회)**  
  * 사원 ID 발급 기능을 통한 사원 생성, 옵션 선택 항목 기준으로 사용자 정보를 조회할 수 있는 사원 조회 기능 구현
    
**게시판(공지사항)**  
  * 게시판 쓰기.읽기.수정.삭제, 답글과 대댓글 그리고 조회수 처리와 좋아요 기능 구현

## 개발 기간
<img src="https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/83997b82-e226-42b5-9d9b-2a012d0456c0" style="width:100%; height:100%;" alt="image6">

## 목업
<details>
<summary>열기/닫기</summary>
<div markdown="1">       

![직원관리 상세조회](https://github.com/user-attachments/assets/d861e401-24b7-40a7-ad8b-7909e8305dad)
![직원관리 생성](https://github.com/user-attachments/assets/8753db2a-58fb-49ff-a8e8-0d3f26b7ad03)
![공지사항 게시글](https://github.com/user-attachments/assets/4a134731-60f0-4324-8dc5-4cc6c31956b1)
![공지사항 게시판 글쓰기](https://github.com/user-attachments/assets/d78e1f41-6ee2-4318-855b-5720b35a8024)
![공지사항 게시판 글쓰기-1](https://github.com/user-attachments/assets/0a61721e-fd8f-48d1-be23-d81c4b13d7bc)
![공지사항 게시판 글쓰기-2](https://github.com/user-attachments/assets/01ea1780-93c2-4be5-a2e9-169fd975fe10)
![공지사항 게시판](https://github.com/user-attachments/assets/66ed9d92-a4f8-4b53-9989-8f8db0ceb547)
![공지사항 게시판-1](https://github.com/user-attachments/assets/f44a2ea0-997d-474c-a688-d11777e54c3b)
![공지사항 게시판-2](https://github.com/user-attachments/assets/c1b80d47-0e41-4392-aee2-a8a262febc3d)
![공지사항 게시판-3](https://github.com/user-attachments/assets/20a28ac4-8f42-496c-a32b-da12a0a957db)
![공지사항 게시판-4](https://github.com/user-attachments/assets/b6cfac52-a6b9-499e-9e21-a7185e552f6c)
![사원 생성](https://github.com/user-attachments/assets/86b57f60-bee7-4022-98bd-cb14279378db)

</div>
</details>

## ERD
<details>
<summary>열기/닫기</summary>
<div markdown="1">       

![image17](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/3523e0f4-e5c2-4d5f-aec3-1b76b522402f)

</div>
</details>

## 플로우 차트
<details>
<summary>열기/닫기</summary>
<div markdown="1"> 

<img width="3127" alt="Untitled (2)" src="https://github.com/user-attachments/assets/acae5ee4-5089-4569-9d6b-495154d642d3">

</div>
</details>

## API 문서
<details>
<summary>열기/닫기</summary>
<div markdown="1">       

![Untitled (4)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/6563d8a5-5a17-4818-9755-fd416dfb2e8a)

</div>
</details>

## 아키텍처
<details>
<summary>열기/닫기</summary>
<div markdown="1">       

![final-hicoding-Page-1 drawio](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/d8e673d8-db29-4172-a6f6-649f7790e0e0)

- 서버는 EC2의 Ubuntu에 SSH를 통해 Docker Engine을 설치한 후, Docker Image에 저장된 Back Build 파일을 Docker Cotainer를 통해 구동시키는 방식이고, Client는 Front Build 파일을 S3 버킷에 업로드하여 호스팅 상태로 만들고, 사용자가 Endpoint를 통해 접속하게 된다.

</div>
</details>

## 기술적 이슈 및 해결과정 (11.25 ~ 12.10)
[Link](https://github.com/songbyhyeok/2023-hicoding-groupware/wiki/%EA%B8%B0%EC%88%A0%EC%A0%81-%EC%9D%B4%EC%8A%88-%EB%B0%8F-%ED%95%B4%EA%B2%B0%EA%B3%BC%EC%A0%95)

## 회고
[Link](https://github.com/songbyhyeok/2023-hicoding-groupware/wiki/%ED%9A%8C%EA%B3%A0)
