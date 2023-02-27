:cactus: Vue3 Lesson 


## v-model.lazy : 데이터 양방향 바인딩을 수행 하며, 텍스트 입력 완료 후 변경된 사항이 표시

```html
<div id="app">
  <input v-model.lazy="myText">
  <p>내용을 입력한 내용 표시「{{ myText }}」</p>
</div>
<script>
Vue.createApp({
data(){
  return { myText:''}
}
}).mount("#app")
</script>
```


## v-model.number
input 폼을 사용하여 입력값을 받는 경우 숫자 또는 문자 무엇을 입력해도 타입이 문자로 나타나게됩니다. 여기에 v-model.number를 사용하면 자동으로 숫자로 바꾸어줍니다. 
```html
<div id="app">
  <input v-model.number="myNumber" type="number">
  <p>100을 더해서 표시「{{ 100 + myNumber }}」</p>
</div>
<script>
Vue.createApp({
data(){
  return { myNumber:0,}
}
}).mount("#app")
</script>

```

## v-model.trim
trim 함수와 동일하게 입력값의 앞과 두의 공백을 제거해줍니다.
