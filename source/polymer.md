# Polymer
[Polymer project](https://www.polymer-project.org/1.0/) / [Polycast](https://www.youtube.com/watch?v=jrt7sMq9lO0&index=49&list=PLOU2XLYxmsII5c3Mgw6fNYCzaWrsM3sMN) / [Polymer Blog](https://www.polymer-project.org/1.0/blog/)

> <3

- [Notes](#)
  - [Basic Setup](#)
    - [Polymer CLI](#)
    - [Bower](#)
    - [Polymer and webcomponents.js](#)
  - [Custom elements](#)
    - [Create an element](#)
    - [Use an element](#)
- [References](#)

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

### Custom elements

#### Create an element
my-element.html

```html
<link rel="import" href="bower_components/polymer/polymer.html">

<dom-module id="my-element">
  <template>
    <style>
      /* CSS rules for your element */
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
