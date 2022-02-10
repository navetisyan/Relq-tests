# Relq-tests
##### Exam for February

## 1. 
Օդանավակայանում ուղևորներին ռեգիստրացիա անելու պրոցեսը կատարվում է 
 checkIn functionի միջոցով: Այն մուտքում ստանում է թռիչքի համարը և ուղևորի տվյալներով օբյեկտ,
 ռեգիստրացիա անցնելուց հետո թռիչքի համարին կցվում է 'checked' բառը, իսկ  ուղևորի
 անվան դիմաց համապատասխանաբար ավելանում է Mr./Mrs. բառը:
 ինչ է տպում այդ 2 արժեքները ֆունկցիան կատարելուց հետո և ինչու:
 ԵՎ ինչպես անենք որ թռիչքի համարը և ուղևորի օբյեկտը մնան անփոփոխ ֆունկցիայի կատարումից հետո:
#
```js story
const flight = "LH234";
const jonas = {
  name: "Jonas Schmedtmann",
  passport: 24739479284,
};

const checkIn = function (flightNum, passenger) {
  flightNum = "LH234-checked";
  passenger.name = "Mr. " + passenger.name;

  if (passenger.passport === 24739479284) {
    console.log("Checked in");
  } else {
    console.log("Wrong passport!");
  }
};

checkIn(flight, jonas);
console.log(flight);
console.log(jonas);
```

## 2. 
Ունենք transformer ֆունկցիա, որը ստանում է 2 parameter
 - առաջինը string, երկրորդը - callback ֆունկցիա sayItIsTheBest անունով:
 sayItIsTheBest ֆունկցիան տրված ստրինգին պիտի գումարի 'is the best!' տեքստը,
 արդյունքում 
 
     transformer("Javascript", sayItIsTheBest);  կտպի 'Javascript is the best!' <br/>
     transformer("Java", sayItIsTheBest);  կտպի 'Java is the best!'

     //Գրել sayItIsTheBest ֆունկցիան, որպեսզի ստանանք վերը նշված ստրինգը.	

 
 ``` js story
const transformer = function (str, fn) {
  const transformedString = fn(str);

  console.log(`Original string: ${str}`);
  console.log(`Transformed string: ${transformedString}`);

  console.log(`Transformed by: ${fn.name}`);
};

transformer("Javascript", sayItIsTheBest);
transformer("Java", sayItIsTheBest);

```

## 3
```js story
function Country(name, yearFounded) {
  //գրել ֆունկցիայի մարմինը
}

const america = new Country("The United States of America", 1776);
america.describe(); // պիտի տպի - '"The United States of America was founded in 1776';

```
ստեղծել նաև Հայաստանի և Վրաստանի մասին համապատասխան օբյեկտը,
 որ describe ֆունկցիան տպի համապատասխան ինֆորմացիան այդ երկրների համար

## 4
 
 ``` js story
 
const book = {
  title: "Brave New World",
  author: "Aldous Huxley",
};

function summary() {
  console.log(`${this.title} was written by ${this.author}.`);
}
summary(); // ինչ կտպի սա, ինչու, և ինչպես վերականգնել

```
## 5
 Ինչ կտպի կոդը և ինչու: Բացատրել ներքոնշյալ 2 ֆունկցիաների կանչերի տարբերությունը։ 

```js story

const whoAmI = {
  name: "Leslie Knope",
  regularFunction: function () {
    console.log(this.name);
  },
  arrowFunction: () => {
    console.log(this.name);
  },
};

whoAmI.regularFunction();
whoAmI.arrowFunction();

```

## 6
```js story

const myUsers = [
  { name: "shark", likes: "ocean" },
  { name: "turtle", likes: "pond" },
  { name: "otter", likes: "fish biscuits" },
];

```
 Ունենք վերոնշյալ օբյեկտների զանգվածը, այս զանգվածից ստանալ մեկ այլ զանգված,
 որը կունենա հետևյալ տեսքը ՝
   
```js story 
	usersByLikes = {
		shark: 'ocean',
		turtle: 'pond',
		otter: 'fish biscuits'
	} 
 
```

## 7
 ինչ գույն կտպի տեքստը 
 
 ``` js story
 
const p = document.querySelector("p");
p.innerHTML = "Hello World";
setTimeout(function () {
  console.log("text color changed");
  p.style.color = "blue";
}, 0);
p.style.color = "red";

```

## 8
Ինչ է տպում այս կոդը:
կոդում կատարել փոփոխություն այնպես, որ լոգում տպվեն միայն 1ից 10 թվերը

``` js story

let i = 0;
function increment() {
  i++;
  console.log(i);
}
setInterval(increment, 1000);

```

## 9

ինչպես կանչենք logMessage ֆունկցիան, որպեսզի այն տպի "Hello, World!"

```js story

const object = {
  message: "Hello, World!",
};
function logMessage() {
  console.log(this.message); // "Hello, World!"
}
// Write your code here…

```

## 10
Ձեր բառերով նկարագրեք, ինչ է closureը(1-2 նախադասությամբ) <br/>
Ուսումնասիրեք հետևյալ կոդը և պատասխանեք հարցերին 

``` js story

function personalDice(name) {
  return function () {
    // generate random number between 1 and 6
    const newRoll = Math.floor(Math.random() * 6);
    console.log(`${name} rolled a ${newRoll}`);
  };
}

const dansRoll = personalDice("Dan");
const zoesRoll = personalDice("Zoe");

dansRoll();
dansRoll();

```

ա. Որտե՞ղ է օգտագործվում closureը այստեղ: Ինչպե՞ս կարող եք բացատրել: <br/>
բ. Համեմատեք և հակադրեք dansRoll ֆունկցիայի կանչը առաջին և երկրորդ անգամ:<br/>
  Ինչն է միշտ նույնը: Ի՞նչը կարող է փոխվել:<br/>
  գ. Ո՞րն է newRoll-ի lexical scopeը:

