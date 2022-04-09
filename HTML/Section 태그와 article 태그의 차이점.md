### section

> section 태그는 섹션(부분, 구역, 영역) 들을 그룹화 해서 분리하는 역할을 한다.
>

### article

> article 태그는 문서내에서 그룹화해서 분리하는 역할을 한다.
>

article과 section 이 두 시맨틱 태그는 **div와 같은 블록 속성**을 가지고 있기 때문에 div로 대치해도 기능상으로 문제가 없고 **두 요소 다 콘텐츠를 구분하는 데 사용**되며 서로 바꿔서 사용 가능

### ****section article 차이****

**▷ article은 내용이 독립적이다.**

article 태그는 section과 다르게 독립적으로 존재할 수 있으며 재사용 할 수 있다.

즉 article이 좀 더 구체적이다.

주로 블로그글, 포럼, 뉴스 기사 등을 article로 묶음

**▷ section은 주제별로 구분한 그룹이다.**

논리적으로 관계있는 요소 또는 문서를 분리할 때 사용한다.

다른 주제의 문서를 구분 짓기위해 사용 (**주제별 영역들을 그룹화**)

※ 논리적인 관계가 없는 요소들을 그룹화 할 경우에는 div를 사용한다.

### ****section과 article 사용예시****

```html
<section>
  <h1>HOT TOPIC</h1>
  <section>
     <p>World</p>
     <article>World news 1</article>
     <article>World news 2</article>
     <article>World news 3</article>
  </section>
  <section>
    <p>Sport</p>
    <article>Sport news 1</article>
    <article>Sport news 2</article>
    <article>Sport news 3</article>
  </section>
</section>
```

section

```html
<section>
   <h1>상품소개</h1>
   <ul>
      <li>상품1</li>
      <li>상품2</li>
      <li>상품3</li>
   </ul>
   <p>상품의 실제이미지와 다를 수 있습니다.</p>
</section>
```

**article**

```html
<article>
   <h3>브랜드 페이스북</h3>
   <ul>
      <li>포스팅1</li>
      <li>포스팅2</li>
      <li>포스팅3</li>
   </ul>
</article>
```