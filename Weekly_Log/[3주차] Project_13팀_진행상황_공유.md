# [3주차] Project_13팀 진행상황 공유

<aside>
✔️ 하단의 내용을 복사하여 .md 파일을 제작해주시길 바랍니다.

</aside>

## 팀 구성원, 개인 별 역할

---

- 개인 스터디 기간

## 팀 내부 회의 진행 회차 및 일자

---

2024.03.15 - 디스코드 (전원참석)

## 현재까지 개발 과정 요약 (최소 500자 이상)

---

### 심규대

- 배포를 위한 aws 공부
- 테라폼 공부
- 타임리프 문법 공부
- 스프링부트 service, dto 공부
- 알고리즘 풀이

### 김상민

- Oauth 2.0 공부
- 카카오 맵 공부
- REST API 공부
- 코딩테스트 알고리즘 공부

### 류형수

점프 투 스프링부트 3장 공부

강사님 강의 자료로 공부

프론트엔드 프레임워크와 스프링부트의 OAUTH2를 이용한 소셜 로그인

### 배현준

### 이재윤

### 🔎 점프투스프링부트 복습 진행 과정

- 부트스트랩 적용
- 타임리프 템플릿 상속으로 표준 HTML 구조 적용
- 질문 등록과 공백 처리, 오류 처리, 폼 클래스 작성, 오류 처리 공동 템플릿 적용
- 내비게이션바 적용
- 페이징 기능 추가
- 게시물 번호 내림차순 적용
- 답변 개수 표시 적용
- 스프링 시큐리티 적용
- 회원가입 기능 구현
- 로그인, 로그아웃 기능 구현
- 글쓴이 항목 추가

### 황인욱

- Spring Security 공부
- properties, yml 공부
- 생성자 관련 공부
- 로그인 인증 구현 방식 공부
    - Session
    - JWT
    - OAUTH2
- 인터페이스 공부

## 개발 과정에서 나왔던 질문 (최소 200자 이상)

---

### 심규대

Q : 배포에 aws와 ncp 어느 것을 사용하는 것이 좋을까요?

A : ncp를 사용하면 성능 좋을 서버를 사용할 수 있지만 aws가 사용하기 더 편하다

---

Q : DTO란?

A : Data Transfer Object의 약자로 프로세스간에 데이터를 전달하는 객체를 의미. DTO를 사용하지 않으면 보안에 취약할 수 있고, DTO를 사용함으로 엔티티 내부 구현을 캡슐화도 가능.

### 김상민

- 카카오 맵 구현 및 사용을 위한 프론트 스택이 필요하다고 느낌.
- 리액트, 타임스크립트 공부가 필요함.

### 류형수

paging 객체의 속성

paging.isEmpty : 페이지 존재 여부를 의미한다(게시물이 있으면 false, 없으면 true).
paging.totalElements : 전체 게시물 개수를 의미한다.
paging.totalPages : 전체 페이지 개수를 의미한다.
paging.size : 페이지당 보여 줄 게시물 개수를 의미한다.
paging.number : 현재 페이지 번호를 의미한다.
paging.hasPrevious : 이전 페이지의 존재 여부를 의미한다.
paging.hasNext : 다음 페이지의 존재 여부를 의미한다.

주요 페이징 기능을 표로 정리
th:classappend="${!paging.hasPrevious} ? 'disabled'" : 이전 페이지가 없으면 '이전' 링크를 비활성화한다.
th:classappend="${!paging.hasNext} ? 'disabled'" : 다음 페이지가 없으면 '다음' 링크를 비활성화한다.
th:href="@{|?page=${paging.number-1}|}" : 이전 페이지 링크를 생성한다.
th:href="@{|?page=${paging.number+1}|}" : 다음 페이지 링크를 생성한다.
th:each="page: ${#numbers.sequence(0, paging.totalPages-1)}" : 0부터 전체 페이지 수 만큼 이 요소를 반복하여 생성한다. 이때 현재 순번을 page 변수에 대입한다.
th:classappend="${page == paging.number} ? 'active'" : 반복 구간 내에서 해당 페이지가 현재 페이지와 같은 경우 active 클래스를 적용한다.

```
paging.hasPrevious
```

---

| paging.isEmpty | 페이지 존재 여부를 의미한다(게시물이 있으면 false, 없으면 true). |
| --- | --- |

| paging.isEmpty | 페이지 존재 여부를 의미한다(게시물이 있으면 false, 없으면 true). |
| --- | --- |
| paging.totalElements | 전체 게시물 개수를 의미한다. |
| paging.totalPages | 전체 페이지 개수를 의미한다. |
| paging.size | 페이지당 보여 줄 게시물 개수를 의미한다. |
| paging.number | 현재 페이지 번호를 의미한다. |
| paging.hasPrevious | 이전 페이지의 존재 여부를 의미한다. |
| paging.hasNext | 다음 페이지의 존재 여부를 의미한다. |

### 배현준

### 이재윤

> 
> 

### 황인욱

th- if : 안에 조건이 참이냐 거짓이냐에 따라 엘리먼트를 보여주냐 안보여주냐 결정함

dependency : 의존성 주입

maven : 부품 가지고 오는애

check box : 복수선택 가능
radio box : 한개만 선택 가능
select box : 밑에 줄 생겨서 선택하는거 -셀렉트박스 : 공통코드

@PathVariable : 경로 변수를 표시하기 위해 메서드에 매개변수에 사용된다. 경로 변수는 중괄호 {id}로 둘러싸인 값을 나타낸다. URL 경로에서 변수 값을 추출하여 매개변수에 할당한다. - 주소창에 던질때 반드시 필요

throw : 안에는 return이 있다

form 태그 : th:action으로 넘겨주는 url이 필요하다

html / css / javascript

jpa는 update와 save를 같이씀
jpa리포지터리가 기본적으로 가지고 있기 때문에

Create => insert => save
Read => select => findById, findAll
Update => update => save
Delete => delete => delete

(+)가 있으면 레프트 조인이다

ID 기반의 엔티티 관리: JPA는 엔티티의 ID를 기반으로 해당 엔티티가 새로운 것인지, 이미 데이터베이스에 있는 것인지를 판단합니다. 만약 엔티티가 이미 데이터베이스에 존재한다면 (id가 존재하고, 관리 상태(managed state)에 있다면), save 메소드는 기존 엔티티를 업데이트합니다.

단순성과 일관성: save 메소드는 새 엔티티를 생성하고 기존 엔티티를 업데이트하는 데 모두 사용될 수 있습니다. 이는 API를 간단하고 일관되게 유지하는 데 도움이 됩니다. 별도의 update 메소드를 제공하지 않음으로써, 개발자는 언제 save를 사용해야 하는지, 언제 update를 사용해야 하는지에 대해 혼란스러워할 필요가 없습니다.

변경 감지(Dirty Checking): JPA는 '변경 감지' 메커니즘을 사용하여, 트랜잭션 내에서 엔티티의 속성이 변경되었는지 감지하고, 변경 사항이 있을 경우 자동으로 데이터베이스에 반영합니다. 이 메커니즘 덕분에, 개발자는 엔티티의 상태를 변경하기만 하면 되고, 나머지는 JPA가 처리합니다.

트랜잭션 관리: save 호출은 트랜잭션의 일부로 수행됩니다. 이는 데이터의 일관성과 무결성을 보장하는 데 중요합니다. modify 메소드가 트랜잭션 내에서 실행되고 있다면, 변경 사항은 트랜잭션이 성공적으로 완료되었을 때만 최종적으로 커밋됩니다.

프레임워크와의 일관성: 대부분의 ORM 프레임워크는 이와 유사한 접근 방식을 채택하고 있습니다. 따라서, JPA와 같은 프레임워크를 사용하면, 다른 프레임워크로 전환하는 학습 곡선이 완만해질 수 있습니다.

요약하자면, save 메소드를 사용하여 엔티티를 업데이트하는 것은 JPA의 기본 동작 방식을 따르며, API를 단순화하고, 개발자가 직접 업데이트 로직을 관리할 필요가 없도록 해줍니다. 이러한 접근 방식은 개발 과정을 간소화하고, 데이터 무결성을 유지하는 데 도움이 됩니다.

## 개발 결과물 공유

---

Github Repository URL: https://github.com/health-community-13team/health-community.git

- 필수) 팀원들과 함께 찍은 인증샷(온라인 만남시 스크린 캡쳐)도 함께 업로드 해주세요 🙂
![image](https://github.com/health-community-13team/13team-doc/assets/148305917/a0b91bdc-6ad0-499d-b8b3-6347e4fc92b5)

