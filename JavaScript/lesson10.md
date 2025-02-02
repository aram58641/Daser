# Java Script 10

## Document.querySelector()

Վերադարձնում է ֆայլում այն բոլոր էլեմենտները , որոնք պատկանում են գրված է սելեկտորի խմբին։Վերադարձնում է NodeList տիպի էլեմենտներ որոնք դասավորված են նույն հերթականությամբ ինչ HTML ֆայլում։

```js
var el = document.querySelector("#test");
var matches = el.querySelectorAll("div.highlighted > p");
```

## Event-ներ (Իրադարձություններ)

Իրադարձություններն այն գործողություններն են, որոնք որ կատարում է օգտվողը բրաուզերում՝ սեղմում է կոճակին, պահում է որևէ էլեմենտի վրա ․․․․ ։ JavaScript - ի միջոցով կարող ենք արձագանքնել այդ իրադարձություններին։
### Onclick ատրիբուտ

```html
<!DOCTYPE html>
<html>
<body>
    <h1 onclick="this.innerHTML = "Ooops!>Click on this text!
    </h1>

    <button onclick="myfunc()">Click on this text!
    </button>
    <script>
        function myfunc() {
            alert('Click');
        };
    </script>
</body>
</html>
```
### Մեկ այլ եղանակ ավելացնելու onclick իրադարձությունն էլեմենտին:

```js
document.getElementById("myBtn").onclick = alert('Click');
```
### addEventListener մեթոդ



```js
document.getElementById("myBtn").addEventListener("click", displayDate <function>)
element.addEventListener("click", function(){ alert("Click"); })  
```
Ավելացնում ենք մի քանի իրադարձություն նույն էլեմենտին

```js
element.addEventListener("mouseover", myFunction);
element.addEventListener("click", mySecondFunction);
element.addEventListener("mouseout", myThirdFunction);
element.addEventListener("mouseout", my4thFunction);
```

### this ցուցիչ

this ցուցիչի արժեքը կախված է նրանից, թե ինչ մեթոդով է կանչված այն։ this - ին չի կարելի արժեք վերագրել ( Կան բացառություններ ES5 - ում հնարավոր է this բանալի բառին արժեք վերագրել , հաշվի չառնելով այն ,թե ինչ մեթոդով է կանչված այն)։
```js
var test = {
prop: 42,
func: function() {
return this.prop;
},
};
console.log(test.func());
// expected output: 42  
```
### this ցուցիչը գլոբալ կոնտեքստում
Գլոբալ կոնտեքստում this -ը վկայակոչում է գլոբալ օբյեկտը, հաշվի չառնելով այն օգտագործված է խիստ ,թե ոչ խիստ ռեժիմում
```js
console.log(this.document === document); // true:
console.log(this === window); // true this.a = 37;
console.log(window.a); // 37
```
### this ցուցիչը ֆունկցիայի կոնտեքստում

Ֆունկցիայի կոնտեքստում this - ը կախված է նրանից , թե ինչպես է կանչված ֆունկցիան։ Պարզագույն դեպքում this - ի արժեքը չի որոշվում ֆունկցիայի կանչով։Քանի որ կոդը գրված է ոչ խիստ ռեժիմում , ապա this - ը պետք է լինի գլոբալ օբյեկտ՝
```js
function f1(){ return this; } //In Browser f1() === window;
```

### this ցուցիչը խիստ ռեժիմում
Խիստ ռեժիմում this - ի արժեքը մնում է այն արժեքը,որը նրան տրված էր կատարման կոնտեքստում։Եթե այդպիսի արժեք չենք տվել , ապա կվերադարձնի undefined;
```js
function f2(){ "use strict"; // see strict mode return this; } f2() === undefined;
```
### Ի՞նչ է Callback ֆունկցիան
Callback -ը ֆունկցիա է ,որը պետք է կատարվի մեկ այլ ֆունկցիա կատարվելուց հետո։Այդ իսկ պատճառով էլ կոչվում է “հետ զանգ”։
Ի՞նչու է անհրաժեշտ օգտագործել Callback ֆունկցիան
JavaScript-ը հանդիսանում է միջոցառումներով պայմանավորված լեզու։ Սա նշանակում է, որ հարցման պատասխանին սպասելու խոփարեն JavaScript- ը կշարունակի կատարել այլ միջոցառումներ: Որպեսզի կարողանանք կառավարել այդ գործընթացը , պետք է ստեղծել Callback ֆունկցիա։

## Տնային աշխատանք 1

1. Սարքել նշված մակետը Java Script- ի միջոցով։ ԵՎ մակետի վրա լինի dark mode: 

<a href="./files/Resume_Portfolio.psd" rel="nofollow" target="_blank" class="btn btn-success btn-lg">Ներբեռնել Մակետը</a>