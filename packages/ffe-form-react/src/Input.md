_The bread and butter_ av skjemaene våre.

Vi har tre varianter av inputfelt:

1. standard
2. inline
3. text-like

_Standard_ og _inline_ er mest relevant for utviklere. De ser helt like ut, men opprører seg annerledes i samspillet
med andre elementer på siden, for eksempel [tooltip](#tooltip).

```js
const { Input } = require('.');

<React.Fragment>
    <Label htmlFor="input-first-name">Fornavn</Label>
    <Input id="input-first-name" />
</React.Fragment>
```

_Text-like_-varianten er designet for å kunne brukes som en del av en setning med et minimum av ramme rundt. Det er opp til en utvikler å sette bredden på dette elementet, siden det vil variere fra gang til gang hva man ønsker.

```js
const { Input } = require('.');

<p className="ffe-body-paragraph">
    Jeg er <Input
        aria-label="Skriv inn alder"
        style={{ width: '47px' }}
        textLike={true}
    /> år gammel
</p>;
```