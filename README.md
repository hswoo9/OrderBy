# ORDER-BY (back & front-end)
## Final-Project

* 수행기간: 2023년 03월 06일 ~ 2023년 04월 28일

* 개발목표 <br> 'ORDER-BY' 프로젝트는 비용 문제로 평소에 쉽게 접할 수 없는 특별한 차량과 오토바이를 경험해보고 싶은 성향의 사용자들을 위해 사이트를 기획. <br>
기존 자동차와 오토바이를 한번에 검색 할 수 없는 단점을 보안하기위해 차량과 오토바이 카테고리를 세분화 하여 사용자가 쉽고 편리하게 사용할 수 있도록 함.


  
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

## 유사사이트 선정

* 롯데렌터카
* 카타고렌터카


## 개발일정

* 주제선정 : 2023.03.06 ~ 2023.03.12
* 기획 및 UI 설계 : 2023.03.13 ~ 2023.03.26 카카오 오븐 UI설계
* DB 설계 : 2023.03.27 ~ 2023.04.29 기획을 바탕으로 DB설계
* 구현 : 2023.04.12 ~ 2023.04.26 DB를 바탕으로 구현


## 개발 주요사항

* Spring framework를 이용한 백엔드 개발
* 관리자 페이지에서 DB에 저장되어 있는 모든 데이터 관리(CRUD)
* 카카오 지도api 사용
* 메인페이지


## 개발 관련 설명

* 관리자 페이지에서 회원, 상품, 지점 등 모든 것을 관리하도록 개발
* 메인페이지에서 바로 결제 가능 및 인기차종 특가상품 선택가능
* 차종 및 요금은 자동차 및 오토바이 테이블에 있는 DB를 중복제거하여 가져오기
* 보험 관련하여 주민번호를 받아와서 보험가입 등을 할려고 했으나, API문제로 연결실패


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

* 메인페이지 - 메인페이지는 상단에 메뉴바를 만들어서 진행
아래 첫번째는 이 달의 특가로 해당지점에 차량을 30%할인하여 대여를 진행
차량은 2대 오토바이는 1대이며 한달에 한번씩 특가차량은 변경
아래 두번째는 인기 차종으로 대여를 진행하게되면 count가 증가하는데 보유한 모든 차량의 count가 높은순서대로 swipe-slide로 처리하여 6개만 노출

<div align="center">
  
  <p><strong> 메인페이지 </strong></p>
  
  <img src="https://user-images.githubusercontent.com/118333635/236735637-7a40a1c7-f486-4e96-b6d4-45d81d7d5385.png"  width="50%" height="50%"> 
</div> 

* 관리자페이지 대시보드 페이지 - 현황판의 경우에는 총 비용 / 보유 차종 / 전국 매장 수가 존재
총 비용의 경우 결제완료된 모든 price값을 더한값이고 보유 차종은 orderby에서 보유중인 차종수이고, 매장 수는 order by에서 소유하고 있는 매장의 카운트 수 

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/a27b04a9-d4ac-4957-83f6-ca01cbdebc8b)
</div>


* 회원관리 페이지 - member table에 있는 데이터를 가져와서 보여주는 방식
* 
<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/2a2701bf-a0ac-4297-9059-5c8b6c021a84)
</div>


* 회원정보관리 페이지 - 회원 이름을 선택하면 db에 있는 해당하는 회원의 정보값을 가져온 후 수정이 가능하게 구현
회원 탈퇴를 진행하게되면 status값이 n으로 변경되고 status가 n값이면 활성화 버튼으로 다시 status값을 y로 바꿔줄수있으며, 비밀번호는 암호화처리로 진행

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/039ce841-f5b3-43b4-9ca1-335d8e18b75f)
</div>


* 상담관리 페이지 - popqna table에 있는 데이터를 가져오는 방식

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/e10a5612-9f36-4971-b5f0-c97cfce2efee)
</div>


* 상담 내용 확인 페이지 - 메인홈페이지에 실시간 상담을 진행하게 되면 db값에 저장된 것을 불러오는 것입니다.
이름을 선택하면 db에 해당하는 상담의 정보를 가져온 후에 전화/이메일을 통하여 상담을 진행 후에 답변 확인 버튼을 클릭하여 답변완료 값으로 변경해줍니다.

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/091289e2-37cd-4bd9-9921-6031ec831ca9)
</div>


* 결제 내역 관리 페이지 - payment table에 있는 데이터를 가져오는 방식
  
<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/6545038c-da9c-4106-8ee8-4c1a53f89791)
</div>


* 결제 내역 확인 페이지 - 상품 이름을 클릭하면 db에 있는 해당하는 정보를 가져옴
 결제 상태가 y이면 결제 취소가 가능하게 되어있으며, 결제를 취소할 경우 결제 최종 금액에 80%를 해당하는 회원의 포인트로 반환

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/2cac6535-02fb-45dc-b9fb-54694bcbe0f5)
</div>


* 자동차 정보 수정 페이지 - 자동차 이름을 눌러 db에 있는 정보값을 가져온 후에 수정 / 삭제(활성화)를 가능하게 구현

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/7b310032-df00-46f4-aeed-8f1c2aa938cf)
</div>


* 오토바이 정보 수정 페이지 - 오토바이 이름을 눌러 db에 있는 정보값을 가져온 후에 수정 / 삭제(활성화)를 가능하게 구현
  
<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/59d59dc1-0143-4a83-b86f-dafe2327f099)
</div>


* 자동차 등록 페이지 - 자동차를 등록하게 되는 폼이며
자동차를 등록할때 사진을 넣으면 해당하는 브랜드에 자동으로 사진이 저장되고 
매장위치를 선택하면 매장위치에 해당하는 StoreNo값을 가져오며, 사진을 등록하면 Pfile이라는 table에 있는 PfileNo값도 가져옴

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/1a063d7b-5e6c-469d-85ff-ae32414d0e52)
</div>


* 매장 관리 페이지 - store table에 있는 데이터를 가져오는 방식

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/b368e846-aac4-464f-aad8-c630fddd6bd9)
</div>


* 매장 정보 수정 페이지 - 해당 이름을 선택하면 db에 있는 정보를 가져오며 위도값과 경도값을 가져온 후 지도에 해당하는 장소를 보여준 후, 다른 테이블과 같이 수정 / 삭제(활성화)를 가능하게 구현

<div align="center">  
![image](https://github.com/hswoo9/OrderBy/assets/118331567/e4598f4b-c650-4750-99f1-ea607d28f6be)
</div>


* 매장 등록 페이지 - 매장을 등록하는 폼이며,
주소검색으로 주소를 검색하면 그 해당하는 주소의 지도와 위도 경도값을 가져온후에 매장이름과 매장 보유 차종수를 기입하여 insert하면 store table에 저장

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/fd7c190f-c200-48df-8bb3-a2e57b378ca5)
</div>


* 차종 및 요금 페이지 - UI식으로 구현되어있으며,
자동차나 오토바이는 테이블에서 중복값을 제거하고 가져옴

<div align="center">
![image](https://github.com/hswoo9/OrderBy/assets/118331567/80ce7691-ef42-4562-88c7-f777fd994f9f)
</div>


## 아쉬웠던 점

* DB를 준비를 열심히 하면서 ERD를 나름대로 구현하였지만 구현과정중에 Table을 변경해야 하는 상황이 있어, 초반 설계에 대한 아쉬움
* 여러가지 API를 사용하고 싶었으나 지식이 부족하여 많은 API를 사용하지 못한점
* 조장으로써 팀원들과의 의사소통을 최대한 신경쓰면서 했지만 중간중간 의사소통문제로 문제가 발생한점
