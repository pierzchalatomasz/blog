W niniejszym poście przedstawię bibliotekę React stworzoną przez Facebook'a i pokażę jak wykorzystać ją do tworzenia aplikacji front-endowych.

React pozwala na tworzenie komponentów komunikujących się przez tzw. **propsy**. Są to wartości, które można przekazać do potomnych komponentów podobnie jak atrybuty w HTML. 

Po zmianie wartości propsów lub stanu wewnętrznego komponentu wywoływana jest metoda render odpowiedzialna za wyświetlenie danego komponentu.

Rozważmy poniższy komponent *Hello* wyświetlający tekst powitalny z imieniem podanym przez propsy (`this.props.name`).

```javascript
import React from 'react';
import PropTypes from 'prop-types';

export default class Hello extends React.Component {
  static propTypes = {
    name: PropTypes.string,
  };

  render() {
    return (
      <div>Hello {this.props.name}!</div>
    );
  }
}
```

Poniższy komponent wyświetli komponent **Hello** z propsem **name** o wartości *"Bartek"*.

```javascript
import React from 'react';
import Hello from './Hello';

export default class Home extends React.Component {
  render() {
    const name = "Bartek";

    return (
      <Hello name={name} />
    );
  }
}
```

#### Zobacz też:
Więcej o React:
  - [Oficjalna strona](https://reactjs.org/)
  - [Tutorial](https://reactjs.org/tutorial/tutorial.html)