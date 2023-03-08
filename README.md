# Vue3 Lesson 를 위한 용어 예습
- 템플릿 ( template ) : 어떤 제품을 만들때 사용되는 '틀'입니다. 매번 반복되는 이미지나 구조를 템플릿(틀)으로 저장해 놓고, 그 안에 바뀌는 부분과 바뀌지 않는 부분이 존재하는데 바뀌는 부분만 수정하여 사용하면되는 것으로 생각하시면 됩니다.

- 프레임워크 (Framework) : 어플리션 개발을 위해 필요한 기본적인 클래스와 라이브러리등이 모두 포함되어 있는 환경
- 바인딩(Binding) 이란 컴퓨터 프로그래밍에서 각종 값들이 확정되어 더 이상 변경할 수 없는 구속(Bind) 상태가 되는 것. 프로그램 내에서 변수, 배열, 라벨, 절차 등의 명칭, 즉, 식별자(identifier)가 그 대상인 메모리 주소, 데이터형 또는 실제 값으로 배정되는 것이 이에 해당된다.원시 프로그램의 컴파일링 또는 링크 시에 확정되는 바인딩을 정적 바인딩(static binding)이라 하고, 프로그램이 실행되는 과정에서 바인딩 되는 것을 동적 바인딩(dynamic binding)이라고 한다.   
- 마운팅 ( mount, mouted, mouting )컴포넌트, 템플릿, 렌더링 된 DOM에 접근할 수 있다.

-  rendering : 화면에 표시할 내용을 만드는 과정으로 웹브라우저는 우리가 어떤 사이트를 방문하거나 웹페이지를 바꿀때마다 렌더링이라는 절차를 거쳐서 우리에게 해당 페이지를 보여주는 것이다. 렌더링과정에는 DOM를 생성하고 csssom를 결합하여 렌더링 트리라는 것을 형성합니다. 그리고 각 노드의 위치와 크기를 계산하고 노드를 화면에 그립니다 (이것을 페인팅 또는 래스터화라고 한다). 사용자의 요구에 의해 위치와 내용이 바뀌면 리플로우, 리페인트가 발생합니다.  
* 렌더링 메카리즘 : Vue는 어떻게 템플릿을 가져와 실제 DOM 노드로 변환할까, Vue는 이러한 DOM 노드를 어떻게 효율적으로 업데이트합니까? 여기서는 Vue의 내부 렌더링 메커니즘을 살펴봐야 합니다.  
* Vue의 렌더링 시스템은 '가상 DOM'이라는 것을 기반으로 한다. 가상 DOM은 메모리에 내용을 갖고 있다가 실제 DOM에 동기화하는 프로그램 기법이다.

-  Updating : 상태 변화로 인한 렌더링
- Destruction : 소멸
- new Vue로 선언하여 만들어진 객체를 vue 인스턴스라고 한다
- el : element의 약자로 어떤 html요소에 Vue객체를 연결한다. 태그에 지정한 ID, 클래스명, 태그명으로 해당 태그와 vue 인스턴스를 연결 
- data: { Vue 객체에서 사용할 데이터들을 정의한다. 대부분 'key-value' 형식의 JSON 형태로, 여러 개를 동시에 명시할 수 있다.}
- methods:{ Vue 객체에서 사용할 함수들을 명시한다. data와 마찬가지로 여러 개의 함수를 동시에 명시할 수 있다.}
- {{ mustache }} :Vue객체에서 정의된 데이터나 함수뿐 아니라 자바스크립트 문법도 적용하여 할 수 있는 있는 템플릿엔진이다. 이름은 콧수염모양처럼 보인다고 해서 지어진 것이다. 
- computed : getter/setter를 지정하는 옵션


- Router(라우터) :[컴퓨터] 라우터(네트워크에서 데이터의 전달을 촉진하는 중계 장치) 
-  vs code > file > preference > User snippets, 검색창에서 vue 엔터 > vue 선택
 ``` {
  "snippets 이름": {
    "prefix": "snippets 실행 트리거",
    "body": [
      // snippets 실행시 원하는 template 작성
    ],
    "description": "snippets에대한 설명을 작성합니다."
  }
}
```
