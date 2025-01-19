# Java Script 4

## Զանգվածի գաղափարը և հայտարարումը

Զանգված նշանակում է տվյալների խումբ, որը բնութագրվում է հստակ անունով, և, որի յուրաքանչյուր տարր պետք է տարբերվի մյուսներից հերթական համարով։ Ծրագրավորման JavaScript լեզվում զանգվածի տարրերի համարակալումը սկսվում է 0-ից։ Զանգվածը հայտարարում ենք [ ], հետևյալ սիմվոլների օգնությամբ։ Զանգված կարելի է նկարագրել նաև արժեքավորելով նրա տարրերը։

```js
var x = [];
var x = ["David", "Hayk", "Artak"];
console.log(x);
```

## Զանգվածների հետ աշխատող հիմնական մեթոդները

1. x.tostring()Զանգվածը դարձնում է տեքստ
2. x.join(‘\*’)Զանգվածները դարձնում է տեքստ։ Ի տարբերություն tostring մեթոդի, << , >> նշանի փոխարեն կօգտագործի փոխանցված պարամետրերը որպես առանձնացնող նշան
3. x.pop()ջնջում և վերադարձնում է վերջին էլեմենտի արժեքը
4. x.push()ավելացնում է նոր էլեմենտ զանգվածում վերջից
5. x.shift()կջնջի զանգվածի առաջին էլեմենտը
   push և unshift ֆունկցիաներ

6. Unshift ֆունկցիան, ավելացնում է իրեն փոխանցված տարրը կամ տարրերը զանգվածին՝ սկսած սկզբնական դիրքից։

```js
var countries = ["Armenia", "Russia", "Italy"];
countries.push("USA");
console.log(countries); // կտպի ['Armenia',  'Russia','Italy', 'USA']

var countries = ["Armenia", "Russia", "Italy"];
countries.unshift("USA");
console.log(countries); // կտպի ['USA','Armenia','Russia','Italy'];
```

## pop և shift ֆունկցիաներ

pop ֆունկցիան հեռացնում է զանգվածի վերջին տարրը։  
shift ֆունկցիան հեռացնում է զանգվածի առաջին տարրը։

```js
var countries = ["Armenia", "Russia", "Italy"];
countries.pop();
console.log(countries); // կտպի ['Armenia','Russia']

var countries = ["Italy", "Armenia", "Russia"];
countries.shift();
console.log(countries); // կտպի ['Armenia','Russia']
```

## splice, to string և join ֆունկցիաները

1. splice ֆունկցիայի օգնությամբ կարող ենք տարր ավելացնել կամ հեռացնել զանգվածի կամայական դիրքում։
2. tostring և join ֆունկցիաները զանգվածը դարձնում են տեքստ։ Ի տարբերություն tostring մեթոդի, join մեթոդը << , >> նշանի փոխարեն կօգտագործի փոխանցված պարամետրերը որպես առանձնացնող նշան։

```js
//splice
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
// կտպի [Banana,Orange,Lemon,Kiwi,Apple,Mango]

//toString
var num = 15;
var stringNum = num.toString();
console.log(typeof stringNum);

//Join
var fruits = ["Banana", "Orange", "Apple", "Mango"];
t = fruits.join("*");
console.log(t);
//կտպի Banana*Orange*Apple*Mango
```

## Զանգվածներ և for ցիկլ

Զանգվածի վրա for ցիկլի կիրառման օրինակ։

```js
var Arr = [5, 10, 15, 20, 30, 40, 55, 10.5];
for (let i = 0; i < Arr.length; i++) {
    console.log(Arr[i]);
}
```



## Տնային աշխատանք

1. Ներմուծել 2 թիվ
2. Ավելացնել այդ թվերը զանգվածի վերջում
3. Արտածել բոլոր անդամները
4. Արտածել գումարը
5. Ներմուծել ևս 1 թիվ
6. Ավելացնել այդ թիվը զանգվածի սկզբում
7. Տպել զանգվածը
