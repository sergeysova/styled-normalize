# normalize-styled

Single file with normalize.css for your [styled-components](https://styled-components.com/)


## Usage

```bash
npm install --save normalize-styled styled-components
```

### JavaScript

```javascript
// ----- styles/index.js
import normalizeStyled from 'normalize-styled'
import { injectGlobal } from 'styled-components'

export default () => injectGlobal`
  ${normalizeStyled}

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
