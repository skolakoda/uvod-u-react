
## render

Metod render vraća opis onoga što želite da prikažete, a zatim react koristi taj opis i prika­
zuje ga na ekranu. Preciznije rečeno, render vraća react element, koji predstavlja jednosta­
van opis onoga što treba prikazati. Većina programera koristi
posebnu sintaksu pod nazivom JSX, koja olakšava pisanje ovih struktura. Sintaksa `<div/>` se pretvara tokom izvršenja u `React.createElement('div')`. JSX izraz `<hl>Hello World</hl>` pretvara se tokom izvršenja u sledeće:

```js
React.createElement('h1', null, 'Hello World')
```

Metod `render` react komponente može da vrati samo jedan čvor. Ako iz render metode pokušate da vratite dva čvora, dobićete grešku.:

```js
return <h1>Hello World</h1><p>ReactRocks</p>
```

Problem se može lako rešiti. Možemo da postavimo čvorove u nadređeni čvor, koji ćemo, zatim, vratiti iz funkcije render:

```js
render(){
  return (
    <div>
      <hl>Hello World</hl>
      <p>React Rocks</p>
    </div>
  )
}
```
