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

let user = {
  name: "John",
  age: 30,

  sayHi() {
    alert(this.name);
  }
};
