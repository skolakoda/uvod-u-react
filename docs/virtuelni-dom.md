# Virtuelni DOM

DOM (objektni model dokumenta) je struktura stabla HTML elemenata na stranici. DOM API-ji, kao što je `getElementById()`, omogućavaju izbor i modifikaciju elemenata DOM stabla. 

Međutim, premeštanje i ažuriranje DOM-a nisu mnogo brze operacije. DOM stablo za veću stranicu može biti veoma veliko. Kada nam je potreban kompleksan korisnički interfejs, ažuriranje DOM eleme­nata može biti sporo i naporno. Možemo skratiti sintaksu za DOM manipulaciju pomoću *jQuery*-a i drugih biblioteka, ali DOM struktura je, sama po sebi, prilično ograničena.

Šta bi bilo kada ne bismo morali da stalno manipulišemo DOM da bi modifikovali ele­mente? Ako bismo samo deklarisali kako komponenta treba da izgleda i dozvolili da neko drugi upravlja logikom za njeno prikazivanje? React omogućava upravo to. Takođe, React radi nešto prilično pametno da bi rešio problem sa performansama.

React koristi nešto što se zove **virtuelni DOM** (*virtual DOM*), koji predstavlja jednostavnu apstrakciju HTML DOM-a. Možemo razmišljati o virtuelnom DOM-u kao o kopiji lokalne memorije DOM-a. React koristi tu kopiju da bi obavio sva izračunavanja koja su potrebna za prikaz stanja komponente korisničkog interfejsa.

React koristi Virtual DOM i diferencijalni algoritam, pa će ažuriranje komponenata biti predvidivo, a u isto vreme dovoljno brzo za aplikacije visokih performansi.

## Literatura

- Ved Antani, Stojan Stefanov, *Objektno-orjentisan JavaScript*, Beograd, 2017.
