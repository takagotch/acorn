### acorn
---
https://github.com/acornjs/acorn

```
npm install
```

```js
const {Parser} = require("acron")
const MyParser = Parser.extend(
  require("acron-jsx"),
  require("acron-bigint")
)
console.log(MyParser.parse("// Some bigint + JSX code"))

module.exports = function noisyReadToken(Parser){
  return class extends Parser {
    readToken(code){
      console.log("Reading a token!")
      super.readToken(code)
    }
  }
}
```

```
```


