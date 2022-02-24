### TEST

## 1
Ի՞նչ կտպի

```js story

let animal = {
  jumps: null
};
let rabbit = {
  __proto__: animal,
  jumps: true
};

alert( rabbit.jumps ); // ? (1)

delete rabbit.jumps;

alert( rabbit.jumps ); // ? (2)

delete animal.jumps;

alert( rabbit.jumps ); // ? (3)

```

## 2

Ի՞նչ կտպի: 

 ```js story

let user = {
  name: "John",
  age: 30,

  sayHi() {
    alert(this.name);
  }

};

user.sayHi(); 

```

## 3
Այս օբյեկտի մեջ ավելացրեք getAge մեթոդ, որը կտպի userի տարիքը.

```js story

let user = {
  name: "John",
  age: 30,

  sayHi() {
    alert(this.name);
  }
};

```

## 4 
Գրել ucFirst(str) ֆունկցիա, որը կվերադարձնի stringը առաջին տառը մեծատառ դարձրած: Օրինակ

```js story
const result = ucFirst('john');
 console.log(result) // կտպի "John"
```

## 5
Նկարագրել ինչպես ենք ստեղծել tom օբյեկտը: tom-ը ինչ property-ներ և մեթոդներ ունի, ինչու ենք calcAge ֆունկցիան գրել prototype-ի մեջ

```js story
const Person = function (firstName, birthYear) {
  // Instance properties this= {}
  this.firstName = firstName;
  this.birthYear = birthYear;
};

Person.prototype.calcAge = function () {
  console.log(2037 - this.birthYear);
};

const tom = new Person('Tom', 20);
```

## 6
Ինչ կտպի այս կոդը և ինչու 

```js story

function job() {
    return new Promise(function(resolve, reject) {
        reject();
    });
}

let promise = job();

promise

.then(function() {
    console.log('Success 1');
})

.then(function() {
    console.log('Success 2');
})

.then(function() {
    console.log('Success 3');
})

.catch(function() {
    console.log('Error 1');
})

.then(function() {
    console.log('Success 4');
});

```
