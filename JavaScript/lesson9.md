# Java Script 9

## Document -ը JavaScript –ում

Եկեք հասկանանք ինչ է իրենից ներկայացնում document - ը։ Դրա համար console - ում արտածենք այն։

```js
console.log(document);
```

Ակնհայտ է դառնում , որ document -ը հանդիսանում է մեր պրոյեկտը:

### Window - ն JavaScript –ում

Փորձենք console - ում արտածել window - ն։

console.log(console)//առաջին տարբերակ
document.defaultView //երկրորդ տարբերակ

Window - ի պատուհանը  
 Console - ում երևում է , որ window - ն իրենից ներկայացնում է պատուհան , որը պարունակում է DOM ֆայլը։ Այն օբյեկտ է , որը իր մեջ պարունակում է բոլոր այն մեթոդների, հատկությունների և event - ների նկարագրությունները, որոնք կան DOM -ում։ Console - ը ևս հանդիսանում է window օբյեկտի մեթոդ։

### Window - ի մեթոդները

1. Window.alert() Ցուցադրում է նախորդ պատուհանի երկխոսությունները
2. Window.back() Պատուհանի պատմության մեջ վերադարձնում է մեկ քայլ հետ
3. Window.find() Window պատուհանում գտնում է համապատասխան տողը
4. Window.getAttention() Ստիպում է ֆայլի կոճակին թարթել

### Window - ի հատկությունները

1. Window.self Վերադարձնում է հղում ինքն իր վրա
2. Window.status Ստանում է կամ իրականացնում է տեքստը browser - ի ներքևի statusbar - ում ։
3. Window.screenX Վերադարձնում է բրաուզերի ձախ շրջանակի չափսերը հաշված էկրանի ձախ մասից
4. Window.screenY Վերադարձնում է բրաուզերի վերին շրջանակի չափսերը հաշված էկրանի վերին մասից

### Document.write()

Այս մեթոդի օգնությամբ կարող ենք վեբ էջում որևէ բան արտածել։ Այն կջնջի ողջ HTML կոնտենտը, և կարտածի այն, ինչ-որ փոխանցենք փակագծերի մեջ:

```js
document.write(5);
document.write("Hello world");
var a = 5;
document.write(a);
```

## Ի՞նչ է DOM - ը

DOM (Document Object Model) – ը փաստաթղթի օբյեկտային մոդելն է։ Այն նկարագրում է էջի կառուցվածքը, էլեմենտների դասավորվածությունը։
Ի՞նչ է HTML DOM - ը

1. HTML DOM – ըփաստաթղթում գտնվող օբյեկտներն են
2. HTML DOM – ըէլեմենտների հատկություններն են
3. HTML DOM – ըայն բոլոր մեթոդներն են, որոնցով մուտք ենք ունենում օբյեկտներ, ստանում ենք օբյեկտների հատկություններ
4. HTML DOM – ը իրադարձություներն են, օրինակ՝ կոճակի վրա քլիք, տեքստային տարածքի մեջ տեքստի փոփոխություն

### Ինչպե՞ս ստեղծել էլեմենտներ

```js
var h1 = document.createElement("h1"); //ստեղծում ենք կոճակ
var textH1 = document.createTextNode("ForEach"); // ստեղծում ենք տեքստ
document.body.appendChild(btn); // Ընդունում ենք <h1>-ը  <body>-ի համար:
```

## inerHTML և innerText մեթոդների տարբերությունը

innerText մեթոդն էկրանավորում է HTML կոնտենտը, այսինքն եթե այնտեղ գրենք HTML թեգեր, թեգերը կտպվեն էկրանին որպես տեքստ։ HTML կոնտենտ մուտքագրելու համար օգտվում ենք innerHTML մեթոդը։

Թեգերի հետ աշխատող մեթոդներ, Ավելացնում ենք / ջնջում էլեմենտներ

1. element.attribute = new value փոխում ենք ատրիբուտի արժեքը
2. element.SetAttribute(attribute, value) ստեղծում ենք նոր ատրիբուտ էլեմենտի համար
3. element.style = ``property = value ստիլավորում ենք էլեմենտը
4. document.createElement(element) ստեղծում ենք նոր էլեմենտ
5. document.removeChild(element) ջնջում ենք էլեմենտը
6. document.appendChild(element) ավելացնում ենք էլեմեն
7. document.replaceChild(element) փոխում ենք էլեմենտը

## HTMLElement.style հատկություն

HTMLElement.style հատկությունը օգտագործվում է HTML - ի էլեմենտները ոճավորելու և ոճերը վերցնելու համար։ Էլեմենի ոճը վերցնելու դեպքում վերադարձնում է CSSStyleDeclaration օբյեկտ, որն իր մեջ պարունակում է ինֆորմացիա տվյալ էլեմենտի բոլոր ոճեր։ Ոճեր ավելանում են HTML - ում inline: Հետևաբար ունի նույն առաջնայինությունն, ինչ տողային գրելաձևը։

```js 
document.getElementById("p2").style = "color: blue;";
```

HTMLElement.style հատկության ճիշտ գրելաձևը
Ոճը խորհուրդ չի տրվում ավելացնել անմիջապես style հրամանի օգնությամբ, քանի որ այն վերադարձնում է CSSStyleDeclaration տիպի օբյեկտ՝ որը նախատեսված է միայն ընթերցանության համար։ Ավելի հարմար է ավելացնել օրինակ

```js
  elt.style.color = “blue”
  /// կամ
  elt.style.cssText = "color:red" ։
```

Ուշադրություն դարձրեք, որ elt.style. գրելաձևում ոճերը գրվում են այսպես կոչված camel-case - ով , այլ ոչ թե kebab-case , օրինակ՝

```js
elt.style.fontSize,
    // այլ ոչ թե
    elt.style.font - size;
```

## Տնային աշխատանք 2

1. Կազմել Ռեզյումե այնպես, որ HTML փաստաթղթում լինի միայն  JavaScript  ֆայլը։ Մնացած կոդը ամբողջությամբ լինի գրված JavaScript ֆայլում։
