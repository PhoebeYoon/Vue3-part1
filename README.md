:cactus: Vue3 Lesson 

## v-on 디렉티브 : 이벤트와 연결

```
<p v-on:이벤트="메소드이름"> </p>
메소드는 인스턴스안에 methods 옵션을 통해 추가하면 됩니다 
```
### v-on:이벤트명 과 @이벤트명은 동일하다
```
<a v-on:click="do">
<a @click="do"> (v-on은 생략할 수 있고 v-on 대신 @ 을 사용합니다 )
```

```html
<h2> v-on 디렉티브</h2>
<div id="app">
  <p>{{ count }}</p>
  <button v-on:click="increase">Increase</button>
</div>
<script>
Vue.createApp({
data(){ 
      return { count:1} 
  },
methods:{
  increase:function(){
    //  console.log('test')
    this.count++ // count앞에 this를 붙여줘야 합니다
   } }
}).mount('#app')
</script>
```
methods에서 data 에 선언된 변수를 가져와 사용하려면 this 키워드를 붙여줘야 합니다

