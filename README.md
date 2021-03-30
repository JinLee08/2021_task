#### 20201493_이진_소프트웨어과제
# GFM_extension
> 본 문서는 [GitHub Flavored Markdown Spec](https://github.github.com/gfm/#disallowed-raw-html-extension-)를 바탕으로 쓰여졌습니다.
## 표(Tables)

GFM에서는 **표**를 사용할 수 있다. 표는 ***하나의 header행, header행과 다른 data를 구분하는 구분자행 그리고 0개 이상의 행***들로 이루어진 **행과 열로 정리되어있는 데이터들**이다.  
> header 행의 경우 하이픈(-)으로 나누고, 파이프(|)로 각 열을 구분한다. 

예시1 - 기본 형태  

    | foo | bar |  
    | --- | --- |  
    | baz | bim |  
결과:  

 | foo | bar |  
 | --- | --- |  
 | baz | bim |  

예시2  

    | abc | defghi |
    :-: | -----------:
    bar | baz  
    
결과:  
| abc | defghi |
:-: | -----------:
bar | baz  

> 한 열의 길이가 일치 할 필요는 없지만 일치할 경우 읽기가 더 쉽다.
>> *셀의 너비는 일치하지 않아도 괜찮지만* ***heder row의 각 열에는 최소 3개의 하이픈(---)이 있어야 한다.***   

> 더 다양한 예시는 [Tables(extension)](https://github.github.com/gfm/#tables-extension-)을 참고하자  

---
## 작업 목록 항목(Task list items)
GFM은 **tasklist 확장기능을 사용할 수 있다.**  
작업 목록 항목은 **작업 목록 항목 표시와 한개 이상의 공백 문자 그리고 내용**으로 이루어져 있다.  
>작업 목록 항목 표시는 **선택적 띄어쓰기와 중괄호 안의 x(대소문자 구분 없음)** 로 이루어져 있다.
> - 표시란의 괄호 안이 공백이면[ ] checkbox에는 check가 되어 있지 않다.
> - 표시란의 괄호 안이 공백이 아니면[X] checkbox에는 check가 되어 있다.  

예시1 - 기본형태   


    - [ ] foo
    - [x] bar

결과 :   
- [ ] foo
- [x] bar

예시2(중첩되어 사용할 수 있다.)  

    - [x] foo  
      - [ ] bar  
      - [x] baz  
    - [ ] bim    

결과:  
- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim



---  
## 취소선(Strikethrough)  
GFM은 추가적 강조를 할 수 있는 **strikethrough 확장기능을 사용할 수 있다.**  
취소선을 사용하기 위해선 텍스트를 두 개의 물결표(~)로 묶어주면 된다.  
  
    ~~Hi~~ Hello, world!

결과: ~~Hi~~ Hello, world!

---  
## 자동링크(Autolinks) 

GFM은 **많은 조건들에서 autoliink를 인식하는 autolink 확장기능**을 사용할 수 있다.  
Autolink들은 *더 적은 상황에서 인식되긴 하지만* 그들을 구분하기 위해 요구되는 **꺽쇠괄호(< >)의 사용없이도 쓸 수 있다.**  
>- 그러한 모든 Autolink들은 **줄의 시작부분, 공백 뒤, 또는 구분문자(\*, \_, ~, ( )뒤에만 올 수 있다.**  

***www텍스트와 뒤에 유효한 도메인***이 발견되면 **extended www autolink**를 사용할 수 있다.
> 유효한 도메인은 숫자, 밑줄(\_) 및 하이픈 (-), 마침표(.)가 하나 이상 있어야하고 도메인의 마지막 두 세그먼트에는 밑줄이 없어야 한다.

예시 1
    
    www.commonmark.org
    
결과: www.commonmark.org  

예시2
    
    Visit www.commonmark.org/help for more information.
    
*유효한 도메인 뒤에 0또는 공백없는 <가 붙을 수 있다.*
> 그렇다면 우리는  extended autolink path validation 적용한다.
>> 후행구두점(?, !, ., ,, :, *, _, ~)은 autolink의 일부로 여겨지지 않는다.


> 더 다양한 예시는 [Autolinks(extension)](https://github.github.com/gfm/#autolinks-extension-)를 참고하자

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


----
추가적인 참고자료들 
> -[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)  
> -[Writing on Github](https://docs.github.com/en/github/writing-on-github)
