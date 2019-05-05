# Stanje

**Stanje komponente je objekat koji sadrži vrednosti. Kada se bilo koja od varijabli unutar stanja promeni, komponenta se ponovo renderuje.**

Stanje možemo postojati samo u klasi. Stanje nije javno, ono pripada komponenti koja ga u potpunosti kontroliše.

## Primer

Možemo da promenimo prethodni primer tako što ćemo koristiti stanje, na sledeći način:

```jsx
class Pozdrav extends React.Component {
  constructor(props) {
    super(props)
    this.state = {
      poruka: "Dobar dan"
    }
  }

  render (){
    return <h1>(this.state.poruka}, {this.props.ime} </h1>
  }
}
```

Postoji nekoliko važnih stvari na koje treba obratiti pažnju ovde. Prvo pozivamo `constructor` metodu da bismo inicijalizovali `this.state`. Takođe pozi­vamo osnovni konstruktor nadklase `super()`, kome prosleđujemo `props`. Nakon što pozovemo `super()`, inicijalizujemo početno stanje.

U metodu `render` koristimo svojstvo stanja `poruka` na sledeći način: `{this.state.poruka}`.

## Ažuriranje stanja

Nakon što podesimo početno stanje, možemo ga ažurirati tako što ćemo dodati polje za unos, a kada se promeni stanje polja za unos, ažuriraćemo stanje. Na primer:

```jsx
class Pozdrav extends React.Component {
  constructor(props) {
    super (props)
    this.state = {
      poruka: "Dobar dan"
    }
  }

  azurirajPoruku(e){
    this.setState({
      poruka: e.target.value,
    })
  }

  render() {
    return (
      <div>
        <input onChange={this.azurirajPoruku.bind(this)}/>
        <h1>{this.state.poruka}, {this.props.ime} </h1>
      </div>
    )
  }
}
```

Ovde dodajemo polje za unos i ažuriramo stanje kada se aktivira događaj `onChange` polja za unos. Metoda `azurirajPoruku()` nam služi da bismo ažu­rirali stanje, tako što unutar nje pozivamo ugrađenu metodu `this.setState`, kojoj prosleđujemo novo stanje u vidu objekta.
