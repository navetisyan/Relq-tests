# Relq-tests
#### React 

## 1. 
#### Any function that takes in a function or returns one out is a higher-order function.
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
React.js-ում life-cycleը ունի հետևյալ ֆազաները ՝ (life-cycle phases ) 

#### Mounting, updating, unmounting

Այս life-cycle մեթոդներից որը որ ֆազայում է կանչվում.

componentWillUnmount
componentDidMount
componentDidUpdate
constructor
Render

Կարող եք ներկայացնել գծագրի տեսքով

9․ Ավանդական life-cycle մեթոդների այժմ որ hook-երն են փոխարինում։ Նշեք մի քանիսը։
10. (State-ը կառավարելու համար որ hook-ն է օգտագործվում, ինչպես նաև որտեղից է import արվում։ Ներքում փորձեք գրել import-ը և hook-ի գրելաձևը։) Նշված օրինակում անհրաժեշտ է count-ը պահել hook-ի մեջ և handleClick-ի ժամանակ այն ավելացնել 1-ով։
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
11. (Պատկերացրեք Ձեր app-ում կան side effect-ներ(կողմնակի էֆֆեկտներ), որ hook-ը կօգտագործեք այն իմպլեմենտելու համար։ Ներքում նշեք մեկական պրակտիկ օրինակ։) Օրինակում ունենք ռեքուստ արած դատա "https://restcountries.com/v3.1/all": Ռեքուստ արած դատան պահել hook-ի մեջ countryData անունով, օգտագործելով side effect-ների համար ստեղծված հուկը իմպլեմենտել fetch արած դատան։
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
12․ Ինչ նպատակով է օգտագործվում ref-ը React-ում, և օրինակում էջը բացելիս օգտագործելով ref-ը focus տեղադրեք input թեգի վրա։
import React from "react";
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
13. Ինչու մենք դատան չենք պահում սովորական փոփոխականի մեջ այլ hook-ի մեջ ենք պահում։
14․ Ծնողից մի քանի մակարդակ ներքև ինչպես կարող ենք դատա փոխանցել, առանց props-ի (hook-ի միջոցով)։
15․ Ինչ է իրենից ներկայացնում Virtual Dom-ը։
16․ Տրված է const names = ["Tigran", "Pap", "Artashes", "Artavazd"] data-ն, սա ինչպես կպատկերեք React-ում համարակալված և իրար հաջորդական (Հաշվի առնել, որ դատան կարող է լինել 1000 հատ անուն, ուստի պետք է գրել դինամիկ կոդ, օգտագործելով array մեթոդ)։
17․ Ինչու ենք key-ը օգտագործում React-ում list-երի ժամանակ։
18․ Ներքևում նշված օրինակում ինչու է օգտագործվում ․․․ կետերը։
<Modal {...this.props} title='Modal heading' animation={false}>

19․ Ներքևում նշված կոդում ինչու է օգտագործվում ․․․ կետերը։
this.setState(prevState => { return {foo: {...prevState.foo, a: "updated"}}; })
