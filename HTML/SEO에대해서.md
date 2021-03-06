> **SEO는 Search Engine Optimization의 약자로 말그대로 검색엔진 최적화라는 의미**
>

Google 및 야후 등이 높은 점유율을 보이는 나라 (일본, 미국, 홍콩 등)에서는 SEO 마케팅에 따른 효과가 엄청나기 때문에 아주 중요한 마케팅 전략 중 하나

- **Google 검색 작동 방식**

  Google은 '웹 크롤러'를 사용하는 자동화된 검색엔진으로 3단계로 작동한다.

    1. 크롤링
    2. 색인생성
    3. 검색결과 게재

  이 중에서 색인 생성 과정을 살펴보자.페이지의 콘텐츠를 분석하고 이미지, 동영상 파일의 목록을 작성 하는 등의 방법을 통해서 페이지를 파악하고 Google 색인에 저장한다.그렇다면 우리가 작성하는 HTML 코드가 검색결과에 영향을 미치는 것은 이 색인 과정일 것이다.

  또한 Google 검색센터에서는 게재 및 순위를 개선하고 최적화하는 방법에 대해서 여러페이지에 걸쳐 자세하게 언급하고 있다.

- **SEO에 영향을 미치는 것들**

  SEO에서 얘기 하는 것은 구글의 검색엔진이 찾을 수 있고, 이해할 수 있는 사이트를 만들라는 것이다. 그렇게 하기 위해서는 아래의 요건들을 체크해볼 필요가 있다.

    1. robots.txt
    2. 모바일 친화적인 페이지
    3. 적절한 `<meta>`태그 사용
    4. 사이트맵 파일을 제공한다.
    5. 명확한 계층구조가 포함되도록 설계한다.
    6. 유효한 HTML (Semantic Markup)을 사용할것.
    7. 이미지, 동영상, 구조화된 데이터에 관한 권장사항을 준수한다.
    8. 모든 페이지가 연결되어 있는지 확인한다.(href 속성이 포함된 `<a>`태그)
    9. `<title>`, `<alt>` 속성이 구체적이고 정확한지 확인한다.
    10. etc
- **1. robots.txt**

  웹 크롤러같은 로봇들의 접근을 제어하기 위한 규약

  robots.txt파일은 크롤러가 사이트에 요청할 수 있는 페이지/파일과 요청할 수 없는 페이지/파일을 검색엔진 크롤러에 알려 주는 역할을 한다.

- **2.모바일 친화적인 페이지**

  모바일 퍼스트 전략을 사용하여 개발한 웹 사이트는 그렇지 않은 사이트보다 빨리 로드될 것

- **3.적절한 `<meta>`태그 사용**
    - `keyword` : 웹페이지의 홍보수단으로 검색 키워드를 지정 가능하며, `,`로 구분하여 선언한다.

        ```html
        <meta name="keyword" content="HTML, tag, element, Frontend">
        ```

    - `subject` : 문서의 제목정보

        ```html
        <meta name="subject" content="HTML tag">
        ```

    - `description` : 웹페이지 요약 정보, 제작자 정보(autuor), 저작권 정보(copyright)

        ```html
        <meta name="description" content="HTML tag 정리">
        ```

    - `author` : 문서의 저작자

        ```html
        <meta name="author" content="Kim Kyuree">
        ```


    위의 `meta`tag는 검색결과에 노출되는 내용을 정의

- **4. 유효한 HTML (Semantic Markup)을 사용**

  올바르고(시맨틱) 오류가 없도록 HTML을 작성한다. HTML과 CSS를 제대로 사용한다면 콘텐츠와 디자인이 분리되므로 페이지를 더 빠르게 렌더링 및 로드할 수 있다

- **5. `<title>`, `<alt>` 속성이 구체적이고 정확한지 확인**