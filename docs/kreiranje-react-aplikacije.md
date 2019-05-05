## Kreiranje React aplikacije

Ranije je za instaliranje i podešavanje Reacta bilo potrebno mnogo zavisnih elemenata o kojima je trebalo voditi računa. Međutim, vremenom je smišljen standardni način za brzo pokretanje Reacta. Modul `create-react-app` omogućuje kreiranje nove React aplikacije bez konfigurisanja. 

## Instalacija i pokretanje

Prvo, potrebno je instalirati `create-react-app`:

```
npm install -g create-react-app
```

Ovde instaliramo node.js modul `create-react-app` globalno. Nakon što je `create-react-app` instaliran, kreiraćemo novu React aplikaciju:

```
create-react-app zdravo-react
cd zdravo-react/
npm start
```

Nakon pokretanja, otvorite adresu http://localhost:3000/ da biste videli aplikaciju. 

## Struktura projekta

Kad otvorimo projekat u editoru, videćemo mnoge fajlove i foldere koji su već kreirani:

- `node_modules` je folder u kom su instalirane biblioteke, odnosno zavisnosti potrebne za pokretanje projekta.
- `src` je direktorij u kom radimo, koji sadrži izvorni kod. Najvažniji fajlovi su `App.js` i `index.js`.
- Datoteka `/public/index.html` mora da sadrži samo osnovni element `div` sa id `root`, koji će biti korišćen kao okvir za React aplikaciju.
