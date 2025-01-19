# Sass - 3

## Օպերատորներ

Օպերատորները ծրագրավորման ամենափոքր ինքնավար մասը կամ հրամանն են։
Վերագրման օպերատոր
SASS - ն օգտագործում է (:), որպեսզի փոփոխականին վերագրվի որևէ արժեք , օրինակ ՝

```scss
$main-color: lightgray;
```

## Թվաբանական օպերատոր

Օպերատոր Նկարագրություն

`+` Գումարում

`-` Հանում

`*` Մազմապատկում

` /` Բաժանում

`%` Բաժանման մնացորդը

```scss
h2 {
    width: 3px \* 5 + 5px; // 20px

    width: 3 * (5px + 5px); // 30px

    width: 3px + (6px / 2) * 3; // 12px
}
```

### Պայմանի օպերատորներ

SASS - ում պայմանի @if օպերատորը ընդունում է SassScript արտահայտությունը , և օգտագործում է իր մեջ ներդրված ոճը , այն դեպքում , երբ արտահայտությունը վերադարձնում է կամայական արժեք բացի false - ից և null - ից:

```SCSS
p {
@if 1 + 1 == 2 { border: 1px solid; }
@if 5 < 3 { border: 2px dotted; }
@if null { border: 3px double; }
}
```

@if արատահայտությունից հետո կարող են գրվել մի քանի @else if արտահայտություններ և մեկ @else արտահայտություն:Եթե @if - ը վերադարձնում է false, ապա փորձ է կատարվում հաշվել @else if արտահայտություները մինչև նրանցից մեկը չվերադարձնի true , կամ էլ մինչև չհասնի @else արտահայտությանը : Օրինակ ՝

```SCSS
$type: NULL;
p {
@if $type == bool {
color: blue;
} @else if $type == undefined {
color: red;
} @else if $type == NULL {
color: green;
} @else {
color: black;
}
}
```

### Հավասարման օպերատոր

Օպերատոր Նկարագրություն

```
== Հավասար է
!= Հավասար չէ
```

```scss
@mixin font-fl($font) {
    &: ։after {
        @if (type-of($font) == string) {
            content: "My font is: #{$font}.";
        } @else {
            content: "Sorry, the argument #{$font} is a #{type-of($font)}.";
        }
    }
}
h2 {
    @include font-fl(sans-serif);
}
```

## Համեմատման օպերատորներ

Օպերատոր Նկարագրություն

`>` Մեծ է
`>=` Մեծ է և հավասար
`<` Փոքր է
`<=` Փոքր է և հավասար

```scss
$padding: 50px;

h2 {
    @if ($padding <= 20px) {
        padding: $padding;
    } @else {
        padding: $padding / 2;
    }
}
```

### Տրամաբանական օպերատորներ

Օպերատոր Պայման Նկարագրություն

```
And x and y Ճշմարիտ է, եթե երկու արտահայտություններն էլ ճշմարիտ են:
```

```
Or x or y Ճշմարիտ է, եթե x - ը կամ y - ը ճշմարիտ են:
```

```
Not x Ճշմարիտ է, եթե x - ը կեղծ է:
```

```scss
$list-map: (
    success: lightgreen,
    alert: tomato,
    info: lightblue,
);

@mixin button-state($btn-state) {
    @if (length($list-map) > 2 or length($list-map) < 5) {
        background-color: map-get($list-map, $btn-state);
    }
}
.btn {
    @include button-state(success);
}
```


## Տնային աշխատանք

1. Ծանոթանալ random ֆունկցիայի հետ։Գրել կոդ , որը կգեներացնի պատահական թիվ։ Այնուհետև կաշխատի ցիկլ ստացված թվի համապատասխան քանակով և կգեներացնի այդ քանակի շրջաններ, որոնք կունենան պատահական գունավորում և դասավորված կլինեն տարբեր տեղերում։
