# Prop Diff
`propDiff(srcObj, destObj)` return true or false, `console.log`  diff message at the same time.

It's useful to check if the real API format match the DOCS

```
⠴ --- [object Object] Delete these keys: foods
⠦ +++ [object Object] Add these keys: house,favorite
### Type error: 'name' [object Symbol] --> [object String]
### Type error: 'age' [object String] --> [object Number]
       ### Recursive check: 'company'
+++ [object Object] Add these keys: niubiliby
```

### STEP1 
install dependencies

```
npm install --save-dev ramda colors prop-diff
```

### STEP2
require and use

* Example1
```
const propDiff = require('propDiff')
var srcObj = {
  name: Symbol('bob alan green'),
  age: '30',
  isMale: false,
  ganDie: undefined,
  stepInTheSameRiver: Symbol('River'),
  changeFace: function (){console.log('I am a king')},
  money: NaN,
  friends: ['ZhangSan', 'Olivia'],
  born: new Date('2019-04-10'),
  company: {name:'google', tel: '1818'},
  foods: ['tomato'],
}

var destObj = {
  name: 'bob alan green',
  age: 30,
  isMale: true,
  ganDie: undefined,
  stepInTheSameRiver: Symbol('River'),
  changeFace: function (){console.log('I am a king')},
  money: NaN,
  house: null,
  friends: ['ZhangSan', 'Olivia'],
  born: new Date('2019-04-10'),
  favorite: /girl/g,
  company: {name:'google', niubiliby:true, tel: '1818'},
  
}

propDiff(srcObj, destObj)

```


* Example2
```
const propDiff = require('propDiff')

var srcObj = $AjaxDataObj 
var destObj = $YourMockDataObj

propDiff(srcObj, destObj)
```