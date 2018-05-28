# Različiti načini kreiranja React komponenti

Postoje različiti načini kreiranja React komponenti, a glavni su:

- ES5 createClass
- ES6 class
- ES6 stateless function

## Komponenta kao ES6 klasa (*Stateful Component*)

```jsx
import React, {Component} from 'react'

export default class Developer extends Component {
  render() {
    return (
      <div className="dev-wrapper">
        <h3 className="dev-name">{this.props.name}</h3>
        <img alt="developer" src={this.props.image} />
        <p>Moje glavne veštine su {this.props.skills}.</p>
      </div>
    )
  }
}
```

## Komponenta kao čista funkcija (*Stateless Functional Components*)

```js
import React from 'react'

const Developer = props => (
  <div className="dev-wrapper">
    <h3 className="dev-name">{props.name}</h3>
    <img alt="developer" src={props.image} />
    <p>Moje glavne veštine su {props.skills}.</p>
  </div>
)

export default Developer
```
