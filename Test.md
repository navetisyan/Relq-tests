# Relq-tests
##### Second Exam for February

## 1. 
Ապահովել getFirstWord ֆունկցիան, որի միջոցով հնարավոր լինի ստանալ string-ի առաջին բառր
#
```js story

let longText = "any text goes here";
const first_word = longText.getFirstWord();
console.log("first_word = ", first_word); // կտպի 'any' բառը

```

## 2. 
Գրել ֆունկցիա, որը կհաշվի տրված լիստի բոլոր value-ների գումարը
#
```js story

let list = {
  value: 1,
  next: {
    value: 2,
    next: {
      value: 3,
      next: {
        value: 4,
        next: null,
      },
    },
  },
};

```

## 3. 
Այս կոդը չի տպում tom-ի անունը: Կարող եք բացատրել թե ինչու և ինչպես ֆիքսենք այն՞

```js story

function Person(name) {
  this.name = name;
}
Person.prototype.getName = () => {
  return this.name;
};
const tom = new Person('Tom');
console.log(tom.getName()); //տպում է '' - դատարկ string

```

## 4
Մարդիկ կանգնած են այգում շարքով, նրանց արանքում կան ծառեր, որոնք հնարավոր չի տեղաշարժել:
Ձեր խնդիրն է սորտավորել մարդկանց ըստ իրենց բոյերի աճման կարգով առանց տեղաշարժելու ծառերը: 
Մեզ տրված է զանգվածը, որտեղ նշված են մարդկանց հասակները, իսկ ծառերի փոխարեն նշված է '-1': 
Գրել solution ֆունկցիան:
Օրինակ

 ```js story
 people = [-1, 150, 190, 170, -1, -1, 160, 180], 
այս զանգվածի համար 
solution(people) = [-1, 150, 160, 170, -1, -1, 180, 190]

```

## 5
Ինչ կտպի այս կոդը՞: Ինչն է այստեղ բաց թողնված՞, Ֆիքսեք այն:

var promise = new Promise(function() {
    setTimeout(function() {
        resolve('hello world');
    }, 2000);
});

promise.then(function(data) {
    console.log(data + ' 1');
});

promise.then(function(data) {
    console.log(data + ' 2');
});

promise.then(function(data) {
    console.log(data + ' 3');
});
