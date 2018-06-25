# styled-normalize

Normalize file for [styled-components](https://styled-components.com/) CSS-in-JS library.

The original `normalize.css` is pulled from [necolas/normalize.css](https://github.com/necolas/normalize.css), and parsed into styled ready format.


## Usage

```sh
npm install --save styled-normalize
```

### JavaScript

```javascript
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
import { normalize, version } from 'styled-normalize'

// CommonJS
const { normalize, version } = require('styled-normalize')

assert(version)
```

## License

The [MIT License](LICENSE)

