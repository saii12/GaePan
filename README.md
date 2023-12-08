# GaePan 프로젝트 작업 일지

프로젝트 기간 : **_2023-11-03 ~ 2023-11-30_**

프로젝트 한줄 소개 : __유기동물 분양 및 입양 커뮤니티 사이트__

<br/>

| 이름 | 역할 | 담당 |
| --- | --- | --- |
| 강원빈 | 팀원 | pet 화면 구현 |
| 권능환 | 팀원 | admin 화면 구현 |
| 고성우 | 팀원 | mypage 화면 구현 |
| 박한산 | 팀원 | cs 화면 구현 |
| 손영우 | 팀원 | 회원가입 및 시큐리티 작업 |

<br/>

**개발 환경**
- Intellj
- Java 17
- Spring boot 3.1.5
- MySql
- MyBatis
- JPA
- thymeleaf
- HikariCP
- Notion
- Github

<br/>

**Dependencies**
- JPA
- oauth2
- security 6
- thymeleaf
- thymeleaf-layout-dialect 3.3.0
- mybatis
- lombok
--------------
- modelmapper 3.1.1
- mapstruct 1.4.2
- commons-io 2.6
- PageMaker(paging처리 자체제작 lib)

<br/>

**작업 내용**
--

* ***admin(작업자 : 권능환)***
  * ****member(회원)****
    * 등록된 회원 목록 보기
    * 등록된 회원 role값 변경 (블랙리스트, 주의(블랙리스트 해제), 추방(탈퇴))
    * **특정 조건**(닉네임, 주소, 양육경력)에 따라 **회원 검색**
    * **check box**를 통해서 여러 회원을 동시에 블랙리스트 or 추방 시킬 수 있음
    
  
  * ****board(게시판)****
    * 하나의 board table로 group(notice, faq, qna)에 따라서 출력(모듈화)
    * group을 기준으로 게시글 번호는 **무조건 1번부터 마지막 번호까지 차례대로 출력**
      * 중간에 글을 삭제하더라도 기존 번호가 유지 되는게 아니라 정렬 됨
    *  group에 따라 **카테고리별로 출력**
      *  검색 또한 같은 group이여도 해당 카테고리에 맞는 결과값 출력
    *  **동일한 글에 대한 조회수**는 처음 1회를 제외 후 **일정 시간 지나야** 조회수 증가하게 설정
    *  현재 게시글에 해당 댓글이 총 몇개가 있는지 출력
    *  **권한에 따라 기능 구현** 조금 씩 다름
      *  **관리자**의 경우 **모든 글에 대한** 개별 **수정, 삭제**가 가능하며, select box를 이용해 다중 삭제도 동시에 처리 가능
      *  일반 회원은 **작성자와 로그인한 사람이 일치** 할 경우 개별 수정, 삭제 가능(게시글 및 댓글)
      *  블랙리스트와 로그인이 안되어 있을 시 글 쓰기, 삭제, 수정 불가
    *  게시글 작성시 **메인 카테고리에 맞게 세부 카테고리 출력** 및 글 등록 가능
    *  게시글 제목 일정 길이 넘어가면 ...으로 표시

- - - 
***pet(작업자 : 강원빈)***

***mypage(작업자 : 고성우)***

***login(작업자 : 손영우)***

***cs(작업자 : 박한산)***
# GaePan
