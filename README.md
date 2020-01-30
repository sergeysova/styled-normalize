# styled-normalize

CSS-normalize library for [styled-components](https://styled-components.com/).

The original `normalize.css` is pulled from [necolas/normalize.css](https://github.com/necolas/normalize.css), and parsed into styled ready format.


## Usage

```sh
npm install --save styled-normalize
```

```sh
yarn add styled-normalize
```

### styled-components v4 / v5

Package exported `normalize` and `Normalize`. `Normalize` is a component with global styles. `normalize` is a css-normalize content to interpolate into styled component.

Use as component:

```js
// index.js
import React from 'react'
import ReactDOM from 'react-dom'
import { Normalize } from 'styled-normalize'

import { App } from './app'

const Root = () => (
  <React.Fragment>
    <Normalize />
    <App />
  </React.Fragment>
)

ReactDOM.render(<Root />, document.querySelector('#root'))
```

Also you can use [`createGlobalStyle`](https://www.styled-components.com/docs/api#createglobalstyle) API:

```js
// styles/index.js
import { createGlobalStyle } from 'styled-components'
import { normalize } from 'styled-normalize'

export const GlobalStyle = createGlobalStyle`
  ${normalize}

  // You can continue writing global styles here
  body {
    padding: 0;
    background-color: black;
  }
`

// index.js
import React from 'react'
import ReactDOM from 'react-dom'

import { GlobalStyle } from './styles'
import { App } from './app'

const Root = () => (
  <React.Fragment>
    <GlobalStyle />
    <App />
  </React.Fragment>
)

ReactDOM.render(<Root />, document.querySelector('#root'))
```

You can also use named imports:

```js
// ES Modules
import { normalize, Normalize } from 'styled-normalize'

// CommonJS
const { normalize, Normalize } = require('styled-normalize')
```

### styled-components v3

If you want to use `styled-normalize` with `styled-components@v3` you should use `prev` npm tag.

```bash
npm install styled-normalize@prev
```

> v3 don't supports `createGlobalStyle` API.

## Version

__NO SEMVER!__

Why? Because X.Y numbers in `vX.Y.Z` version matches X.Y in `normalize.css`

## License

The [MIT License](LICENSE)

