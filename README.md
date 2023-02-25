## html 파일과 js파일을 분리하여 작업해보자

```html
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-GLhlTQ8iRABdZLl6O3oVMWSktQOp6b7In1Zl3/Jr59b6EGGoI1aFkw7cmDA6j6gD" crossorigin="anonymous">
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

    <title></title>
</head>
<body>
    <h1>Hello, Vue :)</h1>
    <div id="app">
        <p>{{ title }} - by {{ author }}, {{ pages }}</p>
    </div>
    <script src="./lesson04/app04-1.js"></script>
</body>
</html>

```

```javascript
        Vue.createApp({
            data(){
                return {
                    title :'The way back to home',
                    author :'Spider man',
                    pages : 100
                }
            }
        }).mount('#app');
```
