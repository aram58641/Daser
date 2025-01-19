# Html Css 9

## Մեդիա հարցումներ

Մեդիա հարցումները ֆիլտրեր են, որոնք թույլ են տալիս իրականացնել որոշակի CSS ոճեր՝ կախված օգտվողի սարքից,
Media օրինակ
Հիմնական օգտագործվող մեդիա տեսակները
all բոլոր տեսակները (լռելյայն արժեք)
print տպիչներ և այլ տպեղ սարքեր
screen համակարգչի էկրան
speech խոսքի սինթեզատորներ, կամ այլ տեքստը ձայնի վերածող ծրագրեր

braille բրայլի համակարգի վրա հիմնված սարքավորումներ
embossed բրայլի համակարգի համար նախատեսված տպիչներ
projection պրոյեկտորներ
tv հեռուստացույցեր

Մեդիա հարցման գրելաձևը (syntax)
Բոլոր մեդիա հարցումները սկսում ենք @media բառից, որից հետո գրվում է մեդիա-հարցման տեսակը կամ տրամաբանական օպերատորները, այնուհետև մեդիա֊ֆունկցիաները։

```css
/*screen*/
@media screen and (min-width: 800px) {
    ...
}
@media only screen and (min-width: 800px) and (max-width: 1000px) {
    ...
}
```

## Մետաթեգ Viewport

Մոբայլ browser-ները վեբ էջերը պատկերում են ավելի մեծ չափերով քան նախատեսված է։Viewport մետաթեգի միջոցով հնարավոր է կառավարել էկրանի չափերն ու մասշտաբը։ Այն գրվում է head թեգի մեջ և ի սկզբանե նախատեսված է եղել Ios ՕՀ-ով աշխատող browser-ի համար։ Բացի width և initial-scale արժեքներից այն կարող է ընդունել այլ արժեքներ ևս։

```html
<head>
    <meta charset="UTF-8" />
    <title>Document</title>

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>
```

Մետաթեգ Viewport օրինակներ

```
<!-- Արգելվում է մեծացնել մասշտաբը  -->
<meta name="viewport"content="width=device-width,maximum-scale=1.0, user-scalable=no">
<!-- Թույլատրվում է փոփոխել մասշտաբը-->
<meta name="viewport"content="width=device-width,user-scalable=yes">
<!-- Արտածման էկրանի լայնությունը 1600pxէ-->
<meta name="viewport"content="width=1600">


```

Էկրանի որ չափերի վրա կարելի է կենտրոնանալ


1. iPads
@media only screen and (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) { ․․․ }

2. Համակարգիչներ և նոութբուքեր 
@media only screen and (min-width: 1224px){ ․․․ }

3. Մեծ էկրաններ
@media only screen and (min-width: 1824px) { ․․․ }


4. iPhone 5 
@media only screen and (min-width: 320px) and (max-height: 568px) and (orientation: landscape) and (-webkit-device-pixel-ratio: 


## Տնային աշխատանք 1
1. Նշագրել հետևյալ PSD ֆայլը և մեդիա հարցումների միջոցով ապահովել ադապտիվությունը:

<a href="http://psd-html-css.ru/sites/default/files/public/old/rar_files/FlattyleWebsiteTemplateminimal.rar" rel="nofollow" target="_blank" class="btn btn-success btn-lg">Ներբեռնել Մակետը</a>