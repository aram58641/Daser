# Html Css 10

## Անիմացիա

CSS3 - անիմացիայի միջոցով  կայքում պարունակվող էլեմենտներին տալիս ենք,որոշակի  դինամիկություն։ Անիմացիայի հիմքում ընկած են կադրեր, որոնք անընդհատ կրկնում են պատկերները որոշակի ժամանակում։ Անիմացիան կարելի է կազմակերպել HTML-ի գրեթե բոլոր էլեմենտների և pseudo-էլեմենտների համար։ Անիմացիան շատ ռեսուրս է ծախսում և ազդում է կայքի արագագործության վրա։
Անիմացիայի հատկությունները
1. Animation-name
2. @keyframes
3. Animation-duration
4. Animation-timing-function
5. Animation-delay
6. Animation-iteration-count
7. Animation-direction
8. Animation-play-state
9. Animation-timing-function


1. Animation-name

Անիմացիային անվանում տալու հատկությունն է, որն օգտագործվում է @keyframes կանոնի ժամանակ։ Կարելի է մի քանի անվանումներ նշել, դրանք միմյանցից առանձնանում են բացատներով։ Հատկությունները չի ժառանգվում։
```css
div {
    animation-name: mymove ( none | initial | inherit );
}                            

@keyframes animation-name  {                        
h1 {
   font-size: 3.5em;
   color: darkmagenta;
   animation: shadow;
}
} 
@keyframes shadow {
   from {text-shadow: 0 0 3px black;}
    50% {text-shadow: 0 0 50px black;}
     to {text-shadow: 0 0 30px black;}
             }                    
@keyframes flash {
        0% {opacity: 0.1;}  
       50% {opacity: 0.5;}
      100% {opacity: 1;} 
   }
   ```
2. Animation-duration  

Այս հատկությունով տրվում է անիմացիայի ընթացիկ ժամանակը (վայրկյաններով կամ միլիվայրկյաններով)։ Եթե էլեմենտին տրված է մեկից ավել անիմացիաներ, ապա յուրաքանչյուրի համար կարող ենք առանձին ժամանակներ գրել և դրանք միմյանցից առանձնացնել բացատներով։ Հատկությունը չի ժառանգվում։
```css
div {
    animation-duration: 2s;
} 
  
div {
animation-duration:  initial ( inherit);
}     
```                   

3. Animation-timing-function 

Այս հատկությունով որոշվում է անիմացիայի արագության փոփոխությունները սկզբից մինչև վերջին ակնթարթ։ Արժեքը տրվում է բանալի բառով կամ cubic-bezier(x1, y1, x2, y2)֊ով։ Արժեքները դիտել այստեղ ։ Հատկությունը չի ժառանգվում։
```css
div {
    animation-timing-function: linear;
}  
```
4. Animation-delay

Animation-delay Animation-iteration-count
Animation-delay-այս հատկությունով որոշում ենք թե անիմացիան կայքի բեռնումից հետո քանի վայրկյան հետո սկսի։ Հատկությունը չի ժառանգվում։
```css
div {
    animation-delay: 2s;
    }                               
```
5. Animation-iteration-count

հատկությունը թույլ է տալիս անիմացիան աշխատեցնել մի քանի անգամ։ 0 կամ բացասական արժեքի դեպքում անիմացիան դադարում է գործել։ Հատկությունը չի ժառանգվում։

```css
div {
     animation-iteration-count: 3 (infinite | initial | inherit);
    }
```

6. Animation-direction:

Այս հատկությունով որոշվում է անիմացիայի կրկնության ուղղությունը, եթե անիմացիան մի անգամ է կատարվելու, ապա այս հատկությունը կորցնում է իր ակտուալությունը։ Հատկությունը չի ժառանգվում։
Անիմացիային վերաբերվող բոլոր հատկությունները կարելի է միավորել մի տողում, և արժեքները միմյանցից առանձնացնել բացատներով։ Անիմացիայի ցուցադրման համար բավարար է լինեն այս հատկությունները՝ animation-name և animation-duration:

```css
div {
animation-direction: alternate (alternate-reverse | normal |reverse | initial | inherit)
}      
```

```
animation: animation-name animation-duration animation-timing-function animation-delay animation-iteration-count animation-direction;
Animation-play-state և animation-fill-mode
Animation-play-state
```

-հատկությունով որոշվում է անիմացիայի ցուցադրումը և դադարը։ Անիմացիան կարելի է դադարեցնել և՛ javascrtip-ի, և՛ մկնիկի իրադարձությունների(event) միջոցով։
Animation-fill-mode - այս հատկությունը որոշում է @keyframes-ի որոշակի օբյեկտների ոճավորման հաջորդականությունը
```css
div:hover {
    animation-play-state: paused (running | initial | inherit);
}                   
```
## Տնային աշխատանք 1
1. Ստեղծել նկարում պատկերված անիմացիան։


![Image](./image/homework10.gif "Homework8")






