# @mybricks/rxui

> Responsive framework for React programing，like the Mobx but not only Mobx

## Usage

```tsx
import {render, useObservable} from '@mybricks/rxui'

render(<App/>, document.querySelector('#containerDomId'))

function App() {
  const obs = useObservable(class {
    num: number = Math.random()
  })

  return (
    <div>
      {obs.num}
      <button onClick={() => obs.num = Math.random()}>ChangeValue</button>
    </div>
  )
}
```