# Vue.JS
[Vue.JS Docs](https://vuejs.org/guide/installation.html) / [Awesome Vue.js](https://github.com/vuejs/awesome-vue)

> Uma biblioteca (lib) javascript para o desenvolvimento de componentes reativos para interfaces web modernas.

- [Notes](#notes)
  - [Setup](#setup)
  - [Overview](#overview)
    - [Hello Word](#hello-word)
    - [Two-way Binding](#two-way-binding)
    - [Render a List](#render-a-list)
    - [Handle User Input](#handle-user-input)
  - [Directives](#directives)
    - [v-text](#v-text)
    - [v-html](#v-html)
    - [<s>v-show</s>](#v-show)
    - [v-if](#v-if)
    - [v-else](#v-else)
    - [v-for](#v-for)
    - [v-on](#v-on)
    - [v-bind](#v-bind)
    - [<s>v-model</s>](#v-model)
    - [v-ref](#v-ref)
    - [v-el](#v-el)
    - [v-pre](#v-pre)
    - [<s>v-cloak</s>](#v-cloak)
  - [Lifecycle](#lifecycle)
    - [created](#created)
  - [Filters](#filters)
    - [capitalize](#capitalize)
    - [uppercase](#uppercase)
    - [lowercase](#lowercase)
    - [currency](#currency)
    - [pluralize](#pluralize)
    - [json](#json)
    - [debounce](#debounce)
    - [limitBy](#limitBy)
    - [filterBy](#filterBy)
    - [orderBy](#orderBy)
    - [Custom Filters](#custom-filters)
- [References](#references)

<hr>

## Notes


### Setup

**CDN**
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/vue/1.0.26/vue.min.js"></script>
```

**NPM**
```sh
$ npm install vue
```

**CLI Scaffolding**

*install vue-cli*
```sh
$ npm install -g vue-cli
```

*create a new project using the "webpack" boilerplate*
```sh
$ vue init webpack my-project
```

*install dependencies and go!*
```sh
$ cd my-project
$ npm install
$ npm run dev
```
<hr>

### Overview

#### Hello World

*index.html*

```html
<div id="app">
  {{ message }}
</div>
```

*app.js*

```js
new Vue({
  el: '#app',
  data: {
    message: 'Hello World'
  }
})
```

<hr>

#### Two-way Binding

*index.html*

```html
<div id="app">
  <p>{{ message }}</p>
  <input v-model="message">
</div>
```

*app.js*

```js
new Vue({
  el: '#app'
})
```

<hr>

#### Render a List

*index.html*

```html
<div id="app">
  <ul>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ul>
</div>
```

*app.js*

```js
new Vue({
  el: '#app',
  data: {
    todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue.js' },
      { text: 'Build Something Awesome' }
    ]
  }
})
```
<hr>

#### Handle User Input

*index.html*

```html
<div id="app">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>
```

*app.js*

```js
new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```
<hr>

### Directives

#### v-text

```html
<span v-text="msg"></span>
<!-- same as -->
<span>{{msg}}</span>
```

<hr>

#### v-html

```html
<div v-html="html"></div>
<!-- same as -->
<div>{{{html}}}</div>
```

<hr>

#### v-show

```html

```

<hr>

#### v-if

```html
<div id="example-2">
  <p v-if="greeting">Hello!</p>
</div>
```

```js
var exampleVM2 = new Vue({
  el: '#example-2',
  data: {
    greeting: true
  }
})
```

<hr>

#### v-else

```html
<div v-if="Math.random() > 0.5">
  Sorry
</div>
<div v-else>
  Not sorry
</div>
```

<hr>

#### v-for

```html
<div v-for="item in items">
  {{ item.text }}
</div>
```

<hr>

#### v-on

```html
<!-- method handler -->
<button v-on:click="doThis"></button>

<!-- inline statement -->
<button v-on:click="doThat('hello', $event)"></button>

<!-- shorthand -->
<button @click="doThis"></button>

<!-- stop propagation -->
<button @click.stop="doThis"></button>

<!-- prevent default -->
<button @click.prevent="doThis"></button>

<!-- prevent default without expression -->
<form @submit.prevent></form>

<!-- chain modifiers -->
<button @click.stop.prevent="doThis"></button>

<!-- key modifier using keyAlias -->
<input @keyup.enter="onEnter">

<!-- key modifier using keyCode -->
<input @keyup.13="onEnter">
```

<hr>

#### v-bind

```html
<!-- bind an attribute -->
<img v-bind:src="imageSrc">

<!-- shorthand -->
<img :src="imageSrc">

<!-- class binding -->
<div :class="{ red: isRed }"></div>
<div :class="[classA, classB]"></div>
<div :class="[classA, { classB: isB, classC: isC }]">

<!-- style binding -->
<div :style="{ fontSize: size + 'px' }"></div>
<div :style="[styleObjectA, styleObjectB]"></div>

<!-- binding an object of attributes -->
<div v-bind="{ id: someProp, 'other-attr': otherProp }"></div>

<!-- prop binding. "prop" must be declared in my-component. -->
<my-component :prop="someThing"></my-component>

<!-- two-way prop binding -->
<my-component :prop.sync="someThing"></my-component>

<!-- one-time prop binding -->
<my-component :prop.once="someThing"></my-component>
```

<hr>

#### v-model

```html

```

<hr>

#### v-ref

```html
<comp v-ref:child></comp>
<comp v-ref:some-child></comp>
```

```js
// access from parent:
this.$refs.child
this.$refs.someChild
```

<hr>

#### v-el

```html
<span v-el:msg>hello</span>
<span v-el:other-msg>world</span>
```

```js
this.$els.msg.textContent // -> "hello"
this.$els.otherMsg.textContent // -> "world"
```

<hr>

#### v-pre

```html
<span v-pre>{{ this will not be compiled }}</span>
```

<hr>

#### v-cloak

```html

```

<hr>


<hr>

### Lifecycle

#### created

```js
var vm = new Vue({
  data: {
    a: 1
  },
  created: function () {
    // `this` points to the vm instance
    console.log('a is: ' + this.a)
  }
})
```

<hr>

### Filters

#### <s>capitalize</s>

```js
{{ msg | capitalize }}

//‘abc’ => ‘Abc’
```

<hr>

#### <s>uppercase</s>

```js
{{ msg | uppercase }}

//‘abc’ => ‘ABC’
```

<hr>

#### <s>lowercase</s>

```js
{{ msg | lowercase }}

//‘ABC’ => ‘abc’
```

<hr>

#### <s>currency</s>

```js
{{ amount | currency }}
//12345 => $12,345.00

{{ amount | currency '£' }}
//12345 => £12,345.00

{{ amount | currency '₫' 0 }}
//12345 => ₫12,345
```

<hr>

#### <s>pluralize</s>

```js
{{count}} {{count | pluralize 'item'}}

//1 => ‘1 item’
//2 => ‘2 items’
```

<hr>

#### <s>json</s>

*Output the result of calling JSON.stringify() on the value instead of outputting the toString()*

```html
<pre>{{ nestedObject | json 4 }}</pre>
```

<hr>

#### <s>debounce</s>

*Wrap the handler to debounce it for x milliseconds*

```html
<input @keyup="onKeyup | debounce 500">
```

<hr>

#### <s>limitBy</s>

```html
<!-- only display first 10 items -->
<div v-for="item in items | limitBy 10"></div>

<!-- display items 5 to 15 -->
<div v-for="item in items | limitBy 10 5"></div>
```

<hr>

#### <s>filterBy</s>

```html
<div id="filter-by-example">
  <input v-model="name">
  <ul>
    <li v-for="user in users | filterBy name in 'name'">
      {{ user.name }}
    </li>
  </ul>
</div>
```

```js
new Vue({
  el: '#filter-by-example',
  data: {
    name: '',
    users: [
      { name: 'Bruce' },
      { name: 'Chuck' },
      { name: 'Jackie' }
    ]
  }
})
```

<hr>

#### <s>orderBy</s>

```html
<ul>
  <li v-for="user in users | orderBy 'name'">
    {{ user.name }}
  </li>
</ul>
```

<hr>

#### <s>Custom Filters</s>

```js
Vue.filter('reverse', function (value) {
  return value.split('').reverse().join('')
})
```

```html
<!-- 'abc' => 'cba' -->
<span v-text="message | reverse"></span>
```

```js
Vue.filter('wrap', function (value, begin, end) {
  return begin + value + end
})
```

```html
<!-- 'hello' => 'before hello after' -->
<span v-text="message | wrap 'before' 'after'"></span>
<hr>
```
#### CLI

```js
// index.js

```

<hr>

## References
- [[Article] - Por que VueJS é uma boa opção? - Vinicius Reis - PT-BR](http://www.vuejs-brasil.com.br/por-que-vuejs-e-uma-boa-opcao/)
