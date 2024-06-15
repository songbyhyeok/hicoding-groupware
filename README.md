![1](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/6c373e92-872b-4fec-9306-0f575ebf399d)

# 하이코딩 그룹웨어
**URL** -> https://github.com/Hicoding-Groupware  
**분류** -> 팀 프로젝트 (F-S 5명)  
**날짜** -> 2023.11.07 ~ 2023.12.22  
**환경** -> React(ReduxThunk, Middleware), Spring(Boot, Security, DataJPA, Criteria), Deploy(AWS, Docker, Ubuntu), MySQL  
**Demo** -> <a href="http://songbyhyeok-deploy.s3-website.ap-northeast-2.amazonaws.com" target="_blank"> (admin, 1234) </a>  

![image6](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/9d18f237-2589-4b48-8715-e4131f8d75e1)

## 소개
공.사교육의 성장으로 이에 따른 증대된 학원들의 시스템 관리 어려움을 그룹웨어 도입으로 해소할 수 있다 판단. 또한, 4차 산업 IT 시장의 유망성을 고려하여 이를 목표로 프로젝트 도입. 해당 프로그램은 인사, 사내, 업무 기능의 시스템 중심으로 구성되어 있고, 유기적 협업 및 관리를 통해 효율적 업무 처리와 높은 생산성을 기대할 수 있다.

## 기능
![Untitled](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/1bfb1b41-9b76-4bc4-9a34-48876d1b6ae5)
**직원관리(사원 생성, 사원조회)** 에서 회원가입 일부 시스템인 사원 ID 발급 기능을 통한 사원 생성, 옵션 선택 항목 기준으로 사용자 정보를 조회할 수 있는 사원 조회 기능 구현  
**게시판(공지사항)** 에서 게시판 쓰기.읽기.수정.삭제, 답글과 대댓글 그리고 조회수 처리와 좋아요 기능 구현

## 프로그램 개발
![11](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/83997b82-e226-42b5-9d9b-2a012d0456c0)

### 이슈 관리
![12](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/0597c3fa-f366-4bfe-b990-16f555f10b40)
<em> Github Issue Role 시스템 메뉴얼과 Branch에 Issue 관리와 상태를 기록한 그림이다. </em>
![13](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/efe4bbf0-82e3-461f-be72-28bf417361df)
<em> Notion 페이지에 작성된 Issue 기록들 </em>

팀 내에서 GitHub 이슈 관리 시스템을 효율적으로 활용하기 위해 관련 메뉴얼을 공유했고, 각자 맡은 기능을 Branch를 통해 중점적으로 관리하면서 체계적이고 협동적인 개발이 가능하였다. 또한, 개발 중 발생하는 이슈 상황을 문서화하기 위해 Notion 페이지를 활용하여 각자가 공유하였다.

### 기획 과정(11.07 ~ 11.25)
![Untitled (1)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/d81a8f3d-10cd-4415-a7cc-dc044b150194)  
<em> 위 그림은 hicoding 프로젝트 당시 Notion을 활용한 작업장이다. </em>

사전 조사 및 설계 단계로서 1.프로젝트 주제 및 기능 분배 | 2.프로토타이핑.업무흐름도.ERD | 3.REST API 설계의 세 가지 단계로 분류 및 절차대로 수행해 나갔다. (1번 부분은 위에 설명을 했으므로 생략하고 2번 부분부터 시작하게 된다.)

#### 2. 프로토타이핑 / 업무흐름도 / ERD
![5](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/d623abde-94e8-41ce-aa60-c40c8808a989)
<em> Figma, FigJam Tool을 활용하여 설계된 프로토타이핑과 순서도 </em>

각자 맡은 기능에 대한 요구 사항 명세서를 작성한 후, 이를 바탕으로 프로토타이핑과 순서도를 함께 도식화하였다. 그 결과 빠르고 정확한 소통과 개발 환경에 산출물들을 바로 코드화하여 높은 생산성을 달성할 수 있었다.

![image17](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/3523e0f4-e5c2-4d5f-aec3-1b76b522402f)
<em> 요구사항 수집과 분석 및 개념적, 논리적 모델링 단계 과정을 거쳐 완성된 ERD </em>

프로젝트 주제와 기능 분배 이후, 각자의 기능에 대한 요구사항을 수집 및 분석한 후, 회의를 통해 개념적 데이터 모델링을 수행하였다. 이 과정에서 카디널리티 개념을 활용하여 모델링 연관관계를 구축 단계를 거쳐, 논리적 모델링을 위한 데이터 정형화 및 정규화 과정을 거쳤고, 마지막으로 물리적 모델링 단계에서 MySql과 사상시켰다.

##### DA#Modeler5 Tool Query Script 기여
- 본 프로그램에서 논.물리 모델링과 Query Script 커스터마이징 생성을 통해 팀 생산성을 높일 수 있었다.
- 문제점을 인식 및 개선안을 도출하는 것은 중요한 일이라고 생각했다. 기존의 방식으로는 체계적인 관리가 이루어지지 않아, 쿼리 작성이 형식적으로 이루어졌으며 무분별한 테이블 삭제로 인해 PK의 무결성 문제가 발생했다. 개발자로서 하나의 목표는 생산성 향상과 사용자 경험 개선이었다. 따라서 팀 프로젝트에서 결과물도 중요하지만, 과정에서 발생하는 사소한 불편한 문제들도 해결 및 향상시키는 경험이 목표를 달성하는 데 도움이 될 것이라고 판단하여 이를 실행하게 되었다.  

**논리 모델링에 기여한 점**  
<img src = https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/74a5acfd-18fa-4808-b999-e57d3a7323d0 width = "50%" height = "50%">  

이전 프로젝트나 타 프로젝트 작업 과정을 보면 산출물 업로드를 단순 ↓로만 하기 때문에 관리되지 않는다는 것을 인지하였고, 형상관리 Tool을 고려하긴 했으나, 기존 Notion 방식에서 날짜 기입을 통해 단점을 보완하였다.

**물리 모델링에 기여한 점**  
<img src = https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/215cda91-74c7-45dc-b6bd-bc080be76925 width = "50%" height = "50%">  

기존 물리 모델링은 Create And Drop Query만 공유하였지만, 해당 프로그램의 DDL 옵션을 통해 Create Table, Drop Table 등 다양한 Script를 생산하였다. 그리고 물리 모델링 옵션을 통해 얻은 성과 중 가장 큰 것은 Increment 설정이다. 무분별한 삭제로 Increment 시작값이 0부터 아니게 되거나, 특정 시작 위치에서 생성이 필요할 때가 있어 이를 TIP란에 자세히 기입해 두었다. 그리고 마지막으로 직원 정보를 랜덤 생성 알고리즘을 통해 Dummy Query에 기여하였다.

#### 3. REST API 설계
![Untitled (4)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/6563d8a5-5a17-4818-9755-fd416dfb2e8a)
<em> Notion Tool을 활용한 REST API 문서화 산출물 </em>

REST API를 설계할 때 일관성과 명확성을 검토 및 개선함으로써 해당 API의 시스템을 보다 더 이해할 수 있었고, 팀원간 효율적인 의사소통과 협업 능력을 향상시켰다.

### 구현 기능(11.25 ~ 12.10)
#### AWS, Docker 활용 배포
![final-hicoding-Page-1 drawio](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/d8e673d8-db29-4172-a6f6-649f7790e0e0)
<em> 배포된 Groupware System Architecture </em>

**간략 설명**
- 서버는 EC2의 Ubuntu에 SSH를 통해 Docker Engine을 설치한 후, Docker Image에 저장된 Back Build 파일을 Docker Cotainer를 통해 구동시키는 방식이고, Client는 Front Build 파일을 S3 버킷에 업로드하여 호스팅 상태로 만들고, 사용자가 Endpoint를 통해 접속하게 된다.

**배포 이슈**
- 정적 웹사이트 호스팅 후 서버 연동이 안되는 상황
  - 서버 구동이 안됐다는 것은 Docker 컨테이너에서 구동되지 않은 걸로 간주, Docker 메커니즘 부분을 다시 학습한 후 ‘docker run’ 명령어를 통해 해결
 
- 서버가 구동 중이지만, DB 연동이 되지 않는 현상
  - 로그인을 할 수 없는 상태라면 AWS 그룹 접근 권한이 올바르게 설정되지 않은 것으로 추정, 이를 확인하고 조정하였으나 문제가 지속됐고, 서버가 연결된 상태인 것을 감안 Spring과 DB의 연동이 되지 않은 것으로 의심하여, Table 명들이 대문자로 표기되어 연동되지 않는 것을 확인하여, 이에 모든 테이블 명을 소문자로 변경하여 문제를 해결
 
#### 답글, 대댓글 구현(Tree 형태로 재구축 후 DFS-Stack 처리)
![Untitled (5)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/8346c973-435a-42f9-9ea9-cd2ba28eddf4)
<em> 데이터를 계층구조 변환 후 페이징화 처리 과정과, DFS의 두 가지 방식으로 처리했을 때 상황을 결과물로 표현 </em>

**출력 과정에서 구조적 이슈**
![Untitled (6)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/f6d06b00-a520-4886-8ff6-f879226b33b0)
<em> dfs 출력 방식에 따라 구조가 달라지는 것을 알 수 있다. </em>

- 레벨 0의 부모들을 게시판에 배치하기 위해 dfs 재귀 방식을 사용했을 때 등록일자 순으로 게시판 상단에서 하단으로 출력되는 문제가 발생, 이는 등록일자를 역순으로 재구조화 시 간단히 해결될 문제라 판단하여 역출력을 시도하였다. 그러나 위 그림의 reverse order DFS - recursive 형식처럼 depth 0의 배치만 역으로 바뀌는 현상이 발생하였다. 문제는 부모의 자식을 먼저 출력시켜야 되는 부분에 있어 재귀 방식은 처리할 수 없어, 이를 다른 stack 방식을 채택하여 역순의 자식들을 먼저 삽입하고, 지정된 크기 5 이상이 될 경우 출력 및 비우기를 반복하여 해결.

**계층구조 변환**
![Untitled (8)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/c4ef0f6a-0faf-4651-afc8-a09ea452bab0)
<em> "PostReadResponseList"에서 저장되는 객체는 레벨 0에 있는 "Parent" 객체만 포함하고 있으며, 자식들은 "Parent" 객체의 필드인 리스트에 저장된다. </em>

- 취합된 데이터를 답글이나 대댓글의 형식으로 처리하기 위해 트리 구조로 표현하는 게 적합 및 판단하였고, 동일 레벨의 여러 개 자식을 구성할 수 있는 m-ary 트리 형태로 변환하기로 결정. 이를 위해 먼저 데이터 집합에서 레벨이 가장 낮은 부모를 최초 리스트에 저장하고 그 외의 자식들은 해당 부모의 리스트에 저장하는 방식으로 처리

  - 계층구조화 변환 과정에서 양방향 Entity JSON 변환 시 순환 참조 문제**
  ![Untitled (10)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/f5e8df72-9726-4343-b78f-44e96598a888)
  <em> 양방향 매핑 과정에서의 참조 이슈에 대한 오류 분석과 해결 방식으로 Entity가 아닌 DTO 필드로 대체한 것을 나타낸 그림 </em>

    - 양방향 JSON 변환 과정에서 Stack Overflow 발생. 원인은 멤버 필드 Entity 참조 과정에서 부모와 자식의 사이클 형성, 이를 방지하기 위해 Entity가 아닌 DTO 필드로 변환시켜 해결

**페이징 처리 문제**
![Untitled (12)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/1a5b04e8-d3bb-41bc-bed7-6aea17f95e56)
<em> Pageable → Page<T> → Pagination 세 단계 절차를 CustomPagination 객체로 대체 </em>

- 쿼리 결과를 JPA의 Page<T> 객체로 변환하는 과정에서 계층구조에 맞게 가공된 데이터에는 PagingButtonInfo를 적용할 수 없는 문제가 발생, 이를 해결하기 위해 기존 방식을 CustomPagination 객체에 옮겨 해결

#### 조회수. 좋아요 구현
![Untitled (13)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/c026dfed-b767-4e88-ba73-db3f585791ca)
<em> 게시글의 조회수와 좋아요 기능이 작동되고 있다. </em>

![Untitled (15)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/08d0d1e2-10e6-4cb2-802f-a11d6fba98f9)
<em> 좌측은 물리데이터와 카디널리티 관계 정의를 나타내고 있고, 우측은 각 사용자가 조회수나 좋아요 클릭 시 작동되는 Logic을 보여주고 있다. </em>

게시글을 읽거나 좋아요 버튼 클릭 시 횟수가 누적되게 구현. 각 사용자마다 개별적으로 동작시키게 하기 위해 물리 모델링에서 게시글과 사용자 사이에 연결되는 기록을 만들어 카디널리티 관계 재구성, 그리고 프로세스 처리 과정에서 첫 방문자 | 방문한 적이 있는지 두 가지 여부로 판단. 첫 방문자의 경우 최초로 게시글을 읽거나 클릭 시점에 방문자의 정보가 없으므로 동작하도록 처리, 이미 방문한 적이 있는 경우는 현재 시간과 방문 시점의 차를 계산하여 설정된 시간을 넘었을 때만 횟수가 누적되도록 설계.

#### 사원 생성 및 상세조회
![Untitled (16)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/7ef9c291-9d4b-45d6-ae9c-40861b5337db)

부서별 사원 ID와 임시 비밀번호를 제공하는 사원 생성 시스템과 옵션 선택 항목 기준으로 동적 쿼리 조회가 가능한 JPA Criteria JPQL 빌더 클래스 기능을 구현

**사원 생성 알고리즘**
- 회원가입 과정에 필요한 부서별 사용자 식별 ID 생성 시스템을 구현하기로 결정, 기능을 개발하기 위해 부서별 번호 체계 정보를 참고. 위 그림에서 (BB 02)는 권한에 맞게 ENUM 값을 활용하였고, (ex ADMIN = 01, STAFF = 02) CC는 최대 입사자 수와 현재 입사자 수를 비교하여 계산하였다. (ex if (MAX = 1000, CurrNo = 55) then Max 0의 개수인 3 - CurrNo 0의 개수인 1의 결과인 2개가 CurrNo 앞에 붙여 결과는 ID = 0055가 된다.) 이를 모두 결합하여 사번 ID를 생성하면 다음과 같다. ‘hc + AA(23) + BB(02) + CC(0055) = hc23020055’
- 해당 알고리즘을 구현하며 고려사항 두 가지는 다음과 같다. 1. 같은 부서에 Next ID 생성, 2. 부서별 최대 인원수를 초과하지 않고 좌측에 여백이 있을 경우 0으로 채우기. 첫 번째 경우는 현재 부서의 마지막 ID + 1 계산 방식을 사용하여 처리, 두 번째 경우는 좌측에 0이 들어갔을 경우에 대해 ex Max = 1000, CurrVal = 100일 경우, 결과 값은 ‘0100’로 가정 및 접근하여 Max와 CurrVal의 0의 자리를 뺀 값을 조합하여 문제를 해결

**사원 조회**
- 기존 Spring Data Jpa로 복잡한 JQPL을 처리 문제에 대해 JPA Criteria를 혼용하여 동적 쿼리 조회 기능을 수행, 구현 과정 중 두 가지 애로사항 발생, 1. Criteria 빌더 재구조화, 2. 조회 이후 Front에서 정렬 처리
  - Criteria Builder 재구조화
  ![Untitled (19)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/0c824781-813f-4cd7-b4c4-01d4fb6cd9b6)
    - 하나의 쿼리를 호출하기 위해서는 복잡한 절차와 상당한 비용이 들 것임을 인식하였고, 방치하게 된다면 유지보수가 어려워질 것으로 판단하여, 이를 해결하기 위해 리팩토링 시도 및 해결.
    - 조회 후에도 정렬을 위해 Criteria 정렬 처리 쿼리를 요청하는 것은 비용이 높다고 판단되어 사용하지 않고, Front 자체에서 JS 정렬 처리 알고리즘을 사용하여 문제를 해결
   
#### 게시판과 댓글 CRUD 구현 (React(Redux, Thunk), RestAPI CRUD)
![Untitled (20)](https://github.com/songbyhyeok/2023-HicodingGroupware/assets/63230518/85913404-be35-4b14-bb45-296833d4678a)
<em> React Redux와 Spring Restful을 결합하여 구현된 게시판과 댓글 CRUD 그림 </em>

주어진 두 주기인 React의 Redux와 Thunk, 그리고 Spring과 Restful API 시스템을 연동하여 게시판과 댓글 CRUD 기능을 구현. 클라이언트 측에서는 Redux를 사용하여 웹의 데이터 상태를 저장 및 관리하고, Thunk는 Dispatch 역할 및 비동기 작업 처리를 담당. Restful API는 양 측 간의 데이터 교환 및 표준화 역할을 수행

### 회고
두 번째 프로젝트다 보니 전보다 더 잘 소화해야만 했고, 기존 Thymeleaf을 사용한 통합된 환경이 아닌 리액트 프레임워크를 활용한 비동기 통신으로 개발을 진행해야 됐기 때문에 기간 내 수행 속도를 올려야만 했고, 부담감이 상당했었다.  

#### 협업과 품질 향상을 위한 노력
정형화된 물리적 모델을 통한 스크립트의 무결성과 생산성을 향상시키기 위해 물리적 도구의 다양한 옵션을 연구하고 접목한 결과, 팀 내 협업이 촉진되어 신뢰성과 전반적인 퀄리티가 향상되었다. 이를 통해 상호 의존성을 줄이고 주도적인 행위를 통해 유연성과 적응력을 높일 수 있었다. 차후 협업 프로젝트 시 개발 외 문서화 및 대화 방식에 있어 효율적인 방안에 대해 초점을 두고 진행하면 좋겠다는 생각이 들었다.

#### 알고리즘 문제 해결 경험
답글과 대댓글 구현 과정에서 쿼리를 통한 조회 방식과 알고리즘 설계를 통한 가공 방식 두 가지 방법이 있었는데, 익숙한 알고리즘 설계 방식을 채택하여 비용을 줄였다. 하지만 Entity 모델링 설계부터 계층구조화 그리고 지원되지 않는 페이징 알고리즘을 직접 구현해야 하는 변수와 DFS 재귀 방식으로 데이터를 읽어들였더니 각 계층의 부모를 역으로 출력해야 하는 문제는 풀리지 않아 골치 아팠다. 그러나 지하철에서 DFS-stack 방식을 통해 처리하면 된다는 사실을 갑자기 깨닫고 이를 실제 접목시켜 터득했던 경험. 지금 와서 생각해 보면 개발자는 역시 끙끙 앓다가 무의식적으로 힌트를 제공받고 이를 시도하여 해결하는 성취감에 한다는 것을 새삼 다시 깨닫게 된다.
