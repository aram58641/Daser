# Bootstrap 8

Յուրաքանչյուր սարքավորման համար կարելի է փոխել կայքի էլեմենտների դիրքերը և միևնույն ժամանակ ապահովել կայքի ադապտիվությունը։

```html
<div class="container-fluid">
    <div class="row">
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
    </div>
</div>
```

Եթե մի տողում սյուների քանակը 12-ից մեծ լինի ապա վերջին էլեմենտը կիջնի ներքև։ Եթե ցանկանում ենք տողի սյուներ բաժանել և էլեմենտների մի մասն տեղափոխել ներքև, կիրառում ենք w-100 կլասը։

```html
<div class="container-fluid">
    <div class="row">
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-6">.col-6 .col-md-4</div>
    </div>
</div>

<div class="container">
    <div class="row">
        <div class="col">col</div>
        <div class="col">col</div>
        <div class="w-100"></div>
        <div class="col">col</div>
        <div class="col">col</div>
    </div>
</div>
```

## Տեքստի համար նախատեսված մի քանի կլասներ

<table class="table table-bordered table-hover">
<tbody>
<tr>
<td class="font-1 bold">text-center<br>text-left<br>text-right<br>text-stretch<br>text-nowrap</td>
<td class="font-1 ">տեքստի տեղափոխումը հորիզոնական ուղղությամբ</td>
</tr>
<tr>
<td class="font-1 bold">text-success<br>text-info<br>text-warning<br></td>
<td class="font-1 ">տեքստի տառերի գունավորում bootstrap-ի ստանդարտ գույներով</td>
</tr>
<tr>
<td class="font-1 bold">bg-success<br>bg-info<br>bg-warning<br></td>
<td class="font-1 ">տեքստի տիրույթի գունավորում bootstrap-ի ստանդարտ գույներով<br><br></td>
</tr>
</tbody>
</table>

## Աղյուսակի համար նախատեսված մի քանի կլասներ

<table class="table table-bordered table-hover">
<tbody>
<tr>
<td class="font-1 bold">table</td>
<td class="font-1 ">Աղյուսակը կազմում է bootstrap-ի ստանդարտներին համապատասխան</td>
</tr>
<tr>
<td class="font-1 bold">table-dark</td>
<td class="font-1 ">Աղյուսակի տիրույթը մգացնում է</td>
</tr>
<tr>
<td class="font-1 bold">table-bordered</td>
<td class="font-1 ">Աղյուսակի եզրերը հաստ գծում է դարձնում</td>
</tr>
<tr>
<td class="font-1 bold">table-hover</td>
<td class="font-1 ">Աղյուսակի տողերին hover հատկությունն է տալիս</td>
</tr>
<tr>
<td class="font-1 ">Շարունակությունը`&nbsp;<a href="https://getbootstrap.com/docs/4.3/content/tables/">tables</a></td>
</tr>
</tbody>
</table>

## Bootstrap. Նկարների համար նախատեսված մի քանի կլասներ

<table class="table table-bordered table-hover">
<tbody>
<tr>
<td class="font-1 bold">img-fluid</td>
<td class="font-1 ">Կայքի չափերը փոքրացնելիս նկարն էլ է փոքրանում</td>
</tr>
<tr>
<td class="font-1 bold">img-thumbnail</td>
<td class="font-1 ">Նկարի եզրերը գծում է</td>
</tr>
<tr>
<td class="font-1 bold">rounded-circle</td>
<td class="font-1 ">Նկարի ֆորման ձևափոխում է շրջանի</td>
</tr>
</tbody>
</table>

## Button (կոճակներ)

Bootstrap-ը ներառում է մի քանի նախապես սահմանված կոճակների ոճեր, որոնցից յուրաքանչյուրը ծառայում է իր իմաստային նպատակին:
Օրինակ՝

```html
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>
```
## Forms 
Ահա արագ օրինակ՝ Bootstrap-ի  ոճերը ցուցադրելու համար table - ում: 

Օրինակ՝

```html
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
```
## Տնային աշխատանք

1. Ստեղծել նկարում պատկերված աղյուսակը։

![Image](./image/table.png "Text to show on mouseover")
2. Ստեղծել նկարում պատկերված ֆորման։

![Image](./image/Forms.jpg "Text to show on mouseover")
