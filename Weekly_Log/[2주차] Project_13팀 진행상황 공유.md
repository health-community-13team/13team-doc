# [2주차] Project_13팀 진행상황 공유

<aside>
✔️ 하단의 내용을 복사하여 .md 파일을 제작해주시길 바랍니다.

</aside>

## 팀 구성원, 개인 별 역할

---

- 개인 스터디 기간

## 팀 내부 회의 진행 회차 및 일자

---

2024.03.08 - 디스코드 (전원참석)

## 현재까지 개발 과정 요약 (최소 500자 이상)

---

### 심규대

# 3/4

### GetMapping, PostMapping 차이점

- GetMapping
    - 리소스 조회
    - 서버에 전달하고 싶은 데이터는 query(쿼리 파라미터, 쿼리스트링)를 통해 전달
    - 클라이언트가 서버에 메시지 보낼 때 사용
- PostMapping
    - 요청 데이터 처리
    - 메시지 바디를 통해 서버로 요청 데이터 전달
    - 주로 전달된 데이터로 신규 리소스 등록, 프로세스 처리에 사용

### JPA란

- 스프링 부트는 JPA(Java Persistence API)를 사용하여 데이터베이스를 관리. JPA는 인터페이스 모음으로, 인터페이스를 구현한 실제 클래스가 필요하다.
- JPA 리포지토리는 JpaRepository 인터페이스를 상속한다. JpaRepository는 JPA가 제공하는 인터페이스 중 하나로 CRUD 작업을 편리하게 처리할 수 있다. <>안에는 어떤 엔티티로 생성하는지, 엔티티의 기본키의 형식이 뭔지 넣는다.
- JPA 리포지토리는 메서드 명을 분석하여 쿼리를 만들고 실행하는 기능이 있다. 예를 들어 findBy + 엔티티의 속성명을 작성하면 입력한 속성의 값으로 데이터 조회가 가능하다.

### @Autowired

- 적용하고자 하는 변수에 Autowired를 적용하면 스프링 부트가 객체를 자동으로 만들어 주입한다. 객체를 주입하는 방식에는 Setter 메서드 또는 생성자를 사용하는 방식이 있는데, 개발 시 생성자를 통한 객체 주입을 권장한다. 그러나 테스트 코드는 JUnit이 생성자를 통한 객체 주입을 지원하지 않으므로 Autowired를 사용한다.

# 알고리즘

---

- 프로그래머스 중앙값 구하기

[](https://school.programmers.co.kr/learn/courses/30/lessons/120811?language=java)

- 풀이
    
    ```java
    import java.util.Arrays;
    
    class Solution {
        public int solution(int[] array) {
            Arrays.sort(array);
            int answer = array[array.length / 2];
            
            return answer;
        }
    }
    ```
    

# 3/5

# 프로그래머스 알고리즘

---

- 문제

[](https://school.programmers.co.kr/learn/courses/30/lessons/120822)

- 풀이
    
    ```java
    class Solution {
        public String solution(String my_string) {
            String answer = "";
            
            for(int i = my_string.length() - 1; i >= 0; i--) {
                answer += my_string.charAt(i);
            }
            
            return answer;
        }
    }
    ```
    

# 점프 투 스프링부트

---

### 2-4

- @Id : 기본키로 지정하는 애너테이션
- @GeneratedValue : 데이터를 저장할 때 해당 속성에 값을 일일이 입력하지 않아도 자동으로 1씩 증가하여 저장된다.
- @Column : 엔티티의 속성은 테이블의 열 이름과 일치하는데 세부 설정을 위해 사용한다. length는 열의 길이를 설정할 때 사용, columnDefinition은 열 데이터의 유형이나 성격을 정의할 때 사용

> 엔티티의 속성을 @Column 을 사용하지 않더라도 열로 인식한다. 테이블의 열로 인식하고 싶지 않다면 @Transient 를 사용한다. 엔티티의 속성을 테이블의 열로 만들지 않고 클래스의 속성으로만 사용하고자 할 때 사용.
> 
- @ManyToOne, OneToMany… : N:1, 1:N…, CascadeType.REMOVE란 질문에 삭제되면 질문의 답변들도 모두 삭제되도록 사용한다.

### 2-5

- 리포지터리는 생성된 데이터베이스 테이블의 데이터들을 저장, 조회, 수정, 삭제 등을 할 수 있도록 도와주는 인터페이스. 데이블에 접근하고 데이터를 관히하는 메서드를 제공
- JPA가 제공하는 인터페이스를 상속하여 CRUD 작업을 처리하는 메서드를 가져다 사용할 수 있다.
- assertEquals(기댓값, 실젯값)

[](https://school.programmers.co.kr/learn/courses/30/lessons/120822)

- 풀이
    
    ```java
    class Solution {
        public String solution(String my_string) {
            String answer = "";
            
            for(int i = my_string.length() - 1; i >= 0; i--) {
                answer += my_string.charAt(i);
            }
            
            return answer;
        }
    }
    ```
    

# 점프 투 스프링부트

---

### 2-4

- @Id : 기본키로 지정하는 애너테이션
- @GeneratedValue : 데이터를 저장할 때 해당 속성에 값을 일일이 입력하지 않아도 자동으로 1씩 증가하여 저장된다.
- @Column : 엔티티의 속성은 테이블의 열 이름과 일치하는데 세부 설정을 위해 사용한다. length는 열의 길이를 설정할 때 사용, columnDefinition은 열 데이터의 유형이나 성격을 정의할 때 사용

> 엔티티의 속성을 @Column 을 사용하지 않더라도 열로 인식한다. 테이블의 열로 인식하고 싶지 않다면 @Transient 를 사용한다. 엔티티의 속성을 테이블의 열로 만들지 않고 클래스의 속성으로만 사용하고자 할 때 사용.
> 
- @ManyToOne, OneToMany… : N:1, 1:N…, CascadeType.REMOVE란 질문에 삭제되면 질문의 답변들도 모두 삭제되도록 사용한다.

### 2-5

- 리포지터리는 생성된 데이터베이스 테이블의 데이터들을 저장, 조회, 수정, 삭제 등을 할 수 있도록 도와주는 인터페이스. 데이블에 접근하고 데이터를 관히하는 메서드를 제공
- JPA가 제공하는 인터페이스를 상속하여 CRUD 작업을 처리하는 메서드를 가져다 사용할 수 있다.
- assertEquals(기댓값, 실젯값)

# 3/6

# 점프 투 스프링 부트

---

### 2-5

findById 메서드는 기본으로 제공하지만 findBySubject 같은 메서드는 기본으로 제공하지 않는다. repogitory 클래스에 작성해줘야 한다.

| sbb% | 'sbb'로 시작하는 문자열 |
| --- | --- |
| %sbb | 'sbb'로 끝나는 문자열 |
| %sbb% | 'sbb'를 포함하는 문자열 |

# 알고리즘

---

[](https://school.programmers.co.kr/learn/courses/30/lessons/120809)

- 풀이
    
    class Solution {
    public int[] solution(int[] numbers) {
    int[] answer = new int[numbers.length];
    
    ```
        for(int i = 0; i < numbers.length; i++) {
            answer[i] = numbers[i] * 2;
        }
    
        return answer;
    }
    
    ```
    
    }
    
    ```java
    class Solution {
        public int[] solution(int[] numbers) {
            int[] answer = new int[numbers.length];
            
            for(int i = 0; i < numbers.length; i++) {
                answer[i] = numbers[i] * 2;
            }
            
            return answer;
        }
    }
    ```
    

# 3/7

# 점프 투 스프링부트

repository가 findById 메서드를 통해 Question 객체를 조회하고 나면 DB세선이 끊어진다.

> DB 세션이란 스프링 부트 애플리케이션과 데이터베이스 간의 연결을 뜻함.
> 

이러한 문제는 테스트 코드에서만 발생한다. @Transactional 을 사용하여 메서드가 종료될 때 까지 DB 세션을 유지할 수 있다.

매개변수로 Model을 지정하면 객체가 자동으로 생성된다.

@RequiredArgsConstructor는 final이 붙은 속성을 포함하는 생성자를 자동으로 만들어 주는 역할을 함. 따라서 스프링 부트가 내부적으로 QuestionController를 생성할 때 롬복으로 만들어진 생성자에 의해 questionRepository 객체가 자동으로 주입됨.

- optional
    - java8 이상부터는 Optional<T> 클래스를 사용해 NPE(NullPointerException)을 방지할 수 있다. 값이 null 이더라도 NPE가 발생하지 않는다.

# 알고리즘

[](https://school.programmers.co.kr/learn/courses/30/lessons/120836)

- 풀이
    
    class Solution {
    public int solution(int n) {
    int answer = 0;
    
    ```
        for(int i = 1; i <= n; i++) {
            if(n % i == 0) {
                answer++;
            }
        }
    
        return answer;
    }
    
    ```
    
    }
    
    ```java
    class Solution {
        public int solution(int n) {
            int answer = 0;
            
            for(int i = 1; i <= n; i++) {
                if(n % i == 0) {
                    answer++;
                }
            }
            
            return answer;
        }
    }
    ```
    

# 3/8

th:each="question : ${questionList}” 여기서 
th:는 타임리프에서 사용하는 속성. 자바코드와 연결되는 부분임

타임리프는 Model 객체에 저장한 questionList를 ${questionList}로 읽을 수 있다.

questionList에 저장된 데이터를 하나씩 꺼내 question 변수에 대입한 후 questionList의 개수만큼 반복하며 <tr>…<tr> 문장을 출력하라는 뜻의 아래 코드.

```html
<table>
    <thead>
        <tr>
            <th>제목</th>
            <th>작성일시</th>
        </tr>
    </thead>
    <tbody>
        <tr th:each="question : ${questionList}">
            <td th:text="${question.subject}"></td>
            <td th:text="${question.createDate}"></td>
        </tr>
    </tbody>
</table>
```

# 알고리즘

---

[](https://school.programmers.co.kr/learn/courses/30/lessons/120910)

- 풀이
    
    ```java
    class Solution {
        public int solution(int n, int t) {
            int answer = n;
            
            for(int i = 0; i < t; i++) {
                answer *= 2;
            }
            
            return answer;
        }
    }
    ```
    

### 김상민

1. Spring Boots
2. 세션, 쿠키, 캐시
3. JPA
4. JWT
5. Spring Security

### 류형수

점프 투 스프링부트를 처음 부터 다시 공부하였다.

1. 스프링 부트 구조
2. ORM과 JPA 이해하기
3. H2 데이터베이스
4. 엔티티 속성 구성하기
5. 예외 처리

### 배현준

### 개인 스터디 진행

1. 리플렉션
2. 제너릭
3. 예외처리
4. 어노테이션
5. 멀티 스레드
6. 람다
7. 스프링 IoC

### 이재윤

### 🔎 MVC 패턴과 JPA, 영속성에 대해서 간단한 개념 정리 진행.

### 🔎 점프투스프링부트 2-01부터 2-13까지 복습 진행 과정

- H2 데이터베이스 생성
- 엔티티 클래스로 DB테이블 만들기
- JPA 메서드 이용해보기
- 자바 파일을 패키지 별로 분류하기
- 타임리프문 적용
- 루트 URL 설정
- Controller, Service, Repository, Entity 클래스로 기능 구분하기
- 예외처리 적용
- 답변 등록기능과 답변 목록 구현해보기
- style.css 적용

### 황인욱

### 스터디

점프 투 스프링부트를 공부하면서 기본 개념들이 생각이 나지 않아 검색하는 시간이 많아졌다

그래서 점프 투 스프링부트 공부를 하면서 몰랐던 java 기초에 대해 공부하였다

- java 코드의 구조
- 메서드
- 변수 - 자료형
- while문 /  for문
- 클래스

## 개발 과정에서 나왔던 질문 (최소 200자 이상)

---

### 심규대

Q : tr, th, td 태그의 의미에 대해 궁금합니다.

A :

- tr : table row, 표의 행을 나타냄. 각 행은 하나 이상의 열을 포함
- th : table header cell, 표의 열 또는 행의 헤더를 나타냄. 일반적으로 표의 첫 번째 행이나 첫 번째 열에 사용되고, 보통 굵은 글씨체로 표시되고 가운데 정렬된다.
- td : table data cell, 표의 일반적인 데이터를 포함하는 셀을 나타냄. 각 셀은 하나의 데이터 값을 가짐.

---

### 김상민

- 인증, 인가에 관한 분류 및 구현 단계에서 오는 실무적인 문제
- 구현 하기 위해서 낮은 단계의 아키텍쳐의 원활한 구현이 필요해 보임.
- 네트워크와 데이터 베이스의 CS 로직의 방법의 다양화하여 필요한 상황에 맞출 수 있는 방법 찾기

### 류형수

**DBMS란?**

DBMS(database management system)란 데이터베이스를 관리하는 소프트웨어이다. DB와 DBMS를 구분하지 않고 사용하는 경우가 많은데, 엄밀히 말해 DB는 데이터를 담은 통이라 할 수 있고, DBMS는 이 통을 관리하는 소프트웨어이다.

### **JPA란?**

스프링 부트는 JPA(Java Persistence API)를 사용하여 데이터베이스를 관리한다. 스프링 부트는 JPA를 ORM(Object-Relational Mapping) 기술의 표준으로 사용한다. JPA는 인터페이스 모음이므로, 이 인터페이스를 구현한 실제 클래스가 필요하다. JPA를 구현한 실제 클래스에는 대표적으로 하이버네이트(Hibernate)가 있다. 정리하자면, 하이버네이트는 JPA의 인터페이스를 구현한 실제 클래스이자 자바의 ORM 프레임워크로, 스프링 부트에서 데이터베이스를 관리하기 쉽게 도와준다. 우리가 계속 만들어 갈 SBB도 JPA와 하이버네이트 조합으로 데이터베이스를 관리한다.

### 배현준

### 스프링 IOC 컨테이너 작동 방식

1. **설정 로딩:** 스프링 IOC 컨테이너가 애플리케이션의 구성 정보를 읽어오기 위해 설정 파일을 로딩한다. 보통 XML 파일, 자바 어노테이션 또는 자바 기반의 설정 클래스로 작성된다.
2. **빈의 생성:** 설정 파일에 정의된 빈(Bean)들을 컨테이너가 생성한다. 이때 빈은 주로 클래스의 인스턴스로 생성되며, 설정 파일에서 빈의 스코프(scope)를 지정할 수 있다. 기본적으로 싱글톤(Singleton)이 사용된다.
3. **의존성 해결:** 컨테이너는 설정 파일에서 정의된 빈들 간의 의존 관계를 해결한다. 주로 생성자 주입, setter 주입, 필드 주입 등의 방식으로 의존성 주입이 이루어진다.
4. **빈의 생명주기 관리:** 컨테이너는 빈의 생명주기를 관리한다. 빈의 초기화(init)와 소멸(destroy) 메서드를 호출하여 객체의 생명주기를 관리한다. 이러한 라이프사이클 콜백은 컨테이너가 빈을 생성하고 소멸할 때 호출된다.
5. **빈의 검색 및 제공:** 컨테이너는 빈의 식별자를 통해 빈을 검색하고 제공한다. 다른 빈이 해당 빈을 필요로 할 때 컨테이너는 해당 빈을 주입하여 의존성을 해결한다.

### 이재윤

### 📢 ORM이란 무엇인가?

> 💡 ORM(Object-Relational Mapping)
> 
> - 객체와 관계형 데이터 베이스의 데이터를 매핑하여 ‘객체 지향적인 코드’를 작성 가능하게 하는 기술을 의미한다.
> - ORM을 사용하면 개발자는 SQL 쿼리를 직접 작성하는 대신, 자바 객체를 사용하여 데이터베이스의 레코드를 쉽게 생성, 조회, 수정, 삭제할 수 있습니다. 이로 인해 개발 과정이 단순화되고, 코드의 가독성이 향상된다.
> - 또한, 데이터베이스와 애플리케이션 코드 간의 중간 계층 역할을 하여, 데이터베이스의 구조가 변경되더라도 애플리케이션 코드를 수정하지 않아도 된다. 이는 유지보수 과정을 간소화시키며, 개발 효율성을 높일 수 있다.

### 황인욱

공부하면서 검색했던 내용을 요약

- 유효성 체크(validation check) : 유효성 검사는 데이터가 서버 혹은 데이터베이스로 옮겨지기 전, 개발자가 만든 조건에 부합하는지 확인, 검증하는 작업을 말한다.
프론트, 백엔드(서비스)에서 한번씩
- 체크박스 : 말 그대로 체크 (체크 있으면 true, 없으면 false)
체크를 필수로 하려면 @NotEmpty가 아니라 @NotNull을 사용한다
- return - 값을 반환 or {}안의 명령 끝내기
- <div/div> 안에 있는 내용을 보여주기 싫으면 th:if를 넣는다 - 가장 바깥쪽 div에 넣어주면 됨
- 타임리프에서 그전 속성을 기억하는게 field이다
- security는 security config(설정)에서 설정
- @bean : 처음 만들어놓고 쓰든안쓰든 대기상태로 해놓다가 필요할때 가져다쓴다
    
    빈(bean)은 스프링에 의해 생성 또는 관리되는 객체를 의미한다. 우리가 지금껏 만들어 왔던 컨트롤러, 서비스, 리포지터리 등도 모두 빈에 해당한다. 또한 앞선 예처럼 @Bean 애너테이션을 통해 자바 코드 내에서 별도로 빈을 정의하고 등록할 수도 있다.
    

@Bean
SecurityFilterChain filterChain(HttpSecurity http) throws Exception {  // filterChain 입력받은 외부 주소창 관리

http
.authorizeHttpRequests((authorizeHttpRequests) -> authorizeHttpRequests
.requestMatchers(new AntPathRequestMatcher("/**")).permitAll())
-> 처음 화면에서 로그인없이 원하는 페이지로 갈수있게 해준다

**의 의미 : 뭐가 오든 상관없다

## 개발 결과물 공유

---

Github Repository URL: https://github.com/health-community-13team/health-community.git

- 필수) 팀원들과 함께 찍은 인증샷(온라인 만남시 스크린 캡쳐)도 함께 업로드 해주세요 🙂
  ![image](https://github.com/health-community-13team/13team-doc/assets/148305917/e7104b04-4e88-4433-8f76-e90106f735cf)
