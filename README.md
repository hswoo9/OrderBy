# ORDER-BY (back & front-end)
## Final-Project

* 수행기간: 2023년 03월 06일 ~ 2023년 04월 28일

* 개발목표 <br> 'ORDER-BY' 프로젝트는 비용 문제로 평소에 쉽게 접할 수 없는 특별한 차량과 오토바이를 렌트할 수 있는 웹 서비스입니다. <br> 사용자들이 원하는 차량 및 오토바이를 간편하게 검색하고 렌트할 수 있는 기능을 제공합니다.


  
## 개발 환경

  |제목|내용|
  |-----|----|
  |운영체제|Window OS, MacOS|
  |개발도구|Spring framework, SqlDeveloper, Visual Studio Code|
  |DBMS|Oracle|
  |Server|Apache Tomcat 9.0|
  |Language|Java 11, JavaScript, jQuery|
  |디자인툴|HTML5, CSS3|
  |협업툴|ERD cloud, Jira, Git hub|
  
-Jira
![image](https://github.com/hswoo9/OrderBy/assets/118331567/bf07ce67-7dca-4bde-9f34-b4ca52e312a7)

-ERD Cloud
![image](https://github.com/hswoo9/OrderBy/assets/118331567/8f4ab56d-c003-42de-adc2-0853e16c639a)


## 개발 주요사항

* Spring framework를 이용한 백엔드 개발
* 관리자 페이지에서 DB에 저장되어 있는 모든 데이터 관리(CRUD)
* 카카오 api 사용
* 메인페이지


## 개발 관련 설명

* 관리자 페이지에서 회원, 상품, 지점 등 모든 것을 관리하도록 개발
* 메인페이지에서 바로 결제 가능 및 인기차종 특가상품 선택가능
* 차종 및 요금은 자동차 및 오토바이 테이블에 있는 DB를 중복제거하여 가져오기


## 관리자 페이지
* 회원관리
회원 삭제 / 수정 / 탈퇴관리 
STATUS값을 'F'면 회원 비활성화 계정 
* 예약된 차량 or 오토바이 현황 
차량이나 오토바이 예를 들어 1번차량을 선택하면 언제부터 언제까지 예약이 되어있는상태를 확인
* 상담처리 페이지 
실시간상담으로 상담내용을 전달하면 이름 / 전화번호 / 내용이 관리자계정 상담처리 페이지로 지정 
처리는 전화번호로 전화나 문자로 진행 처리가 완료되면 처리완료처리
* 차량등록 and 오토바이등록
차량 or 오토바이 등록시에 대여DB에 등록
* 차량, 오토바이 수정 
ex) 차량을 이미 빌려서 주행거리가 늘어날수 있으니 주행거리 수정등 수정할수 있도록

 

## 프로젝트 UI


<div align="center">
  
  <p><strong> 메인페이지 </strong></p>
  
  <img src="https://user-images.githubusercontent.com/118333635/236735637-7a40a1c7-f486-4e96-b6d4-45d81d7d5385.png"  width="50%" height="50%"> 
</div> 
