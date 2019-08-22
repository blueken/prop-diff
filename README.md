# Prop Diff
`propDiff(srcObj, destObj)` return true or false, `console.log`  diff message at the same time

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