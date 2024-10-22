# Nuovo progetto in Laravel 10 + Bootstrap 5.x + SASS

Prima di tutto eseguiamo il solito comando di installazione di npm

- Eseguiamo `npm install`
- Eseguiamo il comando per aggiungere sass `npm i --save-dev sass` o  `npm install -D sass`
- Modifichiamo la cartella `resources/css` in `resources/scss` 
- Modifichiamo il file `resources/css/app.css` in `resources/scss/app.scss` 
- Modifichiamo il file vite.config.js aggiungendo a plugins il path giusto da `'resources/css/app.css'` a `'resources/scss/app.scss'` ,
- Aggiungiamo un alias al file vite.config.js per facilitare l'accesso a resources:
```
resolve: {
        alias: {
            '~resources' : "/resources/"
        }
} 
```
- Aggiungiamo `import "~resources/scss/app.scss";` al file  `resources/js/app.js`
- Aggiungiamo `@vite("resources/js/app.js")` ad ogni layout della nostra applicazione
- Aggiungiamo a `resources/js/app.js` una direttiva per la corretta gestione delle immagini
```
  import.meta.glob([
      '../img/**'
  ]);
```
- Aggiungiamo la riga `package-lock.json` al file `.gitignore`

