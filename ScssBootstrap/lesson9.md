# Bootstrap 9

## Margin & Padding

margin & Padding - ները դրանք լուսանցքներ են

Bootstrap - ում դրանք գրվում են հետևյալ ձևով:

Օրինակ

1. margine-top & padding-top

```html
<div class="mt-5">Welcome</div>
<div class="pt-5">Welcome</div>
```

2. margine-bottom & padding-bottom

```html
<div class="mb-5">Welcome</div>
<div class="pt-5">Welcome</div>
```

3. margine-left & padding-left

```html
<div class="ms-5">Welcome</div>
<div class="ps-5">Welcome</div>
```

4. margine-right & padding-right

```html
<div class="me-5">Welcome</div>
<div class="pe-5">Welcome</div>
```

## Carousel (Slide-Show)



նշենք որ Carousel օգտագործելու համար մենք պետք է ունենանք մեր html փաստաթղթում կցաց նաև Bootstrap - ի Java script file - ը

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
  
    <script src="bootstrap.min.css"></script>
</body>
</html>
```
Slide-Show - ի Օրինակ՝

```html
<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="..." alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Third slide">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
```


## Տնային աշխատանք 1

1. Ստեղծել Carusel ձեր նկարներով։
2. Margin & Padding - ով ստանալ նկարում պատկերվածը։
![Image](./image/lesson9margin.png "Text to show on mouseover")


