#Spring Framework

###프레임워크
프로그래밍에서 특정 운영 체제를 위한 응용 프로그램 표준 구조를 구현하는 클래스와 라이브러리 모임.
틀(뼈대)이 어느 정도 정해져 있어 수정이나 업데이트가 빠르고 코드도 비교적 이해하기 쉽고
처음부터 만드는 것보다 시간을 아낄 수 있는 장점이 있다. 

###스프링
자바 기반의 엔터프라이즈급 애플리케이션 개발에 필요로 하는 경량형 프레임워크
객체의 생성 및 소멸을 스프링이 직접 관리하고 스프링 컨테이너에서 필요한 객체를 가져와 작동

###엔터프라이즈급 애플리케이션
수많은 데이터처리와 트랜잭션등이 동시에 여러 사용자로부터 행해지는 매우 큰 규모의 애플리케이션

###컨테이너
인스턴스의 생성 및 소멸을 관리하고 추가적인 기능제공

###클래스/객체/인스턴스
객체의 설계도/소프트웨어에 구현할 대상/소프트웨어에 구현된(생성된) 실체

###IOC(제어의 역전)
스프링은 오브젝트의 생성과 의존관계 설정, 사용, 제거 작업을 개발자가 아닌 스프링 컨테이너가 담당

###DI(의존성 주입) @@@
DI 는 스프링에서 IoC 구조를 만드는 방식
객체간의 의존성을 줄이기 위해 밖에서 객체를 생성해 넣어줘서 재사용성이 늘어나고 수정이 쉬움

###Spring Bean
스프링 컨테이너가 관리하고 필요한 곳에 주입해주는 객체들을 Bean이라고 함

###JAVA Bean
데이터 전달을 위해 사용되는 자바 객체이다. private 변수와 getter/setter 만을 가지고있는
직렬화 가능한 객체이다

###JDBC
자바에서 DB 프로그래밍을 하기위해 사용되는 API

###MVC(Model, View, Controller)
사용자 인터페이스와 비즈니스 로직을 분리하여 개발 가능하여
서로의 영향을 최소화해 개발 및 수정이 쉽게 제작 가능한 디자인패턴.
(화면과 데이터처리를 분리)


###Servlet
클라이언트의 요처을 처리하고 그결과를 반환하는 Servlet 클래스의 구현 규칙을 지킨 자바 웹프로그래밍 기술임
MVC 패턴에서 컨트롤러로 이용되고 자바의 스레드를 이용하여 동작함 html 변경시 Servlet을 재 컴파일 해야하는
단점이 있따

###Was
웹서버와 웹컨테이너의 결합으로 다양한 기능을 컨테이너에 구현하여 여러 역할을 수행할 수 있는 서버
web서버는 html 문서같은 정척컨텐츠를 처리 was 서버는 asp, php, jsp 등 개발언어를 읽고 동적컨텐츠
및 응용 프로그램 서비스 처리

###웹컨테이너
클라이언트의 요청이 있을 때 내부의 프로그램을 통해 결과를 만들어내고 클라이언트에게 전달해주는 역할

#Spring Boot
(xml 파일 설정대신 @만 적절하게 명시해주면 자동으로 적용)

메인클래스에 붙어있는 @SpringBootApplication은
@SpringBootConfiguration
@ComponentScan – 
(컴포넌트 어노테이션을 가진 Bean 스캔 후 등록(Repository, @Service, @Controller, @RestController 포함)  
(@EnableAutoConfiguration – Bean을 등록하는 설정파일)
위에 것들이 합쳐진 거라고 생각하면 됨

스프링 프레임워크를 기반으로 바로 실행가능한 애플리케이션을 쉽게 만들도록 도와주는 프레임워크
스프링의 많은 부분을 자동화(web.xml, rootContext.xml,ServletContext.xml 등)
톰캣 내장 war파일로 패키징안하고 jar파일로 패키징해서 실행할 수 있음

###jar / war
어플리케이션을 쉽게 배포하고 동작시킬 수 있도록 관련 파일 패키징
jar – 자바프로젝트를 압축한 파일 jre만 가지고도 실행 가능함
war – 웹 어플리케이션 압축 파일포맷 웹 관련 자원만 포함, 웹 어플리케이션을 쉽게 배포
       실행하려면 톰캣 등 웹서버 또는 웹 컨테이너가 필요함

###보안
SQL 인젝션, XSS, CSRF, 클릭재킹과 같은 보안 공격을 기본으로 막아 준다.
- SQL 인젝션은 악의적인 SQL을 주입하여 공격하는 방법이다.
- XSS는 자바스크립트를 삽입해 공격하는 방법이다.
- CSRF는 위조된 요청을 보내는 공격 방법이다.
- 클릭재킹은 사용자의 의도하지 않은 클릭을 유도하는 공격 방법이다.

#Maven
수많은 라이브러리등을 관리해주는 도구로 라이브러리들과 연관된 라이브러리들까지 관리됨
pom.xml 기능
-프로젝트 정보 : 프로젝트의 이름, 라이센스 등
-빌드 설정 : 소스, 리소스, 라이프사이클별 실행한 플로그인 등 빌드와 관련된 설정
-빌드 환경 : 사용자 환경 별로 달라질 수 있는 프로파일 정보
-pom 연관 정보 : 의존 프로젝트(모듈), 상위 프로젝트, 포함하고 있는 하위 모듈 등

pom.xml
<project> 태그 안에 전부 기술
<modelVersion>POM 모델 버전
<groupid>프로젝트를 만들 때 입력했던 그룹 ID. 회사 단체등 식별
<artifactid>프로젝트에 할당한 고유 id로 프로젝트명(라이브러리명)
<version>프로그램(라이브러리) 버전
<dependencies> 안에 <dependency>를 사용하여 다운 받을 의존 라이브러리 코드 작성 

#Gradle
-빌드 속도가 Maven에 비해 월등히 빠르다
-Ant Builder와 Groovy 스크립트 기반으로 만들어져 Ant의 역할과 배포 스크립트 기능 모두 사용 가능


#Spring Scheduler
일정한 시간간격 또는 일정한 시각에 특정 로직을 돌리기 위해 사용
별도의 추가적인 의존성이 필요하지 않고 스프링부트에 제공됨
@SpringBootApplication 어노테이션이 붙은 곳에다가
@EnableScheduling 추가하면 사용 가능

스케줄을 적용할 메소드에 @Scheduled 작성하면 적용됨
적용할 메소드는 void 타입을 가져야하고 파리미터를 가질 수 없다.

기본적으로 한 개의 thread를 사용하고 동기형식으로 진행됨. 비동기형식으로 진행하고 싶으면
@EnableAsync 찾아보기

@Scheduled 옵션
-fixedDelay 이전작업이 종료된 후 설정 시간만큼 기다린 후 시작
-fixedRate 이전작업이 종료되지 않아도 설정된 시간마다 시작한다.
-initialDelay 작업 시작 시, 설정된 시간만큼 기다린 후 시작
-cron 원하는 시간대를 설정하여 작업 실행 (cron=“초 분 시간 일 월 요일”)
-zone 시간대를 설정한다. 미설정시 로컬 시간대 적용(cron이랑 사용)

Spring Quartz
스케줄러에 Clustering 기능이나 스케줄러 실패(에러 혹은 사용할 thread가 없는 경우)시 후처리 기능 추가가능

Lombok
getter setter toString 등 중복되는 메서드들의 코드를 줄여주는 라이브러리로
어노테이션을 추가하는 방식으로 작성하고 컴파일 과정에서 이를 생성해주는 방식으로 동작함
가독성 및 유지보수성을 향상시킬 수 있다.

주의
api설명과 내부동작을 어느정도 숙지해야함 예시로 @Data 어노테이션이나 @ToString 어노테이션으로
자동 생성된 ToString()메서드는 순환 참조 또는 무한 재귀 호출 문제로 StackOverflowError가 발생가능
롬복내에서 해결할 수 있는 속성은 있음

-순환참조 : A클래스가 B클래스의 Bean을 주입받고 B클래스가 A클래스의 Bean을 주입받는상황처럼
서로 순환되어 참고하는 경우
-무한 재귀 호출 : 자기자신을 호출하는 함수가 무한히 반복되는 것

어노테이션 종류
클래스 이름위에 적용하면 모든변수에 적용, 변수위에 적용하면 해당변수만 적용
@Getter 
@Setter
@ToString – 출력을 원하지 않는 변수에 @ToString.Exclude 추가로 제외가능
@AllArgsConstructor – 모든 변수를 사용하는 생성자 만들기
@NoArgsConstructor – 변수를 사용하지 않는 생성자 만들기
@RequiredArgsConstructor – 특정변수만 활용하는 생성자. 활용할 변수위에 @NonNull 추가 혹은 final 선언
@EqualsAndHashCode – equals 함수와 hashCode 함수 생성 특정변수가 같다면 동일객체로 인식설정 가능
@Data – 아래 다섯가지 포함
 -@ToString
 -@EqualsAndHashCode
 -@Getter
 -@Setter
 -@RequiredArgsConstructor
 실무에서는 무겁고 객체의 안정성을 지키기 위해 잘 활용하지는 않음
@Builder – 클래스의 객체 생성에 builder 패턴을 적용해 준다. 특정 변수만 build 하기 원한다면 생성자를 작성하고 그위에 붙여주면 된다.
@Delegate – 한 객체의 메소드를 다른 객체로 위임시켜 준다.
@Log4j2 – 해당 클래스의 로그 클래스를 자동완성

사용 
롬복 자르 파일을 cmd에서 실행후 설치
maven 프로젝트의 경우 pom.xml에 아래 의존성 추가 후 메이븐 업데이트 프로젝트
(pom.xml 안열리면 open with 다른걸로)

<dependency>
	<groupId>org.projectlombok</groupId>
	<artifactId>lombok</artifactId>
	<optional>true</optional>
</dependency>

Gson
GSON은 구글에서 만든 자바 오브젝트 직렬화/역직렬화 라이브러리다.
자바객체를 JSON으로 JSON을 자바객체로 변환할 때 사용
디펜던시에 추가해서 사용

직렬화
객체를 전송 가능한 형태로 만드는 것을 의미함. 객체의 데이터를 연속적인 데이터로 변형함
Serializable 인터페이스를 implements해서 사용

Oracle과 MySql 차이점
Oracle
DB서버가 통합된 하나의 스토리지 공유
중첩 루프 조인, 해시 조인, 소트 머지 조인
별도 DBMS 사용불가
수백메가바이트 설치

MySql
DB서버마다 독립적인 스토리지 할당
중첩 루프 조인
별도DBMS 사용가능
1메가바이트 환경에도 설치가능

스토리지
컴퓨터가 접근할 수 있는 데이터를 저장하기 위한 별도의 장소 또는 장치

중첩 루프 조인
한 집합의 원소 값을 다른 집합의 원소값과 매칭해 나가는 방법
(가능한 모든 경우를 조회)

소트 머지 조인
한집합과 다른 집합을 합하기 위해서 양쪽 다 정렬이 되어 있어야만 비교가능.
소트 머지의 경우 대등하게 합병되기 때문에 선행 또는 후행 테이블이 존제하지 않음

해시 조인
해시를 사용하는 경우는 해당 조인 키가 정렬되어있지 않고, 인덱스도 존제하지 않으면서
비교할 대상은 많을 때 사용

문법차이(오라클 / mysql)
------------------------------------------------------------------------------------
NULL 대체
-NVL(열명, ‘대체값’) / IFNULL(열밍, ‘대체값’)
SELECT 결과 개수 제한(페이징처리)
-ROWNUM <= 숫자 / LIMIT 시작위치, 가져올 데이터 건수
가상테이블 DUAL * 함수에 대한 쓰임을 알고 싶을때 특정 테이블을 생성할 필요없이 dual 테이블 사용
-SELECT 1 FROM　DUAL; / SELECT 1;
현재날짜
-SELEC SYSDATE FROM DUAL; / SELECT NOW();
조건식
-SELECT DECODE(칼럼, 값, TRUE일 때, FALSE일 때) FROM TABLE; 
/ SELECT IFNULL(조건식, TRUE일 때, FALSE일 때) FROM TABLE;
날짜형식
SELECT TO_CHAR(SYSDATE, 'YYYY-MM-DD') FROM DUAL;
/SELECT DATE_FORMAT(NOW(), '%Y-%m-%d');
시퀀스
시퀸스 사용법도 다르니 사용할 때 찾아보고 쓰자
MYSQL은 INSERT 시 값이 자동 생성되어 들어감
문자열 자르기
SELECT SUBSTR( 문자열/칼럼, 시작위치, 잘라낼 문자열의 길이) FROM DUAL;
/SELECT SUBSTRING(문자열/칼럼, 시작위치, 잘라낼 문자열의 길이);
------------------------------------------------------------------------------------

AWS


