# Relq-tests
#### React 

## 1. 
#### Any function that takes in a function or returns one out is a higher-order function(HOF).
Այն ֆունկցիան, որը որպես պարամետր ստանում է ֆունկցիա, կամ վերադարձնում է ֆունկցիա, կոչվում է higher-order function:
Իսկ մյուս ֆունկցիաները - first class ֆունկցիաներ:
Ուսումնասիրեք կոդի օրինակը, որտեղ multiply և summarize-ը first-class ֆունկցիաներ են, իսկ describingFuncը higher-order function։ 
Գրեք մեկ այլ higher-order function, որի անունը կլինի - withoutNegatives , այդ ֆունկցիան կվերադարձնի մուտքագրված ֆունկցիան, բայց արգումենտներից ֆիլտրած բացասական թվերը.

```js-story
const  numbers = [10, 20, -2, 30, -3];

const multiply = (arr) => {
	return arr.reduce((agg, value) => {
  			return agg * value;
  }, 1);
};

const summarize = (arr) => {
	return arr.reduce((agg, value) => {
  			return agg + value;
  }, 0);
};

const describingFunc = (func) => {
			return (args) => {
      			return `The result of ${func.name} is ${func(args)}`;
      }

};

const wrappedMultiply = describingFunc(multiply);
const wrappedSummarize = describingFunc(summarize);


console.log(wrappedMultiply(numbers));
console.log(wrappedSummarize(numbers));
```

## 2. 
Ինչ է Imperative(հրամայական) և declarative(նկարագրողական) programmingը. 

```js-story
//version 1
let name = "Alonzo";
let greeting = "Hi";
console.log(`${greeting}, ${name}!`);

//version 2
function greet(greeting, name){
 return `${greeting}, ${name}!`;
};
greet("Hi", "Alonzo");
```
Ո՞ր տիպին է պատկանում reactը.


## 3. 
  Ինչ կոմպոնենտների տեսակներ գիտեք React-ում։
  
## 4. 
 Ինչ դերակատարում ունի render մեթոդը React-ում, ինչի համար է այն նախատեսված։

## 5.

Ինչ է վիրտուալ DOMը


## 6.

Ինչպես կարող ենք կոմպոնենտից կոմպոնենտ դատա փոխանցել։ Ինչպես data-ն կփոխանցեք Parent-ից Child: 
Նշված օրինակում լրացնել բաց թողնվածը, Child div-ի մեջ նկարելով ծնողից փոխանցված դատան։

```js-story
import React from "react";

function Parent() {
  const data = "Data from parent";
  return (
    <div>
      <Child />
    </div>
  );
}

function Child() {
  return <div></div>;
}

export default Parent;

```

## 7. 
Ինչպես դատան Child-ից կփոխանցեք Parent-ին։ Նշված օրինակում data-ն փոխանցեք ծնողին և նկարեք ծնողի կոմպոնենտում։

```js-story
import React from "react";

function Parent() {
  return (
    <div>
      <Child />
      {data}
    </div>
  );
}

function Child() {
  const data = "Data from child";
  return <div></div>;
}

export default Parent;

```

## 8. 
React.js-ում որոնք են life-cycleի ֆազաները ՝ (life-cycle phases ) և մեթոդները


Կարող եք ներկայացնել գծագրի տեսքով


## 9. 

State-ը կառավարելու համար որ hook-ն է օգտագործվում, ինչպես նաև որտեղից է import արվում։ Ներքում փորձեք գրել import-ը և hook-ի գրելաձևը։ 
Նշված օրինակում անհրաժեշտ է count-ը պահել hook-ի մեջ և handleClick-ի ժամանակ այն ավելացնել 1-ով։

```js-story
import React from "react";
function Counter() {
  function handleClick() {}
  return (
    <React.Fragment>
      <button onClick={handleClick}></button>
      <h1>{count}</h1>
    </React.Fragment>
  );
}
```

## 10.
ինչ է թույլ տալիս useEffect-ը

```js-story
> Perform side-effects inside a function components
> Accept a context object and return the current context value for that context object
> Return a statefull value and a function
```

## 11.
Պատկերացրեք Ձեր app-ում կան side effect-ներ(կողմնակի էֆֆեկտներ), որ hook-ը կօգտագործեք այն իմպլեմենտելու համար։
Օրինակում ունենք ռեքուստ արած դատա "https://restcountries.com/v3.1/all": Ռեքուստ արած դատան պահել hook-ի մեջ countryData անունով:
Օգտագործելով side effect-ների համար ստեղծված հուկը գրել դատան fetch անելու ֆունկցիոնալը.

```js-story
import React from "react";
import "./App.css";

function App() {
  return (
    <div className="App">
      {countryData &&
        countryData.map((country) => (
          <li width={"200px"} height={"200px"}>
            {country.name.official}
          </li>
        ))}
    </div>
  );
}

```

## 12.

Ինչ նպատակով է օգտագործվում ref-ը React-ում, և օրինակում էջը բացելիս օգտագործելով ref-ը focus տեղադրեք input թեգի վրա։
import React from "react";

```js-story
const InputModal = ({ initialValue, onSubmit, onClose }) => {
  return (
    <div className="modal--overlay">
      <div className="modal">
        <h1>Insert a new value</h1>
        <input type="text" value={value} />
      </div>
    </div>
  );
};
export default InputModal;

```
