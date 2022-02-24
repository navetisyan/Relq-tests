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
