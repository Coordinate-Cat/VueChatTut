# vue-chatkit

## deploy
[https://mystifying-bose-20acae.netlify.com/] <br>
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/)

## local
[http://localhost:8080/chat](http://localhost:8080/chat)

## まずった

元のコードと自分のlint設定に差異があってエラー出まくった
下記例

store/index.js
ERROR:Expected an assignment or function call and instead saw an
 expression
```
getters: {
  <!-- hasError: state => state.error ? true : false //動かん -->
  hasError: state => state.error
},
```

components/RoomList.vue
ERROR:space-before-function-paren
```
methods: {
    statusColor (status) { //関数と()の間開けない
        return status === 'online' ? 'success' : 'warning'
    }
}
```

components/MessageForm.vue
```
data () { //dataと()の間開ける
    return {
      message: ''
    }
  },
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
