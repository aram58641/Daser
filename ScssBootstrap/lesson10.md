# Bootstrap 10

## flexbox

Օգտագործեք

1. flex-row - հորիզոնական ուղղություն սահմանելու համար (default)
2. flex-row-reverse հորիզոնական ուղղությունը հակառակ կողմից սկսելու համար:

```html
<div class="d-flex flex-row">
    <div class="p-2">Flex item 1</div>
    <div class="p-2">Flex item 2</div>
    <div class="p-2">Flex item 3</div>
</div>
<div class="d-flex flex-row-reverse">
    <div class="p-2">Flex item 1</div>
    <div class="p-2">Flex item 2</div>
    <div class="p-2">Flex item 3</div>
</div>
```

## flex-column

1. flex-column ուղղահայաց ուղղություն սահմանելու համար
2. flex-column-reverse ուղղահայաց ուղղությունը հակառակ կողմից սկսելու համար:

```html
<div class="d-flex flex-column">
    <div class="p-2">Flex item 1</div>
    <div class="p-2">Flex item 2</div>
    <div class="p-2">Flex item 3</div>
</div>
<div class="d-flex flex-column-reverse">
    <div class="p-2">Flex item 1</div>
    <div class="p-2">Flex item 2</div>
    <div class="p-2">Flex item 3</div>
</div>
```

## justify-content -

ֆլեքս տարրերի դասավորվածությունը հիմնական առանցքի վրա փոխելու համար :

1.  start(default),
2.  end,
3.  center,
4.  between կամ around:
```html
<div class="d-flex justify-content-start">...</div>
<div class="d-flex justify-content-end">...</div>
<div class="d-flex justify-content-center">...</div>
<div class="d-flex justify-content-between">...</div>
<div class="d-flex justify-content-around">...</div>
```
## align-items

ճկուն տարրերի դասավորությունը y առանցքի վրա:

1. start(default),
2. end,
3. center,
4. baselineկամ stretch;

```html
<div class="d-flex align-items-start">...</div>
<div class="d-flex align-items-end">...</div>
<div class="d-flex align-items-center">...</div>
<div class="d-flex align-items-baseline">...</div>
<div class="d-flex align-items-stretch">...</div>
```
## wrap տողադարձ
1. flex-nowrap 
2. flex-wrap
3. flex-wrap-reverse:

```html 
<div class="d-flex flex-nowrap">
  ...
</div>
```

## order
  Այս գործիքը թույլ է տալիս տարրերի հերթականությունը դասավորել ըստ ցանկության։
  ```html
  <div class="d-flex flex-nowrap">
  <div class="order-3 p-2">First flex item</div>
  <div class="order-2 p-2">Second flex item</div>
  <div class="order-1 p-2">Third flex item</div>
</div>
```
## Տնային աշխատանք 2

1. Հավաքել մակետը ։
   <a href="./files/lesson9.psd" rel="nofollow" target="_blank" >Ներբեռնել մեդիա Մակետը</a>
