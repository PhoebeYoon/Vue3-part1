:cactus: Vue3 Lesson 

## radio 버튼

```html
<div id="app">
  <input type="radio" value="red"   v-model="colors">빨강
  <input type="radio" value="blue"  v-model="colors">파랑
  <input type="radio" value="green" v-model="colors">초록
  <p>선택하신 색상은 {{ colors }} 입니다</p>
</div>
<script>
Vue.createApp({
data(){
  return { colors:'red' }
}
}).mount("#app")
```   
여기서 html에서 폼태그의 내용 작동방법을 상기시켜보자. 색상3개는 마치 하나짜리 구성으로 red, blue, green이 따로 작동하는 것이 아니라, 3개중 1개만 선택하게 만들기위해 name 속서에 같은 이름을 준다. 그래야    
red를 선택하면 blue, green이 선택되지 않고,   
blue를 선택하면 선택되어 있던 red가 자동으로 해제되어  
green를 선택하면 blue, red가 모두 해제된 상태가 된다.   
이것이 일반 html에서의 작동방법일 것이다. 하지만 vue에서는 name 속성을 지정하지 않았지만 3개 중 1개만 유일하게 선택되어진다는 것을 알수있다. 여러개의 라디오버튼에 v-model="같은 프로퍼티명"를 지정하면 이렇게 작동된다.  

## radio 버튼으로 이미지를 바꿔보자 (컵케이크 또는 피자 뭘 먹을까 )
```html
<div id="app">
  <input type="radio" v-model="fileName" value='./img/cupcake.png'>컵케이크
  <input type="radio" v-model="fileName" value='./img/pizza.png'> 피자 
<p> <img v-bind:src="fileName" > </p>
</div>
<script>
Vue.createApp({
data(){
  return { fileName:''}
}
}).mount("#app")
</script>
```

## select 문
```html
<div id="app">
  <select v-model="selectColor">
    <option value="" >원하는 색을 선택하세요</option>
    <option value="red">Red</option>
    <option value="blue">Blue</option>
    <option value="green">Green</option>
  </select>
  <p v-bind:style="{ backgroundColor: selectColor }">선택하신 색상은 {{ selectColor}}입니다</p>
</div>
<script>
Vue.createApp({
data(){
  return {  selectColor:''}
}
}).mount("#app")
```

#### :coffee: 여기서 잠깐
> 이제까지의 설명으로 '{{ }}'는 알겠는데, ``` <p v-bind:style="{ backgroundColor: selectColor } ~ ``` 에서 갑자기 나오는 { } 하나짜리는 뭐지? 하실분이 있을 듯해서 짧게 설명드릴께요. { }는 객체표현에 사용되는거죠. 자바스크립트하셨으면 기억나실거예요.

