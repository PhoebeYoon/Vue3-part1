# Vue3 Lesson 를 위해 

#### 속성
```html
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-list">
        <div class="container-fluid">
            <a href="#" class="navbar-brand">My Vue</a>
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li v-for="link in links" class="nav-item">
                    <a href="#" class="nav-link">{{ link.text }} </a> # 여기를 수정
                </li>
            </ul>
        </div>
    </nav>
    <div id="content" class="container">
        <h1>{{pageTitle}}</h1>
        <p>{{pageContent}}</p>
    </div>

    <script>
        Vue.createApp({
            data(){
                return {
                    links:[
                        {text:"Home", url:'home.html'},
                        {text:"About", url:"about.html"},
                        {text:'Contact',url:'contact.html'}
                    ]  #여기를 수정
                }
            }
        }).mount('nav');
        Vue.createApp(
            {
                data() {
                    return {
                        pageTitle:'Hello, Vue ',
                        pageContent : 'Welcome to wonderful world'
                    }
                }
            }
        ).mount('#content');
    </script>

```
(lesson05 에서 사용했던 예제를 가져와 수정한다).  
위의 내용이 작동되는지 확인한 후에 <a>태그 부분만 아래처럼 수정해보자.   
``` html 
<a href="{{link.url}}" class="nav-link">{{ link.text }} </a>
```
정상적으로 출력되는것처럼 보이지만 개발자도구를 보면,  <b>link.url </b>가 'home.html' 바뀌지 않은 것을 볼수있다.   
<img width="422" alt="스크린샷 2023-02-25 오후 1 50 01" src="https://user-images.githubusercontent.com/48478079/221338934-c9068610-92c4-4e1d-8fdd-615196b0aca1.png">

 ```html
  <a v-bind:href="link.url" class="nav-link">{{ link.text }} </a> 
  ``` 
 v-bind를 삽입하고 {{ }}는 빼고 v-bind:href="link.url" 수정하면 결과가 정상적으로 나온다. 어플리케이션에서 html속성을 사용하겠다는 의미로 <b>v-bind:</b>를 적고 속성을 적어준다. 그리고 <b>속성의 값은 자바스크립트표현식 </b>이 와야하기 때문에 {{ }} 는 없애준다.   
    
    
    
