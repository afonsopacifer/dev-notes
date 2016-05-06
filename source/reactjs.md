# ReactJS
[Facebook Docs](http://facebook.github.io/react/docs/getting-started.html) / [Awesome React](https://github.com/enaqx/awesome-react) / [egghead](https://egghead.io/) / [udemy](https://www.udemy.com/react-redux/)

> O React é uma biblioteca para criar interfaces, que foi idealizada pela galera do Facebook e Instagram.

- [Notes](#notes)
  - [Workspace Setup](#workspace-setup)
  - [Components](#components)
  - [JSX](#jsx)
  - [Props](#props)
  - [States](#states)
  - [Events](#events)
  - [Refs](#refs)
  - [Keys](#keys)
  - [Component Lifecycle](#component-lifecycle)
  - [<s>Inline Styles</s>](#)
  - [<s>React Router</s>](#)
  - [<s>Tests</s>](#)
  - [<s>a11y</s>](#)
  - [<s>Flux</s>](#)
  - [<s>Redux</s>](#)
  - [<s>Best Practices</s>](#)
  - [<s>RxJS</s>](#)
  - [<s>Immutable</s>](#)
- [References](#references)
  - [Webpack e Babel](#)
  - [ES6](#)
  - [Tests](#)
  - [Flux](#)
  - [Redux</s>](#)

<hr>

## Notes

#### Workspace Setup
[slush-react-start](https://github.com/afonsopacifer/slush-react-start) - Generator for React + ES5 (Browserify) or ES6 (Webpack/Babel)

#### Components

Componente com ES5 e createClass:

```js
// index.js
var React    = require('react'),
    ReactDOM = require('react-dom');

var Layout = React.createClass({
  render: function(){ // ou apenas render(){
    return (
      <h1>Hello</h1>
    )
  }
});

ReactDOM.render(<Layout/>, document.getElementById('app'));
```
Componente com ES6 e createClass:

```js
// index.js
import React from "react";
import ReactDom from "react-dom";

const Layout = React.createClass({
  render(){
    return (
      <h1>Hello</h1>
    )
  }
});

ReactDOM.render(<Layout/>, document.getElementById('app'));
```

Componente com ES6 e Class/Extends:

```js
// index.js
import React from "react";
import ReactDom from "react-dom";

class Layout extends React.Component {
  render() {
    return (
      <h1>Hello</h1>
    );
  }
}

ReactDom.render(<Layout/>, document.getElementById('app'));
```

Sub Componente com ES6:

```js
// hello.js
import React from "react";

class Hello extends React.Component {
  render() {
    return (
      <h1>Hello</h1>
    );
  }
}

export default Hello;
```

Sub Componente com ES6 / simple function:

```js
// hello.js
import React from "react";

function Hello() {
  return (
    <h1>Hello</h1>
  );
}

export default Hello;
```

Carregando o subcomponente ES6:

```js
// index.js
import React from "react";
import ReactDom from "react-dom";
import Hello from "./hello.js";

class Layout extends React.Component {
  render(){
    return (
      <Hello />
    )
  }
});

ReactDOM.render(<Layout/>, document.getElementById('app'));
```

#### JSX

```js
```

```js
```

#### Props

```js
```

```js
```

#### States

```js
```

```js
```

#### Events

```js
```

```js
```

#### Refs

```js
```

```js
```

#### Keys

```js
```

```js
```

#### Component Lifecycle

```js
```

```js
```

#### Inline Styles

```js
```

```js
```

#### React Router

```js
```

```js
```

#### Tests

```js
```

```js
```

#### a11y
?????

#### Flux
?????

#### Redux
?????

#### Best Practices
?????

#### RxJS
?????

#### Immutable
?????

<hr>

## References
- [[Guide] - Começando com ReactJS - Willian Justen - PT-BR](http://willianjusten.com.br/comecando-com-react/)
- [[Guide] - Como usar o ReactJS - Willian Justen - PT-BR](http://willianjusten.com.br/como-usar-o-reactjs/)
- [[Guide] - O básico da API do ReactJS - Willian Justen - PT-BR](http://willianjusten.com.br/o-basico-da-api-do-reactjs/)
- [[Article] React.js na vida real do Codecademy - Bonnie Eisenman - PR-BR ](http://www.infoq.com/br/articles/reactjs-codecademy)
- [Video] ReactJS a biblioteca javascript do facebook - Eu Programador - PT-BR
  - [Introdução](https://www.youtube.com/watch?v=y08X0vpd6q4&index=1&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT)
  - [Props](https://www.youtube.com/watch?v=xhhxPLyVEUY&index=2&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT)
  - [PropTypes](https://www.youtube.com/watch?v=w4oD5dPUndY&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT&index=3)
  - [Trabalhando com Props](https://www.youtube.com/watch?v=MMHTMyhi_qQ&index=4&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT)
  - [Eventos e Componentização](https://www.youtube.com/watch?v=cfefccP1Kgc&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT&index=5)
  - [Refs](https://www.youtube.com/watch?v=6PEPmrLVcuA&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT&index=6)
  - [State e Manipulação do DOM](https://www.youtube.com/watch?v=p3P1dZlgvzU&index=7&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT)
  - [Diferentes Sintaxes](https://www.youtube.com/watch?v=9WKoglv7yhQ&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT&index=9)
- [[Video] React e Flux - Uma nova abordagem - Cássio Zen - PT-BR ](https://www.youtube.com/watch?v=4FroPIYEsYY)
- [[Video] Palestra ReactJS - Eu Programador - PT-BR ](https://www.youtube.com/watch?v=gIGB0061wzM&list=PLXFk6ROPeWoAe9BdLdy--VBtDwMP1L6sT&index=9&spfreload=5#t=852.305222)
- [[Example] 5 Practical Examples For Learning The React Framework - Martin Angelov - EN](http://tutorialzine.com/2014/07/5-practical-examples-for-learning-facebooks-react-framework/)
- [[Example] - React Demos - Ruan YiFeng - EN](https://github.com/ruanyf/react-demos)
- [Video] - ReactJS Tutorial - LearnCode - EN
  - [Intro & Workspace Setup](https://youtu.be/MhkGQAoc7bc)
  - [Anatomy of a Component](https://youtu.be/fd2Cayhez58)
  - [Composing Multiple Components](https://youtu.be/vu_rIMPROoQ)
  - [State, Props & Data](https://youtu.be/qh3dYM6Keuw)
  - [Events & Data Changes](https://youtu.be/_D1JGNidMr4)
  - [React Router & Intro to Single Page Apps](https://youtu.be/1iAG6h9ff5s)
  - [React Router Params & Queries](https://youtu.be/ZBxMljq9GSE)
  - [React Inline Styles & Component Arrays](https://youtu.be/XVdwq8W2ZsM)
- [[] - - ]()
- [[] - - ]()

#### Webpack end Babel
- [[Guide] Começando com React ES6 e Webpack - Bu Kinoshita - PR-BR ](http://chocoladesign.com/comecando-com-react-es6-e-webpack)
- [[Guide] React preset - BabelJS - EN](https://babeljs.io/docs/plugins/preset-react/)
- [[] - - ]()
- [[] - - ]()

#### ES6
- [[Article] React.createClass versus extends React.Component - Swizec Teller - EN](https://toddmotto.com/react-create-class-versus-component/)
- [[] - - ]()
- [[] - - ]()

#### Tests
- [[Article] How React Components Make UI Testing Easy - Todd Motto - EN](https://www.toptal.com/react/how-react-components-make-ui-testing-easy)
- [[Article] Testing in ES6 with Mocha and Babel 6 - James K Nelson - EN](http://jamesknelson.com/testing-in-es6-with-mocha-and-babel-6/)
- [[Article] Testing React on Jsdom - Jake Trent - EN](http://jaketrent.com/post/testing-react-with-jsdom/)
- [[Article] Test Driven React Tutorial - Spencer - EN](http://spencerdixon.com/blog/test-driven-react-tutorial.html)
- [[Article] UI Testing in React - Arunoda Susiripala - EN](https://voice.kadira.io/ui-testing-in-react-74fd90a5d58b#.snpwoe76s)
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()

#### Flux
- [Video] - React Flux Tutorial - LearnCode - EN
  - [React Flux Tutorial](https://youtu.be/PvjNglsyOHs)
  - [Flux Store Events (Coming Mon, Feb 22@11CST)](https://youtu.be/bvEC6i7CUyE)
  - [The Flux Dispatcher (Coming Tues, Feb 23@11CST)](https://youtu.be/MZfCVq5iCBw)
  - [Flux Actions (Coming Wed, Feb 24@11CST)](https://youtu.be/0yW7C22ooos)
  - [Async Flux Actions](https://youtu.be/CuYd9uDB0vg)
  - [React Flux Memory Leaks](https://youtu.be/Fgd2ivSnXXo)
- [[Video] Arquitetura com Flux - Eric Yoshi - PT-BR](https://www.youtube.com/watch?v=_nwIM9MFioo&annotation_id=annotation_893873139&feature=iv&src_vid=3tIpOl0lLKo)
- [[Video] Flux: A simple architecture model to build Client-side apps! - Pedro Nauck - PT-BR]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()

#### Redux
- [Video] - Redux Tutorial - LearnCode - EN
  - [How Redux Works](https://www.youtube.com/watch?v=1w-oQ-i1XB8)
  - [Immutable JS](https://www.youtube.com/watch?v=9M-r8p9ey8U)
- [[Guide] Full-Stack Redux Tutorial - Tero Parviainen - EN](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
- [[] - - ]()
