# Polymer
[Polymer project](https://www.polymer-project.org/1.0/) / [Polycast](https://www.youtube.com/watch?v=jrt7sMq9lO0&index=49&list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN) / [Polymer Blog](https://www.polymer-project.org/1.0/blog/)

> <3

- [Notes](#notes)
  - [Basic Setup](#basic-setup)
    - [Polymer CLI](#polymer-cli)
    - [Bower](#bower)
    - [Polymer and webcomponents.js](#polymer-and-webcomponents.js)
  - Criando elementos
    - [Elements Setup](#elements-setup)
    - [Custom elements](#custom-elements)
      - [Create an element](#create-an-element)
      - [Use an element](#use-an-element)
    - [Properties](#properties)
      - [Create a property](#create-a-property)
      - [Use a property](#use-a-property)
    - [Events](#events)
  - Criando Apps
    - [App Setup](#app-setup)
    - [App structure](#app-structure)
    - [Deploy](#deploy)
      - [Build for deployment](#build-for-deployment)
      - [Deploy to a server](#deploy-to-a-server)
  - Mais coisas legais
    - [Data binding](#data-binding)
    - [two-way binding](#two-way-binding)
    - [Extendendo elementos nativos](#)
  - Catalog de elementos
    - [App Elements](#)
    - [Iron Elements](#)
    - [Paper Elements](#)
    - [Google Web Components](#)
    - [Gold Elements](#)
    - [Neon Elements](#)
    - [Platinum Elements](#)
    - [Molecules](#)
- [References](#references)

<hr>

## Notes

### Basic Setup

#### Polymer CLI
```bash
  $ [sudo] npm install -g polymer-cli
```

#### Bower
```bash
  $ [sudo] npm install -g bower
```

```bash
  $ bower init
```

#### Polymer and webcomponents.js
```bash
  $ bower install polymer/polymer --save
```

<hr>

### Elements Setup

```bash
  $ polymer init
```

**Element structure**

	.
	├── index.html
	├── element-name.html
	├── bower.json
	├── README.md
	├── demo/
	├── test/
	└── bower_components/

**Start a serve**

```bash
  $ polymer serve
```

**View element docs**

http://localhost:8080/components/element-name/

**View element demo**

http://localhost:8080/components/element-name/demo/

### Custom elements

#### Create an element
my-element.html

```html
<link rel="import" href="bower_components/polymer/polymer.html">

<dom-module id="my-element">
  <template>
    <style>
      /* CSS rules for your element */
      :host {

      }
    </style>

    <!-- local DOM for your element -->
    <h1>Hello world</h1>
  </template>

  <script>
    // element registration
    Polymer({
      is: 'my-element'
    });
  </script>
</dom-module>
```

#### Use an element
index.html

```html
<!doctype html>
<html>
  <head>
    <title>My app</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="my-element.html">
  </head>
  <body>
    <my-element></my-element>
  </body>
</html>
```

> **Note:** Para o import funcionar de boas é preciso de um server, para isso, podemos usar o polymer-cli: `$ polyserve`

<hr>

### Properties

#### Create a property
my-element.html

```html
<link rel="import" href="bower_components/polymer/polymer.html">

<dom-module id="my-element">
  <template>
    <h1>Hello {{prop}}</h1>
  </template>

  <script>
    Polymer({
      is: 'my-element',
      properties: {
        myProp: String
      }
    });
  </script>
</dom-module>

```

#### Use a property
index.html

```html
<!doctype html>
<html>
  <head>
    <link rel="import" href="my-element.html">
  </head>
  <body>
    <my-element myProp="World"></my-element>
  </body>
</html>
```

### Events

```js
Polymer({
  is: 'my-element',

  listeners: {
    'tap': 'showLog'
  },

  showLog: function() {
    console.log("hey hey hey");
  },
});
```

### App Setup

```bash
  $ mkdir my-app
```

```bash
  $ cd my-app
```

```bash
  $ polymer init app-drawer-template
```

```bash
  $ polymer serve --open
```

### App structure

	.
	├── index.html
	├── src/
	├── bower_components/
	├── images/
	└── test/

### Deploy

#### Build for deployment

```bash
  $ polymer build
```

Minifica o HTML , JS, e dependências CSS, gera um Service Work com um cache de todas as dependências para que tudo rode off-line.

`build/unbundled`: Versão para HTTP/2

`build/bundled`: Versão no formato "bundler" para HTTP/1

#### Deploy to a server

[View on docs](https://www.polymer-project.org/1.0/start/toolbox/deploy)

#### Data binding

my-element.html

```html
<link rel="import" href="bower_components/polymer/polymer.html">

<dom-module id="my-element">
  <script>
    Polymer({
      is: 'my-element',
      // add a callback to the element's prototype
      ready: function() {
        this.textContent = "Hey hey hey"
      }
    });
  </script>
</dom-module>
```

#### two-way binding

```bash
  $ bower install iron-input --save
```

my-element.html

```html
<link rel="import" href="bower_components/polymer/polymer.html">
<link rel="import" href="bower_components/iron-input/iron-input.html">

<dom-module id="my-element">
  <template>
    <p>{{owner}}</p>
    <input is="iron-input" bind-value="{{owner}}">
  </template>

  <script>
    Polymer({
      is: 'my-element',
      properties: {
        owner: {
          type: String,
          value: "Daniel"
        }
      }
    });
  </script>
</dom-module>
```

#### Extendendo elementos nativos

```js
MyInput = Polymer({

  is: 'my-input',

  extends: 'input',

  created: function() {
    this.style.border = '1px solid #000';
  }

});

var el1 = new MyInput();
// ou
var el2 = document.createElement('input', 'my-input');
```

Para usar:
```html
<input is="my-input">
```

#### Lifecycle

```js
MyElement = Polymer({

  is: 'my-element',

  created: function() {
    console.log(this.localName + '#' + this.id + ' was created');
  },

  ready: function() {
    console.log(this.localName + '#' + this.id + ' has local DOM initialized');
  },

  attached: function() {
    console.log(this.localName + '#' + this.id + ' was attached');
  },

  detached: function() {
    console.log(this.localName + '#' + this.id + ' was detached');
  },

  attributeChanged: function(name, type) {
    console.log(this.localName + '#' + this.id + ' attribute ' + name +
      ' was changed to ' + this.getAttribute(name));
  }

});
```

## References
- [[Video] Polymer and Progressive Web Apps: Building on the modern web - Google I/O 2016 - EN](https://www.youtube.com/watch?v=fFF2Yup2dMM)
- [[Docs] Get Started - Polymer Project - EN](https://www.polymer-project.org/1.0/start/index)
- [[Docs] Features - Polymer Project - EN](https://www.polymer-project.org/1.0/docs/devguide/feature-overview)
- [[Video] Progressive, Performant, Polymer: Pick Three - Google I/O 2016 - EN](https://www.youtube.com/watch?v=J4i0xJnQUzU&index=2&list=PLNYkxOF6rcIDnSm7bZRJC36Ca1DYXSQ70)
- [[Video] Practical lessons from a year of building web components - Google I/O 2016 - EN](https://www.youtube.com/watch?v=zfQoleQEa4w&index=3&list=PLNYkxOF6rcIDnSm7bZRJC36Ca1DYXSQ70)
- [[Video] Building the Google I/O Web App: Launching a Progressive Web App on Google.com - Google I/O 2016 - EN](https://www.youtube.com/watch?v=__KvYxcIIm8&index=4&list=PLNYkxOF6rcIDnSm7bZRJC36Ca1DYXSQ70)
- [[Video] Accessibility is My Favorite Part of the Platform - Google I/O 2016 - EN](https://www.youtube.com/watch?v=2qjgxH384Nc&index=5&list=PLNYkxOF6rcIDnSm7bZRJC36Ca1DYXSQ70)
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
