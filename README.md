# Vite Boolando

## Milestone 1
- Creare un nuovo progetto utilizzando Vite e Vue 3 e definire i componenti necessari per strutturare il layout.
- Riprendere l'esercizio precedente di cui si ha già html e css, e suddividerlo in componenti provando a sfruttare SASS per rendere lo stile più leggibile e flesibile.

## Milestone 2
- Aggiungere un array di prodotti e stamparlo in pagina usando un componente ProductCard e le props necessarie per visualizzarlo correttamente.
- Ciascun oggetto dell'array avrá le proprietá necessarie per stampare la card di prodotto.

## Milestone 3
- Installare la libreria json-server e aggiungere al package.json lo script “serve” necessario per avviarlo: `json-server --watch db.json`.
- Impostare uno stato globale: quali dati globali gestisce l'app?
- Fare in modo che la nostra App, all’avvio, non legga più i dati dall’array statico presente nel componente, ma dall’API che ci rende disponibile json-server.

## Milestone 4
- Fare in modo che al click sul nome del prodotto nella card venga emesso un evento 'showProduct' verso il componente App.
- In App, quando riceviamo l’evento, apriamo una modale che mostra tutte le informazioni testuali del prodotto.
- Nella modale è presente una X (o un pulsante) per chiuderla.