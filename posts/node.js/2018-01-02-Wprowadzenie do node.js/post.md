W dzisiejszym wpisie chciałbym przedstawić node.js. Jest to środowisko uruchomieniowe dla języka JavaScript oparte na silniku Chrome V8 pozwalające na wykonywanie aplikacji w JS poza przeglądarką.

Przykładowy serwer wykorzystujący **Express** nasłuchujący na porcie 3000:

```javascript
  const express = require('express');
  const app = express();

  app.get('/', (req, res) => {
    res.send('Hello!');
  })
  
  app.listen(3000);
```

Na każde zapytanie serwer odpowie wiadomością *Hello!*.

#### Zobacz też:
Więcej o node.js:
  - [Oficjalna strona](https://nodejs.org/en/)
  - [Tutorial W3Schools](https://www.w3schools.com/nodejs/)

Więcej o Express:
  - [Oficjalna strona](https://expressjs.com/)
  - [Dokumentacja Express](https://expressjs.com/en/4x/api.html)