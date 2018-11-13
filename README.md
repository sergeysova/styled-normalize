# styled-normalize

CSS-normalize library for [styled-components](https://styled-components.com/).

The original `normalize.css` is pulled from [necolas/normalize.css](https://github.com/necolas/normalize.css), and parsed into styled ready format.


## Usage

```sh
npm install --save styled-normalize
```

### styled-components v4

styled-components [createGlobalStyle documentation](https://www.styled-components.com/docs/api#createglobalstyle)

> This is just usage example

```js
// ----- index.js
import React from 'react'
import { Normalize } from 'styled-normalize'

import { App } from './app'

const Root = () => (
  <React.Fragment>
    <Normalize />
    <App />
  </React.Fragment>
)
```

Also you can use `injectGlobal` API:

```js
// ----- styles/index.js
import styledNormalize from 'styled-normalize'
import { injectGlobal } from 'styled-components'

injectGlobal`
  ${styledNormalize}

  // You can continue writing global styles
  body {
    padding: 0;
    background-color: black;
  }
`
```

You can also use named imports:

```js
// ES Modules
import { normalize, Normalize } from 'styled-normalize'

// CommonJS
const { normalize, Normalize } = require('styled-normalize')

injectGlobal` ${normalize} `
<Normalize />
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

