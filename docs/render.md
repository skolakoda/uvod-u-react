# Render

**`render` je najvažniji i jedini obavezan metod svake React komponente.** 

Iz metoda `render` vraćamo opis onoga što želimo da prikažemo, a React iscrtava prikaz. React će automatski obnoviti prikaz svaki put kada se stanje podataka promeni.

## JSX

Za prikaz komponenti, React koristi posebnu sintasku nalik HTML-u, pod nazivom JSX. U pozadini, ova sintaksa se prevodi u validan Javascript.

Na primer, JSX izraz `<hl>Hello World</hl>` se tokom izvršenja pretvara u:

```js
React.createElement('h1', null, 'Hello World')
```

## Jedan korenski čvor

Metod `render` može da vrati samo jedan čvor. Dobili bi grešku ako pokušamo da vratimo dva čvora iz render metode:

```jsx
render(){
    return <h1>Hello World</h1><p>ReactRocks</p>
  )
}
```

Ovo se može lako rešiti. Možemo da ugnjezdima oba čvora u treći čvor:

```jsx
render(){
  return (
    <div>
      <hl>Hello World</hl>
      <p>React Rocks</p>
    </div>
  )
}
```
