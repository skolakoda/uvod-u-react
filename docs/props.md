# Props (ulaz komponente)

**React komponente se mogu konceptualno smatrati JavaScript funkcijama. One koriste proizvo­ljan broj ulaza, kao i funkcije. Ulazni podaci komponente su organizovani u props objekat.**

## Komponenta kao funkcija

Kod komponente kao funkcije, ulazni podaci su smešteni u `props` objekat:

```jsx
function Pozdrav(props) {
  return <hl>Zdravo, {props.ime}</hl>
}
```

Funkcija prima ulaz pod nazivom `props` i vraća `JSX`. Važno je napomenuti da komponenta ne može da modifikuje ulazni `props` objekat. Unutar JSX-a možemo koristiti izraze unutar vitičastih zagrada. 

## Prosleđivanje svojstava

Iz roditeljske komponente možemo proslediti svojstvo komponenti `Pozdrav` na sledeći način:

```jsx
render(){
  return (
    <div>
      <Pozdrav ime="Nikola"/>
    <div>
  )
}
```

## Komponenta kao klasa

Unutar komponente kao klase, `props` objektu pristupamo preko ključne reči `this`, na sledeći način:

```jsx
class Pozdrav extends React.Component {
  render(){
    return <hl>Zdravo, {this.props.ime}</hl>
  }
}
```

## Literatura

- Ved Antani, Stojan Stefanov, *Objektno-orjentisan JavaScript*, Beograd, 2017.
