# Java Script 5

## Զանգվածի հետ աշխատող Reduce մեթոդը

Reduce մեթոդը նախատեսված է որպեսզի պտտվենք զանգվածի էլեմենտների վրայով վերցնենք դրանցում առկա մեկից ավել զանգվածները , օբյեկտները եվ այլն։
Այդ ամենը լցնենք մի նոր տարրի մեջ արդյունքում կլինի զանգվածի փոքրացում։
Այդ էլեմենտներն էլ կլինեն մեկ տարրի մեջ։

Reduce մեթոդով կարելի է ստանալ թե Map թե Foreach մեթոդբերը ավելի կարճ տարբերակով;

```js
let people = [
    {
        name: "John",
    },
    {
        lastname: "Doe",
    },
    {
        age: "20",
    },
];

let mapPeople = people.reduce((aggr, item) => {
    if (item.name !== undefined) {
        aggr.name = item.name;
    } else if (item.lastname !== undefined) {
        aggr.lastname = item.lastname;
    } else if (item.age !== undefined) {
        aggr.age = item.age;
    }
    return aggr;
}, {});


console.log(mapPeople);







const array = [10, 5, 6, 35, 8, 9, 10, 11, 14, 15, 63, 52, 152, 1, 21, 5];

const result = array.reduce((aggr, value) => {
    if (value % 2 != 0) {
      aggr.odd.list.push(value);
      aggr.odd.sum += value;
    } else {
      aggr.even.list.push(value);
      aggr.even.sum += value;
    }

    return aggr;
  },
  {
    odd: {
      list: [],
      sum: 0,
    },
    even: {
      list: [],
      sum: 0,
    },
  }
);
```


### Filter

Filter մեթոդը պտտվում է զանգվածի էլեմենտների վրայով վերցնում միայն այն էլեմենտները որոնք բավարարում են մեր պայմանին։

```js
    let people = [
        name:"John",
        lastname:"Doe",
        age:"35"
    ];

    people.filter((item)=>{

        return item.name === John;

    })
```



## Տնային աշխատանք


2. Վերցնել զանգվածում առկա օբյեկտները և սարքել մեկ օբյեկտ Reduce մեթոդի միջոցով։
3. Այդ էլեմենտների վրա կատարել ֆիլտեր վերցնել միայն նրանք որոնց տարեթիվը մեծ է 2015 թ․ - ից։
