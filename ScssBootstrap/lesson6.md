# Sass - Less 6

## Ի՞նչ է LESS-ը
LESS (Language for End System Services) - համարվում է CSS - ի ընդլայնում : Այն պարունակում է մեծ ֆունկցիոնալ և դրա շնորհիվ հեշտացնում է աշխատանքը CSS միջավայրում։
Փոփոխականները LESS-ում
SASS -ի առաջին դասում ծանոթացել ենք փոփոխականների հետ։ Ի տարբերություն SASS - ի LESS -ում փոփոխականները հայտարարվում են @ - ի օգնությամբ։

```css
// Variables
@my-selector: banner;
// Usage
.@{my-selector} {
font-weight: bold;
line-height: 40px;
margin: 0 auto;
}
```
## Փոփոխականներ
LESS - ում հնարավոր է սահմանել փոփոխականի անվանում օգտագործելով մեկ այլ փոփոխական, օրինակ`
Որը կկոմպիլիացվի հետևյալ կոդի՝

```scss
@primary: green;
@secondary: blue;
.section {
@color: primary;
.element {
color: @@color;
}
} ////////////
.section .element {
color: green;}
```
## Փոփոխականի առանձնահատկությունները
Ստորև նշված օրինակներում ցույց է տրվում օգտագործման երկու հնարավոր տարբերակները:
Երկու դեպքում էլ կստանանք նույն կոդը՝

```less
.lazy-eval {
width: @var;
}
@var: @a;
@a: 9%;

    //second example
    @var: @a;
    @a: 9%;
    .lazy-eval {
    width: @var;
    }

////////////result
.lazy-eval {
width: 9%;
}
```
Երբ երկու անգամ սահմանում ենք նույն փոփոխականը , ինչպես և CSS - ում , կոդը կարդացվում է վերևից ներքև ։ Դիտարկենք հետևյալ օրինակը:Այս դեպքում կստանանք հետևյալ արդյունքը՝
```less
@var: 0;
.class {
@var: 1;
.brass {
@var: 2;
three: @var;
@var: 3;
}
one: @var;
}

//result
.class {
one: 1;
}
.class .brass {
three: 3;
}
```

## Ծնող սելեկտորներ
& օպերատորը ներկայացնում է ծնող սելեկտորի ներդրման կանոները: Օրինակ՝
```scss
a {
color: blue;
&:hover {
color: green }
}
///result
a {
color: blue; }
a:hover {
color: green;
}
&-ի օգտագործումը
& օպերատորը կարող ենք օգտագործել մի քանի անգամ հետևյալ կերպ՝
.link {
& + & {
color: red;
}
& & {
color: green;
}
&& {
color: blue;
}
&, &ish {
color: cyan;
}
}
//result
.link + .link {
color: red;
}
.link .link {
color: green;
}
.link.link {
color: blue;
}
.link, .linkish {
color: cyan;}
```
## @extend -ը LESS-ում
@extend -ների մասին գաղափար կազմել ենք դաս 3-ում: Սակայն LESS - ում նրա սինտաքսը այլ է։ Այն գրելաւձևով նման է փսեվդո կլասի գրելաձևին, մի բացառությամբ՝ @extend -ի ներսում կարող ենք գրել all բանալիային բառը, որը կնշանակի, որ հատկությունները կժառանգվեն կլասի հնարավոր տարբերակներից։Օրինակ ՝
```less
.c:extend(.d all) {
// extends all instances of ".d" e.g. ".x.d" or ".d.x"
}
.c:extend(.d) {
// extends only instances where the selector will be output as just ".d"
}
```
## MIXIN - ներ
Mixin-ները կամ խառնուրդները թույլ են տալիս որոշել և օգտագործել այն ոճերը, որոնք ծրագրում օգտագործվում են մի քանի անգամ։ Սա օգնում է խուսափել կոդի կրկնությունից:։LESS - ում միքսինների գրելաձևը հետևյալն է ։ Օրինակ՝
```less
.bordered {
border-top: dotted 1px black;
border-bottom: solid 2px black;
}
#menu a {
color: #111;
.bordered();
}
.post a {
color: red;
.bordered();
}
```

## Տնային աշխատանք

1. Կրկնել ամբողջ թեման մինչև այսօր։