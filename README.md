#### 20201493_이진_소프트웨어과제
# GFM_extension
> 본 문서는 [GitHub Flavored Markdown Spec](https://github.github.com/gfm/#disallowed-raw-html-extension-)를 바탕으로 쓰여졌습니다.
## 표(Tables) - 길음

GFM에서는 표를 사용할 수 있다. 표는 하나의 header행, header행과 다른 data를 구분하는 구분자행 그리고 0개 이상의 행들로 이루어진 행과 열로 정리되어있는 데이터들이다.  

  \| foo | bar |  
  \| --- | --- |  
  \| baz | bim |  
  

---
## (Task list items)


---  
## 취소선(Strikethrough)  
GFM은 추가적 강조를 할 수 있는 **strikethrough 확장기능을 사용할 수 있다.**  
취소선을 사용하기 위해선 텍스트를 두 개의 물결표(~)로 묶어주면 된다.  
  
    ~~Hi~~ Hello, world!

결과: ~~Hi~~ Hello, world!

---  
## 자동링크(Autolinks) - 길음

GFM은 **많은 조건들에서 autoliink를 인식하는 autolink 확장기능**을 사용할 수 있다.  
Autolink들은 *더 적은 상황에서 인식되긴 하지만* 그들을 구분하기 위해 요구되는 **꺽쇠괄호(< >)의 사용없이도 쓸 수 있다.**  
\- 그러한 모든 Autolink들은 **줄의 시작부분, 공백 뒤, 또는 구분문자(\*, \_, ~, ( )뒤에만 올 수 있다.**
***www텍스트와 뒤에 유효한 도메인***이 발견되면 **extended www autolink**를 사용할 수 있다.
> 유효한 도메인은 숫자, 밑줄(\_) 및 하이픈 (-), 마침표(.)가 하나 이상 있어야하고 도메인의 마지막 두 세그먼트에는 밑줄이 없어야 한다.


---
## 허용되지 않은 원시 HTML(Disallowed Raw HTML)

GFM은 **HTML 출력을 렌더링할 때에 다음의 HTML 태그들이 걸러지는 tagfilter 확장기능**을 사용할 수 있다.

- <title>
- <textarea>
- <style>
- <xmp>
- <iframe>
- <noembed>
- <noframes>
- <script>
- <plaintext>

이 태그는 특히 HTML이 고유한 방식으로 해석되는 방식을 변경하기 때문에 선택된다.  
***필터링은 <을 \&lt; 로 대체하며 진행된다.***  
다른 HTML 태그들은 변경되지 않고 그대로 남아있는다.
