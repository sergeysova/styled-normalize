# styled-normalize

Single file with normalize.css for your [styled-components](https://styled-components.com/)

Original normalize.css copied from [necolas/normalize.css](https://github.com/necolas/normalize.css)


## Usage

```bash
npm install --save styled-normalize styled-components
```

### JavaScript

```javascript
// ----- styles/index.js
import styledNormalize from 'styled-normalize'
import { injectGlobal } from 'styled-components'

export default () => injectGlobal`
  ${styledNormalize}

  body {
    padding: 0;
    background-color: black;
  }
`

// ----- client.js
// ... imports
import baseStyles from './styles/index'

const render = () => {
  baseStyles()

  ReactDOM.render(<AppContainer />, document.getElementById('app-root'))
}

render()
```

## ServerSide Rendering

Styled-components supports SSR, you can [read discussion](https://github.com/styled-components/styled-components/issues/386) or [open RURARAR](https://github.com/lestad/rurarar/)
