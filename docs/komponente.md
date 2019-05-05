# Šta je React komponenta?

**Komponenta je bilo koji element web stranice (poput dugmeta), koji sadrži sopstveni prikaz, stil i funkcionalnost.**

React komponente se mogu konceptualno smatrati JavaScript funkcijama. One koriste proizvo­ljan broj ulaza, kao i funkcije.

## Komponenta kao funkcija

Funkcija može da služi kao React komponenta. Ulazni podaci komponente su smešteni u `props` objekat. Na primer: 

```jsx
function Pozdrav(props) {
  return <hl>Zdravo, {props.ime}</hl>
}
```

Ova funkcija prima ulaz pod nazivom `props` i vraća `JSX` (nestandarnu sintaksu koju koristi React). Važno je napomenuti da komponenta ne može da modifikuje svoj ulazni objekat `props`. Unutar JSX-a možemo koristiti varijable pomoću vitičastih zagrada. 

U roditeljskoj komponenti možemo upotrebiti komponentu `Pozdrav` na sledeći način:

```jsx
render(){
  return (
    return <Pozdrav ime="Nikola"/>
  )
}
```

Potrebno je da naziv komponente počinje velikim slovom. React tretira tagove koji počinju malim slovom kao standardne HTML tagove, a očekuje da prilagođene komponente počinju velikim slovom. 

## Komponenta kao klasa

Takođe, možemo kreirati komponentu pomoću klase. Ona mora biti potklasa klase `React.Com­ponent`. Ekvivalent prethodne funkcije `Pozdrav` je sledeći:

```jsx
class Pozdrav extends React.Component {
  render(){
    return <hl>Zdravo, {this.props.ime}</hl>
  }
}
```

## Literatura

- Ved Antani, Stojan Stefanov, *Objektno-orjentisan JavaScript*, Beograd, 2017.
