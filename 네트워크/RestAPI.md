# REST API란?

REST 아키텍처를 기반으로 서비스 API를 구현한 것

## REST API의 탄생 배경

- 2000년도에 로이 필딩의 박사학위 논문에서 최초로 소개되었다.
- HTTP의 주요 저자 중 한사람으로 웹(HTTP) 설계의 우수성에 비해 제대로 사용되지 못하는 모습이 안타까워 장점을 최대한 활용할 수 있는 아키텍처로 REST를 발표했다.

## REST

- Representational State Transfer의 약자로 웹사이트의 컨텐츠(TEXT, 이미지, 동영상 등), DB의 내용 들을 전부 하나의 자원으로 파악해 각 자원의 고유한 URI를 부여하고,  HTTP Method를 통해 해당 자원에 대한 CRUD작업을 하는 것을 의미한다.
- 구성 요소
    - 자원(Resource) : URI
        - 모든 자원은 고유한 ID가 존재하며, 이 자원들은 Server에 존재한다.
        - 자원을 구별하는 ID는 ‘/user/:user_id’와 같은 HTTP URI이다.
            - > ex) “https://www.acmicpc.net/user/cheon4050”
        - Client는 URI를 이용해 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청할 수 있다.
    - 행위(Verb): HTTP Method
        - HTTP 프로토콜의 Method를 사용해 CRUD 작업을 한다.
        - CRUD - 기능(Method)
            - Create - 생성 (POST)
            - Read - 조회(GET)
            - Update - 수정(PUT)
            - Delete - 삭제(DELETE)
    - 표현(Representation of Resource):
        - Client가 자원의 상태(정보)에 대한 조작을 요청하면 Server는 이에 맞는 적절한 응답(Representation)을 보낸다.
        - REST에서 자원은 JSON, XML과 같은 형태의 응답(Representation)으로 나타내어 질 수 있다.
        - JSON 혹은 XML을 통해 데이터를 주고받는 것이 일반적이다.

## REST가 필요한 이유

- 애플리케이션 분리 및 통합
    - MSA(Micro service architecture)를 사용하는 기업이 많아지는데,  이 서버, 클라이언트들 간의 통신을 할 때 유용하기 때문.
- WEB브라우저 외의 클라이언트를 사용할 수 있다. (멀티 플랫폼)
    - 기존에는 웹에서는 웹 페이지를 위한 HTML 및 이미지를 서버에서 보냈기 때문에 데이터가 무겁고 모바일 어플리케이션에서는 html을 호환할 수 있는 브라우저가 모두 존재하지 않았기 때문에 모두 사용할 수 없었다.
    - 그래서 rest api를 사용해 데이터만을 주고받게 되면 여러 클라이언트가 부담 없이 자유롭게 데이터를 사용할 수 있다.

## REST의 특징

1. Uniform(일관된 인터페이스)

   URI로 지정한 자원에 대한 조작을 통일되고 한정적인 인터페이스로 수행할 수 있다.

    - 특정 언어나 기술에 종속받지 않는다.
    - 플랫폼(Android, Ios)에 무관하다.
2. Cachable(캐시 가능)

   기존 웹 표준인 HTTP프로토콜을 그대로 사용하기 때문에 웹에서 사용하는 인프라를 그대로 활용이 가능하다. 그래서 그 기능 중 하나인 캐싱 기능을 사용할 수 있다.

3. stateless(무상태성)

   불필요한 정보(세션 정보, 쿠키)를 별도로 저장하고 관리하지 않기 때문에 서버는 들어오는 요청만을 단순 처리하면 된다. 이 때문에 서비스의 자유도가 높아지고 구현이 단순해 진다.

    - 이전 요청과 현재의 요청이 관계 없음 → 현재 요청만 처리하면 되기 떄문에 구현이 단순해짐
4. Self-descriptiveness(자체 표현 구조)

   REST API의 이름을 붙이는 것은 자유이기 때문에 이해하기 쉬운 이름을 붙이면 REST API 메세지만을 보고도 이를 쉽게 이해할 수 있다.

5. Client - Server 구조

   자원이 있는 쪽은 Server, 자원을 요청하는 쪽은 Client로 구분이 가능하다.

    - 각자의 역할이 명확해 진다.
    - 서로간의 의존성이 줄어든다.
6. 계층형 구조

   서버와 클라이언트를 연결하는 중간 서버(로드 밸런싱, 공유 캐시 등)를 추가할 수 있어 시스템 규모 확장성이 향상되고, 구조를 유연하게 설계할 수 있다.


## REST API

REST 기반으로 서비스 API를 구현한 것이다.

- API: 컴퓨터 프로그램 간의 상호작용을 통해 서로 정보를 교환 가능하도록  하는 것.

### REST API 특징

- REST를 기반으로 만들어졌기 때문에 시스템을 분산해 확장성과 재사용성이 높다.→ 유지보수 및 운용을 편리하게 할 수 있다.
- 프로그래밍 언어가 HTTP를 지원한다면 자유롭게 언어를 선택해 클라이언트, 서버를 구현할 수 있다.

### REST API 설계 기본 규칙

REST에서 가장 중요하며 기본적인 규칙

1. URI는 정보의 자원을 표현해야 한다. → 명확한 이해가 가능하게 지어야 한다.
2. 자원에 대한 요청은 HTTP Method(GET, POST, PUT, DELETE)로 표현한다. → URI에 메서드와 같은 기능을 나타내는 단어는 사용하지 않는다.

   > ex) **GET /members/show/1 → GET /members/1**

   > ex) **GET /members/insert/2 → POST /members/2**


### REST API 설계 세부 규칙

1. 슬래시 구분자(/)는 계층 관계를 나타내는데 사용한다.

   ex ) **https://www.smu.ac.kr/lounge/notice/notice.do**

2. URI 마지막 문자로 슬래시(/)를 포함하지 않는다.
    - 슬래시 계층을 구분하기 위한 것으로, 마지막에는 사용하지 않는다.

   > ex) http://restapi.example.com/users/ (x)

   > ex) http://restapi.example.com/users (o)

3. 하이픈(-)은 URI 가독성을 높이는데 사용
    - 너무 긴 URI경로를 사용하게 될 경우 하이픈을 사용해 가독성을 높인다.
4. 밑줄(_)은 URI에서 사용하지 않는다.
    - 밑줄은 잘 보이지 않아 보기 어렵기 때문에 가독성을 위해 사용하지 않는다.
5. URI경로에는 소문자가 적합하다.
6. 파일 확장자는 URI에 포함하지 않는다.

   ex) http://restapi.example.com/members/soccer/345/photo.jpg (X)

   GET / members/soccer/345/photo  |

   Header HTTP/1.1 Host: restapi.example.com  Accept: image/jpg (O)


## RESTful

RESTful이란 일반적으로 REST 아키텍처를 잘 준수하고 있는 REST API를 얘기한다.

- REST API를 제공하는 웹 서비스를 ‘RESTful’하다고 할 수 있다.
- REST를 REST답게 쓰기 위한 방법으로, 누군가 공식적으로 발표한 것은 아니다.

### RESTful의 목적

- 이해하기 쉽고 사용하기 쉬운 REST API를 만드는 것이다.
- RESTful한 API를 구현하는 근본적인 목적은 성능향상이 아닌 API의 이해도 및 호환성을 높이는 것이 주된 이유이다.

## 참고 자료

---

- [https://meetup.toast.com/posts/92](https://meetup.toast.com/posts/92)
- [https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html](https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html)
- [https://www.redhat.com/ko/topics/api/what-is-a-rest-api](https://www.redhat.com/ko/topics/api/what-is-a-rest-api)