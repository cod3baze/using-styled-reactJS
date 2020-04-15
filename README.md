# Demo

> Define folha de estilos usando Javascript

## encadeamento

usa-se regras de encadeamento igual no Saas.

```js
import styled from "styled-components";

export const Container = styled.h1`
  color: #f00;

  // encadeado
  span {
    color: #000009;
    font-weight: bold;
    line-height: 24;
  }
`;
```

## Passando props

podem ser passadas propriedades atraves do objeto: `props`

```js
import styled from "styled-components";

export const Container = styled.h1.attr(prop)`
  color: #f00;

  // acessando o props com uma função
  background: ${(props) => `${props.color}px`};
`;
```

## Herdando estilos de outros components

Para herdar estilos é usado o **styled** como método passando o arg **parent**: `styled(parent)`

```js
import styled from "styled-components";

export const Axe = styled.h1.attr(prop)`
  color: rgba(0, 0, 0, 0.5);
  background: #fff;
  box-shadow: 1px 0.5px 0.3px black;
`;

// herda estilos do component: Axe
export const Tuner = styled(Axe)`
  // estilos adicionais
  border-left: 1px solid black;
`;
```
