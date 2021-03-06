# opensource-report

기간 : 2020.07.10(금) ~ 2020.07.17(금)

학습주제 IoT

------------------------------------------------------------------
2020.07.10(금) 요약

    오픈소스의 미래유망
    
    Rlottie : 웹 페이지 디자인
    
    NNstreamer : 포즈를 학습하여 이용자의 상황 파악
    
------------------------------------------------------------------
2020-07-13

개발 환경 구축
- chocolately
- node.js
- react
- IDE(vscode)
- proxy server(NginX)

------------------------------------------------------------------
2020-07-14

프로젝트 아이디어 기획

 프로젝트명 : 꿀잠
 
 컨셉 : 수면 패턴 교정 웹사이트

개발 환경 구축
- vue.js
- spring
- apache tomcat 8.5

------------------------------------------------------------------
2020-07-14

프로젝트 아이디어 기획 및 논의
- 수면 패면 교정 웹사이트
- 블랙박스를 통한 교통법규 위반 신고
- 자세 교정 플랫폼

React 학습 필요
- 스켈레톤 프로젝트 기반

------------------------------------------------------------------
2020-07-16

프로젝트 아이디어 확정
- 블랙박스를 통한 교통법규 자동 신고 웹 사이트
- 카메라 센서, 버튼 센서 또는 터치 센서 등 필요
- 위치 기반의 서비스

웹 디자인 연구
- 기술 스택 : React -> Vue (확정)
- 로그인 기능 개발
- Vue 템플릿 수정

이슈
- 프론트 엔드 개발 스택 선정(완료)
- 차량과 웹의 통신 방법 논의 필요

기타
- 확정 주제에 대한 와이어프레임 작성

------------------------------------------------------------------
2020-07-17

웹 사이트 UI/UX 구현
- 로그인 기능 모달 창으로 구현
- Navbar, Sidebar에서 필요한 컴포넌트를 선별하고, 그렇지 않은 것들을 제거
- 메인 페이지에 보여줄 요소들을 선정

------------------------------------------------------------------
2020-07-20

웹 백엔드 서버 개발 환경 구축
- Spring 개발 환경
- MySQL 개발 환경
- Spring Project와 Git 연동하여 Team Share
- 브랜치명 규칙
- 기본 스프링
- Spring 기본 개발 프레임 세팅

------------------------------------------------------------------
2020-07-21

웹 백엔드 서버 개발 - 로그인
- 회원 테이블 설계
- User SQL 작성
- Repository 제작
- Service 제작
- Controller 제작

Front-End 와 Back-End 연동
- 로그인 데이터 서버로 전송

------------------------------------------------------------------
2020-07-22

웹 백엔드 서버 개발 - 회원 관리
- 회원 가입
- 회원 정보 수정
- 회원 탈퇴
- 회원 조회
- 프런트엔드와 연결 및 테스트

기타
- Git Merge Conflict 발생 => 해결 X
- 대안 : Branch 초기화 후 재사용
- 
------------------------------------------------------------------
2020-07-23

보안 이슈 방안 정리
- JWT Token으로 회원 인증
- 네이버 로그인

AWS 배포 성공(학습 필요)
Open Api 학습 (Naver 검색)

------------------------------------------------------------------
2020-07-24

네이버 아이디로 로그인 기능 구현 중
프로필 파싱까지 완료

이슈)

Session에 토큰 값이 중간에 사라짐
=> 원인 파악 후 해결할 것

------------------------------------------------------------------
2020-07-27

네이버 아이디 로그인 => 재작성
프로필 파싱 및 로그인 성공

이슈)
로그아웃 : 토큰 삭제 후 Redirect => URL QueryString에 토큰 존재
                                 => 재로그인 (해결 중..)
                                 
------------------------------------------------------------------
2020-07-28

- 네이버 로그아웃 해결 못함
- 네이버 로그인 코드 리팩토링
- 로컬에서 MP4 동영상 파일 입출력
- 회원가입 코드 수정(이메일 중복 불가능)

------------------------------------------------------------------
2020-07-29

네이버 로그인
- JWT를 이용하여 토큰 암호화 처리
- 로그아웃 해결
- 코드 리팩토링
- 네이버 회원 데이터 관리 필요

신고 기능 구축
- 신고 테이블 설계
- 데이터 CRUD 구현
- Repository 마무리 작업 필요

------------------------------------------------------------------
2020-07-30

신고 기능 구축
- Repository 마무리 완료
- CRUD 테스트 필요

네이버 로그인
- 로그아웃 코드 수정
- 작은 이슈 (로그아웃 시 토큰 삭제)
- 소셜 회원 테이블 모델링
- 네이버 로그인 시 회원 정보 DB에 저장 기능 필요

테이블 간 관계 설계
- 자체 회원, SNS 회원, 신고 테이블 관계 설정 방법 고안 필요
- 2개의 회원 테이블을 한번에 신고 테이블에 관계를 설정할 수 있다면 베스틑
- 자체 회원 - 신고 / SNS 회원 - 신고

------------------------------------------------------------------
2020-08-03

SNS User 데이터 관리 기능
- SNS User Table Modeling
- SNS Violation Table Modeling
- SNS User - SNS Violation Relationship Setting
- SNS User Repository
- SNS User Service, ServiceImpl
- SNS Domain
- SNS User SQL Statement 작성(SNSUser.xml)

Swagger UI 적용
- UserController
- ViolationController
- SNSUserController

------------------------------------------------------------------
2020-08-04

로그인 기능 추가 수정 및 보완

회원 신고 기능 추가 수정 및 보완

신고 현황 테이블 모델링
- Situation Teble
- no, date, accident, report, handling

SNS 유저의 신고 기능 만들기
- SNS Violation Controller
- SNS Violation Service, ServiceImpl
- SNS Violation Repository
