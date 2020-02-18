# REST-API
# Goal
- REST의 개념을 이해한다.
- REST의 특징을 이해한다.
- REST API의 개념을 이해한다.
- REST API의 설계  규칙을 이해한다.
- RESTfull의 개념을 이해한다.


# REST의 개념 
![image](https://user-images.githubusercontent.com/34269126/74712605-090bca00-526a-11ea-9036-ee85287e8c86.png)


# REST란
- REST 정의
  - “Representational State Transfer” 의 약자
    - 자원을 이름(자원의 표현)으로 구분하여 해당 자원의 상태(정보)를 주고받는 모든것을 의미한다.
    - 즉, 자원(resource)의 표현(representation)에 의한 상태 전달.
        - 자원의 표현
            - 자원: 해당 소프트웨어가 관리하는 모든것   →  ex.문서,그림,데이터, 해당 소프트웨어 자체
            - 자원의 표현: 그 자원을 표현하기 위한 이름 →  ex.DB의 학생 정보가 자원일때, 'students'를    자원의 표현으로 정한다. 
        - 상태(정보) 전달 
            - 데이터가 요청 되어지는 시점에서 자원이 상태(정보(를 전달한다.
            - JSON 혹은 XML를 통해 데이터를 주고 받는것이 일반적이다.
        - 월드 와이드 웹(www)과 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 개발 아키텍처의 한 형식
            - REST는 기본적으로 웹의 기존 기술 과 HTTP 프로토콜을 그대로 활용하기 떄문에 웹의 장점을 최대한 활용할수 있는 아키텍처 스타일이다.


- REST의 구체적인 개념
    - HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.
        - 즉, REST는 자원 기반의 구조(ROA, Resource Oriented Architecture) 설계의 중심에 Resource가 있고 HTTP Method를 통해 Resource를 처리하도록 설계된 아키텍쳐를 의미한다.
        - 웹 사이트의 이미지, 텍스트, DB 내용 등의 모든 자원에 고유한 ID인 HTTP URI를 부여한다.
        - CRUD Operation
            - Create : 생성(POST)
            - Read : 조회(GET)
            - Update : 수정(PUT)
            - Delete : 삭제(DELETE)
            - HEAD: header 정보 조회(HEAD)


- REST의 장단점
    - 장점 
        - HTTP 프로토콜의 인프라를 그대로 사용하므로 REST API 사용을 위한 별도의 인프라를 구출할 필요가 없다.
        - HTTP 프로토콜의 표준을 최대한 활용하여 여러 추가적인 장점을 함께 가져갈수 있게 해준다.
        - HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다.
        - REST API 메시지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악할 수 있다.
        - 여러가지 서비스 디자인에서 생길 수 있는 문제를 최소화한다.
        - 서버 와 클라이언트의 역할을 명확하게 분리한다.
    - 단점
        - 표준이 존재하지 않는다.
        - 사용 할수 있는 메소드가 4가지 밖에 없다.
        - HTTP Method 형태가 제한적이다


-   REST가 필요한 이유
    -  ' Application 분리 및 통합 '
    -  ' 다양한 클라이언트의 등장 '
    - 최근의 서버 프로그램은 다양한 브라우저와 안드로이폰,아이폰 과 같은 모바일 디바이스에서도 통신을 할수 있어야 한다.


-   REST 구성 요소 
    -   자원(Resource): URI
        - 모든 자원에 고유한 ID가 존재하고, 이 자원은 Server에 존재한다
        - 자원을 구별하는 ID는 '/groups/:group_id' 와 같은 HTTP URI다.
        - Client는 URI를 이용해서 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청한다. 


-   행위(Verb): HTTP Method
    -  HTTP 프로토콜의 Method를 사용한다.
    -  HTTP 프로토콜은 GET, POST, PUT, DELETE 와 같은 메서드를 제공한다.

- 표현(Representataion of Resource)
    - Client가 자원의 상태(정보)에 대한 조작을 요청하면 Server는 이에 적절한 응답(Representation)을 보낸다.
    - REST에서 하나의 자원은 JSON, XML, TEXT, RSS 등 여러 형태의 Representation으로 나타내어 질 수 있다.
    - JSON 혹은 XML를 통해 데이터를 주고 받는 것이 일반적이다.



# REST API란 
-   API(Application Programming Interface)란
    - 데이터 와 기능의 집합을 제공하여  컴퓨터 프로그램 간 상호자용을 촉진하며, 서로 정보를 교환가능 하도록 하는것 
-   REST API 정의
    - REST 기반의 서비스를 API로 구현한것
    - REST API란 REST 아키텍처 스타일을 지키는 API를 말합니다. REST 아키텍처는 클라이언트와 서버간의 독립적인 개발을 진행할 수 있는 아키텍처 스타일입니다. 서버와 클라이언트의 데이터는 HTTP 프로토콜 위에서 데이터를 주고받으며 REST 아키텍처 스타일에서 명시하는 조건을 준수하여 해야 합니다.



-   REST API의 특징
    -   사내 시스템들도 REST 기반으로 시스템을 분산해 확장성 과 재사용성을 높여 유지보수 및 운용을 편리하게     할수 있다.
    -   REST HTTP 표준을 기반으로 구현하므로, HTTP를 지원하는 프로그램 언어로 클라이언트, 서버를 구현할수     있다.
    -   즉, REST API를 제작하면  자바 ,C#,웹 등을 이용해 클라이언트를 제작할수 있다.


-   REST API 설계 기본 규칙
    -   참고 리소스 원형
        -   도큐먼트: 객체 인스턴스나 데이터베이스 레코드와 유사한 개념
        -   컬렉션: 서버에서 관리하는 디렉터리라는 리소스
        -   스토어: 클라이언트에서 관리하는 리소스 저장소
-   URI는 정보의 자원을 표현해야 한다.
    -   resource는 동사보다 명사를, 대문자보다는 소문자를 사용한다.
    -   resource의 도큐먼트 이름으로는 단수 명사를 사용해야 한다.
    -   resource의 컬렉션 이름으로는 복수 명사를 사용해야 한다.
    -   resource의 스토어 이름으로는 복수 명사를 사용해야 한다.
        -       EX) GET/Member/1  → GET/Members/1
-   자원에 대한 행위는 HTTP Method(GET, PUT, POST, DELETE 등)로 표현한다.
    -   자원에 대한 행위는 HTTP Method(GET, PUT, POST, DELETE 등)로 표현한다.
        -       Ex) GET /members/delete/1 -> DELETE /members/1
    -   URI에 행위에 대한 동사 표현이 들어가면 안된다.(즉, CRUD 기능을 나타내는 것은 URI에 사용하지 않는다.)
        -       Ex) GET /members/show/1 -> GET /members/1
        -       Ex) GET /members/insert/2 -> POST /members/2
-   경로 부분 중 변하는 부분은 유일한 값으로 대체한다.(즉, :id는 하나의 특정 resource를 나타내는 고유값이다.)
    -       Ex) student를 생성하는 route: POST /students
    -       Ex) id=12인 student를 삭제하는 route: DELETE /students/12


-   REST API 설계 규칙
    - 슬래시 구분자(/ )는 계층 관계를 나타내는데 사용한다.
        -       Ex) http://restapi.example.com/houses/apartments

-   URI 마지막 문자로 슬래시(/ )를 포함하지 않는다.
    -   URI에 포함되는 모든 글자는 리소스의 유일한 식별자로 사용되어야 하며 URI가 다르다는 것은 리소스가   -   다르다는 것이고, 역으로 리소스가 다르면 URI도 달라져야 한다.
    -   REST API는 분명한 URI를 만들어 통신을 해야 하기 때문에 혼동을 주지 않도록 URI 경로의 마지막에는        슬래시(/)를 사용하지 않는다.
        -       Ex) http://restapi.example.com/houses/apartments/ (X)

-   하이픈( - ) 은 URI 가독성을 높이는데 사용
    -   불가피하게 긴 URI경로를 사용하게 된다면 하이픈을 사용해 가독성을 높인다.

-   밑줄(_)은 URI에 사용하지 않는다.
    -   밑줄은 보기 어렵거나 밑줄 때문에 문자가 가려지기도 하므로 가독성을 위해 밑줄은 사용하지 않는다.
-   URI 경로에는 소문자가 적합하다.
    -   URI 경로에 대문자 사용은 피하도록 한다.
    -   RFC 3986(URI 문법 형식)은 URI 스키마 와 호스트를 제외하고는 대소문자를 구별하도록 규정하기             떄문이다.
-   파일 확장자는 URI에 포함하지 않는다.
    -   REST API에서는 메시지 바디 내용의 포맷을나타내기 위한 파일 확장자를 URI 안에 포함시키지 않는다.
        Accept header를 사용한다
        -       Ex) http://restapi.example.com/members/soccer/345/photo.jpg (X)
        -       Ex) GET / members/soccer/345/photo HTTP/1.1 Host:
                restapi.example.com Accept: image/jpg (O)
-   리소스 간에는 연관 관계가 있는 경우
    -   /리소스명/리소스ID/관계가 있는 다른 리소스명
        -       Ex) GET: /users{userid}/devices(일반적으로 소유 'has'의 관계를 표현할때)


-   REST API 설계 예시
![image](https://user-images.githubusercontent.com/34269126/74713897-cf888e00-526c-11ea-95b0-35c67e562d2d.png)

-   참고 응답상태코드
    -   1xx : 전송 프로토콜 수준의 정보 교환
    -   2xx : 클라어인트 요청이 성공적으로 수행됨
    -   3xx : 클라이언트는 요청을 완료하기 위해 추가적인 행동을 취해야 함
    -   4xx : 클라이언트의 잘못된 요청
    -   5xx : 서버쪽 오류로 인한 상태코드



# RESRful의 개념

-   RESTful이란
    -   RESTful은 일반적으로 REST라는 아키텍처를 구현하는 웹  서비스를 나타내기 위해 사용되는 용어이다.
        -   'REST API'를 제공하는 웹 서비스를 'RESTful 하다고 할수있다 
    -   RESTful은 REST를 REST 답게 쓰기 위한 방법으로,누군가가 공식적으로 발표한 것이 아니다.
        -   즉,REST 원리를 따르는 시스템은 RESTful이란 용어로 지칭된다.


-   RESTful의 목적
    -   이해하기 쉽고 사용하기 쉬운 REST API를 만드는것
    -   RESTful한 API를 구현하는 근본적인 목적이 성능 향상에 있는 것이 아니라 일관적인 컨벤션을 통한 API의    이해도 및 호환성을 높이는 것이 주 동기이니, 성능이 중요한 상황에서는 굳이 RESTful한 API를 구현할       필요는 없다.

-   RESTful 하지 못한 경우
    -       Ex1) CRUD 기능을 모두 POST로만 처리하는 API
    -       Ex2) route에 resource, id 외의 정보가 들어가는 경우(/students/updateName)
