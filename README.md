# vue-chatkit

## connect
[http://localhost:8080/](http://localhost:8080/)
[http://localhost:8080/chat](http://localhost:8080/chat)

## まずったところ
store/index.js
ERROR:Expected an assignment or function call and instead saw an
 expression
```
getters: {
  <!-- hasError: state => state.error ? true : false //動かん-->
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

src/chatkit.js
```
const MESSAGE_LIMIT = Number(process.env.VUE_APP_MESSAGE_LIMIT) || 10 // eslint-disable-line
...
let activeRoom = null // eslint-disable-line
```

store/mutations.js
- ESLintのエラー出まくり
- ERROR:indent
- 元々VScodeのタブでのインデントでの設定がスペース4つなので2に変更

/ほとんどのファイル
- 最後空白行入れないとエラー出る
- 元のコード自体に","など余計なものが多い

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
