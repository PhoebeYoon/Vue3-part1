## Vue란 무엇인가  

1. Vue란 

뷰(Vue)는 사용자 인터페이스를 구축하기 위한 자바스크립트 프레임워크이다. 표준 html, css, javascript를 기반으로 구축되며 사용자 인터페이스를 효율적으로 개발할 수 있도록 도와주는 __선언적이고(declarative)__  __구성요소(Component)__ 기반의 프로그래밍 __모델(model)__ 을 제공한다. vue의 공식문서에는 이렇게 뷰를 설명하고 있다. 
이것을 영어로 보면 보다 명확하다.

```
Vue (pronounced /vjuː/, like view) is a JavaScript framework for building 
user interfaces.
It builds on top of standard HTML, CSS, and JavaScript and provides 
a declarative and component-based programming model that helps you 
efficiently develop user interfaces, be they simple or complex.
```


> <b>선언적</b> -  여기서 선언적이라는 것은 선언적 랜더링을 한다는 의미로, 이것은 뷰가 자바스크립트를 기반으로 hmtl 문서를 출력할때 템플릿 구문을  사용한다는 뜻이다. ```템플릿이란 워드프로세서에서 사용된 용어인데, 이미 일부 세부정보가 있는 샘플문서를 말한다. ```   
그러니 여기서 우리는 Vue가 뭔가를 미리 만들어놓고 그것을 마치 정해진 양식처럼 가져와 사용한다는 것을 짐작할 수 있다   

><b>구성요소</b> - '뷰의 구성요소' 로 구글에서 검색을 하면 많은 내용이 나오지만 읽어봐도 무슨 소리인지, 그걸 이해하려면 또 다시 다른 단어를 검색해야 하고... 이것은 설명을 못해서가 아니라, 한마디로 정의하기가 어렵고 여러요소들이 복잡적으로 작동하기 때문일것이다.  
그래서 일단 <u>뷰(view)</u> 와 <u> 뷰(Vue) </u>를 구분하고,   
- 뷰(view) : 앱안에 들어가는 각 화면의 구성요소를 말하는 것이고   
- 구성요소를 영어로 'component'로 사용해서 헷갈리지 않게 정리하자. 그럼 구성요소란 component(컴포넌트)라는 것을 사용한다는 의미이다 

><b>모델</b> -  이 단어 또한 검색해도 정확한 검색이 되지 않는듯 보인다. 그래서 영어로 검색 (What is a model in vue ) 라고 하면 ``` Vue v-model is a directive that creates a two-way data binding between a value in our template and a value in our data properties``` 이라고 나온다. 즉 Vue v-model은 템플릿의 값과 데이터 속성의 값 사이에 양방향 데이터 바인딩을 생성하는 지침이다 뭐 이런 뜻이다 그럼 우리는 모델이라는 것은 v-model이라는 것과 깊은 관련이 있다는 정도로 이해하자.   

여기서 좀더 검색을 해보면  

<img width="530" alt="스크린샷 2023-02-24 오후 1 10 26" src="https://user-images.githubusercontent.com/48478079/221089832-9f117c4d-03c3-41b7-9913-400e706107d2.png">   

*출처:https://wikidocs.net/17701*
 
이런 이미지를 찾을 수 있다 이걸 보면 조금 더 이해가 되는듯하다  해당 문서에는 컴포넌트를 이렇게 설명한다   
```  컴포넌트는 화면에 비춰지는 뷰의 단위를 쪼개어 재활용이 가능한 형태로 관리하는 것, Vue은 재사용이 가능한 컴포넌트로 웹페이지를 구성할 수 있다  ```   


2. Vue.js는 '데이터와 뷰(view) 를 연결해 주는 역할'로 설명해 보자   
- 위의 이미지를 이렇게도 해석해 볼수 있다. 여기서의 모델(model)를 <U>Vue 안에 들어가는 데이터로</U> View를 <U> html에서 표시되는 요소</U>로 그리고 중간에 ViewModel이라는 것이 있다. 

