# Sass - 4

## Տողային օպերատորներ

• Եթե տողը գրում ենք չակերտների մեջ (+ օպերատորից առաջ) առանց չակերտների գրված տողի հետ , արդյունքում կստանանք տող՝ գրված չակերտներում:

• Եթե առանց չակերտների գրված տողը գրում ենք չակերտներով գրված տողի հետ , արդյունքում կստանանք տող՝ գրված առանց չակերտների:

```scss
@mixin string-concat {
    &:after {
        content: "My favorite language is " + Sass;
        font: Arial + " sans-serif";
    }
}
h2 {
    @include string-concat;
}
```

### Ցիկլեր

Ցիկլերը թույլ են տալիս տրված սահմաններում հաջորդաբար փոխել փոփոխականների արժեքները։ Sass-ում ցիկլ ստեղծելու համար օգտագործվում է @for հրամանը։ Հաշվարկների մեջ փոփոխականը գրվում է $i-ի տեսքով, սակայն կլասսերի կամ այլ հատկությունների արժեքը գրվում է #{$i}: Ցիկլերը հարմար են CSS-Sprites-ի համար, որում օգտագործվում է մեկ նկար, որը,իր հերթին, բաղկացած է բազմաթիվ նկարներից։

```scss
%craft {
    background: url(images/craft.png) no-repeat;
    width: 27px;
    height: 31px;
    display: inline-block;
    margin-right: 10px;
}
@for $i from 0 through 2 {
    .craft#{$i} {
        @extend %craft
$length: -31px*$i;
        background-position: 0 $length;
    }
}
```

## @each

@each հրամանը թույլ է տալիս անցնել ցուցակի արժեքների վրայով և յուրաքանչյուրին տալ հրամանների որոշակի քանակ։ Այն որոշ չափով համարվում է ցիկլի տարատեսակ, սակայն այստեղ մենք գործ ունենք ոչ թե թվային հաշվիչի, այլ ցուցակի, որի արժեքներն ինքներս ենք ստեղծում։ Սկզբից գրում ենք @each հրամանը, հետո փոփոխականի անունը, որը հաջորդաբար ընդունում է ցուցակի արժեքները, այնուհետև գալիս է in բանալիային բառը և արժեքների ցուցակը՝ ստորակետերով առանձնացված։ Ցիկլի մարմինը գրվում է ներսում՝ ձևավոր փակագծերի մեջ։

```scss
@each $browser in ie, chrome, firefox, opera {
    .#{$browser} {
        background: url(../img/#{$browser}.png) no-repeat;
    }
}
```

## @while

@while դիրեկտիվը գեներացնում է ոճեր այնքան ժամանակ, մինչև իրեն փոխանցված պայմանը չդառնա false: Այն նման է @for դիրեկտիվին, բայց ավելի ճկուն է։ Արժեքների դիապազոն տալու փոխարեն (ինչպես անում էին @for-ի դեպքում), մենք փոխում ենք ցիկլում փոփոխականի արժեքը և նորից ստուգում ենք պայմանը։

```scss
$x: 1;
@while $x < 13 {
    .col-#{$x} {
        width: 100/12 \* $x;
    }
    $x: $x + 1;
} ;
```

### Քննարկել հետևյալ կոդը տեղում

```scss
@mixin grid($cols, $margin) {
    float: left;
    background-color: brown;
    margin-right: $margin;
    margin-bottom: $margin;
    height: 150px;
    width: ((100% - (($cols - 1) \* $margin)) / $cols);

    &:nth-child(#{$cols}n) {
        margin-right: 0;
    }
}

.grid {
    float: left;
    width: 100%;
    > div {
        @include grid(4, 3%);
    }
}
```

## Տնային աշխատանք

1. Գրել մեդիա հարցում վերջինս ուսումնասիրած կոդի հիման վրա։

<a href="./files/lesson4_1.psd" rel="nofollow" target="_blank" >Ներբեռնել Մակետը</a>

<a href="./files/lesson4_2.psd" rel="nofollow" target="_blank" >Ներբեռնել մեդիա Մակետը</a>




