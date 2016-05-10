# AngularJS
[Awesome AngularJS](https://github.com/gianarb/awesome-angularjs)

>

- [Notes](#notes)
  - [Setup](#Setup)
  - [Diretivas básicas](#diretivas-basicas)
    - [ng-app](#ng-app)
    - [ng-model](#ng-model)
    - [ng-bind](#ng-bind)
    - [<s>ng-controler</s>](#)
    - [<s>ng-click</s>](#)
    - [<s>ng-repeat</s>](#)
    - [<s>ng-show</s>](#)
    - [<s>ng-hode</s>](#)
    - [<s>ng-class</s>](#)
    - [<s>ng-init</s>](#)
    - [<s>ng-route</s>](#)
  - [<s>Model</s>](#)
  - [<s>View</s>](#)
    - [<s>Filters</s>](#)
  - [<s>Controlers</s>](#)
  - [<s>CRUD</s>](#)
    - [<s>Create</s>](#)
    - [<s>Retrieve</s>](#)
    - [<s>Update</s>](#)
    - [<s>Delete</s>](#)
  - [<s>Dependencies injection</s>](#)
  - [<s>Rest API</s>](#)
  - [<s>Routes</s>](#)
  - [<s>Animations</s>](#)
  - [<s>Diretivas personalizadas</s>](#)
- [References](#references)

<hr>

## Notes

## Diretivas básicas

#### Setup
```html
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.5/angular.min.js"></script>
```

#### ng-app
Inicia o app:

```html
<body ng-app>
...
</body>
```

Seleciona o modulo:

```html
<body ng-app="demo">
...

  <script>
    angular.module('demo', []);
  </script>
</body>
```

#### ng-model
Define o model:

```html
<body ng-app>
  <input type="text" ng-model="nome"/>
  {{nome}} <!-- view -->
</body>
```

#### ng-bind
Define a variavel que sera renderizada na view:

```html
<body ng-app>
  <input type="text" ng-model="nome"/>
  <span ng-bind="nome"></span>
</body>
```

####
```html
```

<hr>

### Model

####
```html
```

<hr>

### View

#### Filters

```html
```

```html
```

<hr>

####
```html
```

####
```html
```

####
```html
```

####
```html
```

####
```html
```

<hr>

## References
- [[Guide] angularjs-directive-manual - Suissa - PT-BR ](https://github.com/suissa/angularjs-directive-manual)
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
