# Java Script 11

## Ի՞նչ է Json - ը

Json – ը տվյալների փոխանակման սինտաքսիս է։ JavaScript և սերվեր տվյալների փոխանակումը կատարվում է Json – ի միջոցով։

### Json սինտաքսի կանոններ

1. Տվյալները գրվում են զույգ - զույգ ՝ անուն - արժեք։
2. Տվյալները իրարից անջատվում են ստորակետով։
3. Օբյեկտները գրվում են ձևավոր փակագծերի մեջ։
4. Զանգվածներ

```json
{
    "username": "admin",
    "email": "admin@localhost.com",
    "adm": {
        "password": "123"
    }
}
```

### Ի՞նչ է Ajax - ը

Ajax – ը կլիենտ – սերվեր տվյալների փոխանակման տեխնոլոգիա է։ Այս տեխնոլոգիայի միջոցով կարող ենք ասինխրոն հարցում կատարել սերվերին, այսպիսով կստանանանք սերվերի պատասխանը առանց էջը թարմացնելու։
Ստեղծում ենք Json օբյեկտ

```js
// text.text
[
{
    "name":"John",
    "age":31,
    "city":"New York"
};
]
// Կարդում ենք Json օբյեկտի տվյալները //
 function f() {
         const xhttp = new XMLHttpRequest();
         xhttp.onload = function() {
           document.getElementById("box").innerHTML =
           this.responseText;
         }
         xhttp.open("GET", "text.text");
         xhttp.send();
     }
```

## Տնային աշխատանք 1

1. Ստեղծել table, որտեղ Select - ում գտնվող ցանկացած երկրի անվան վրա սեղմելով կստանանք ամեն երկրի մասին ցանկացած ինֆորմացիա։
