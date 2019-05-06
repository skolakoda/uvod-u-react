# Šta je React komponenta?

**Komponenta je element web stranice (poput dugmeta ili zaglavlja), koji sadrži sopstveni prikaz i funkcionalnost.**

React komponente se mogu praviti pomoću funkcije ili pomoću klase.

## Komponenta kao funkcija

Obična funkcija postaje React komponenta ukoliko vraća JSX (format nalik HTML-u). Na primer: 

```jsx
function Pozdrav() {
  return <hl>Zdravo Svete</hl>
}
```

Unutar Reacta, komponentu `Pozdrav` možemo koristiti kao tag, na sledeći način:

```html
<div>
  <Pozdrav/>
<div>
```

> Potrebno je da naziv komponente počinje velikim slovom. React tretira tagove koji počinju malim slovom kao standardne HTML tagove, a očekuje da prilagođene komponente počinju velikim slovom. 

## Komponenta kao klasa

Komponentu možemo kreirati i pomoću klase. Ona mora nasleđivati `React.Com­ponent` i imati `render` metodu koja vraća JSX. Na primer:

```jsx
class Pozdrav extends React.Component {
  render(){
    return <hl>Zdravo Svete</hl>
  }
}
```
