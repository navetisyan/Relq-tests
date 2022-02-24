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
Ինչպես՞ է new Classname()ը աշխատում: գրեք հերթական քայլերը: ինչ է իրենից  ներկայացնում __proto__-ն, ինչ տարբերություն prototype-ի հետ՞

## 5
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

## 6
Ինչ կտպի այս կոդը՞: Ինչն է այստեղ բաց թողնված՞, Ֆիքսեք այն:

```js story
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
```

## 7 
Ունենք 2 API request-ներ, ամեն մեկը տևում է ենթադրենք 2 վայրկյան: Այս դեպքում այս 2 requestները իրար հետևից կանչելով 2ի աշխատանքը կտևի 4 վայրկյան:
Ինչպես կարող ենք փոփոխել կոդը, որ 2ի պատասխանը միասին ստանանք 2 վայրկյան հետո: Գրեք փոփոխած կոդը

``` js story

fetch(`https://restcountries.com/v2/name/armenia`)
  .then((response) => {
    if (!response.ok) throw new Error(`Country not found (${response.status})`);
    return response.json();
  })
  .then((data) => {
    console.log("Armenia: data=", data);
  });

fetch(`https://restcountries.com/v2/name/australia`)
  .then((response) => {
    if (!response.ok) throw new Error(`Country not found (${response.status})`);
    return response.json();
  })
  .then((data) => {
    console.log("Australia: data=", data);
  });

```

## 8
Տրված է PersonCl classը: 
1. Ստեղծեք PersonCl-ի instance
2. Ինչ տարբերություն greet և het ֆունկցիաների միջև:
class PersonCl {
  constructor(fullName, birthYear) {
    this.fullName = fullName;
    this.birthYear = birthYear;
  }

  // Instance methods
  // Methods will be added to .prototype property
  calcAge() {
    console.log(2037 - this.birthYear);
  }

  greet() {
    console.log(`Hey ${this.fullName}`);
  }

  // Static method
  static hey() {
    console.log("Hey there 👋");
    console.log(this);
  }
}
