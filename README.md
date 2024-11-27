# PHP & HTML Tags and Functions Tutorial

Questa repository offre una guida completa ai tag HTML più famosi e alle funzioni PHP più comuni, con esempi e spiegazioni.

## Indice
1. [HTML Tags](#html-tags)
    - [Tag di Struttura](#tag-di-struttura)
    - [Formattazione del Testo](#formattazione-del-testo)
    - [Liste](#liste)
    - [Form](#form)
    - [Multimedia](#multimedia)
    - [Tabelle](#tabelle)
    - [Altri Tag Comuni](#altri-tag-comuni)
      
2. [Funzioni PHP](#funzioni-php)
    - [Variabili](#variabili)
    - [Iterazioni](#iterazioni)
    - [Gestione Array](#gestione-array)
    - [Gestione Date e Ore](#gestione-date-e-ore)
    - [Altro](#altro)

---

## HTML Tags

### Tag di Struttura

- **`<html>`**: Racchiude tutto il contenuto di un documento HTML.
    ```html
    <html lang="it">
        ...
    </html>
    ```
    L'attributo `lang` specifica la lingua principale del contenuto.

- **`<head>`**: Contiene meta-informazioni sul documento (titolo, codifica, link a fogli di stile e script).
    ```html
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="style.css">
        <title>Il mio sito</title>
    </head>
    ```

- **`<link>`**: Collega risorse esterne, come fogli di stile CSS.
    ```html
    <link rel="stylesheet" href="style.css">
    ```

- **`<title>`**: Specifica il titolo della pagina web, visibile nella scheda del browser.
    ```html
    <title>Il mio sito</title>
    ```

- **`<style>`**: Contiene regole CSS scritte direttamente all'interno del documento HTML.
    ```html
    <style>
        body {
            background-color: lightgray;
        }
    </style>
    ```

- **`<header>`**: Contiene informazioni introduttive o elementi di navigazione.
    ```html
    <header>
        <h1>Benvenuti</h1>
        <nav>
            <ul>
                <li><a href="#sezione1">Sezione 1</a></li>
                <li><a href="#sezione2">Sezione 2</a></li>
            </ul>
        </nav>
    </header>
    ```

- **`<body>`**: Contiene il contenuto visibile della pagina.
    ```html
    <body>
        <h1>Intestazione</h1>
        <p>Contenuto della pagina.</p>
    </body>
    ```

- **`<main>`**: Identifica il contenuto principale della pagina.
    ```html
    <main>
        <section>
            <h2>Sezione Principale</h2>
            <p>Testo principale.</p>
        </section>
    </main>
    ```

- **`<footer>`**: Contiene il piè di pagina della pagina web.
    ```html
    <footer>
        <p>&copy; 2024 - Tutti i diritti riservati</p>
    </footer>
    ```

---

### Formattazione del Testo

- **`<h1>` – `<h6>`**: Intestazioni da grande (`<h1>`) a piccola (`<h6>`).
    ```html
    <h1>Intestazione Principale</h1>
    <h2>Seconda Intestazione</h2>
    ```

- **`<p>`**: Paragrafo.
    ```html
    <p>Questo è un paragrafo.</p>
    ```

- **`<br>`**: Va a capo senza aggiungere spazi.
    ```html
    Riga 1<br>Riga 2
    ```

- **`<hr>`**: Inserisce una linea orizzontale.
    ```html
    <hr>
    ```

- **`<strong>`**: Rende il testo importante (in grassetto).
    ```html
    <strong>Testo importante</strong>
    ```

- **`<i>`**: Rende il testo in corsivo.
    ```html
    <i>Testo in corsivo</i>
    ```

---

### Liste

- **`<ul>`**: Lista non ordinata (punti elenco).
    ```html
    <ul>
        <li>Elemento 1</li>
        <li>Elemento 2</li>
    </ul>
    ```

- **`<ol>`**: Lista ordinata (numerata).
    ```html
    <ol>
        <li>Elemento 1</li>
        <li>Elemento 2</li>
    </ol>
    ```

- **`<li>`**: Elemento della lista.
    ```html
    <li>Elemento</li>
    ```

---

### Form

- **`<label>`**: Etichetta per i campi di input.
    ```html
    <label for="email">Email:</label>
    <input type="email" id="email">
    ```

- **`<input>`**: Campo di input generico (con dettagli sui tipi disponibili sotto).
    ```html
    <input type="text" name="username">
    ```

- **`<button>`**: Pulsante cliccabile.
    ```html
    <button>Invia</button>
    ```

- **`<select>`**: Crea un menu a discesa.
    ```html
    <select name="opzioni">
        <option value="1">Opzione 1</option>
        <option value="2">Opzione 2</option>
        <option value="3">Opzione 3</option>
    </select>
    ```

- **`<option>`**: Rappresenta un'opzione all'interno di un menu `<select>`.
    ```html
    <option value="1">Opzione 1</option>
    ```

---

### Multimedia

- **`<img>`**: Mostra un'immagine.
    ```html
    <img src="immagine.jpg" alt="Descrizione dell'immagine">
    ```

- **`<video>`**: Inserisce un video.
    ```html
    <video controls>
        <source src="video.mp4" type="video/mp4">
        Il tuo browser non supporta i video HTML5.
    </video>
    ```
    - **`controls`**: L'attributo `controls` è un attributo booleano che, se presente, aggiunge un'interfaccia utente predefinita (come play, pausa, volume, e barra di avanzamento) per il controllo del video. Se non è presente, l'utente non avrà un'interfaccia di controllo.
    - **`source`**: L'elemento `<source>` viene utilizzato per specificare il file video. L'attributo `src` indica la posizione del video e l'attributo `type` specifica il tipo del file video, per esempio `video/mp4`.
      
    - **Tipi di `controls`**: Il controllo predefinito aggiunge tutti i comandi disponibili come play, pausa, volume e avanzamento. È anche possibile aggiungere ulteriori attributi per personalizzare l'interfaccia utente:
        - **`autoplay`**: Se presente, il video inizia a riprodursi automaticamente quando la pagina viene caricata.
        - **`loop`**: Se presente, il video si ripete automaticamente quando arriva alla fine.
        - **`muted`**: Se presente, il video inizia senza audio.


---

### Tabelle

- **`<table>`**: Crea una tabella.
    ```html
    <table>
        <thead>
            <tr>
                <th>Nome</th>
                <th>Età</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Mario</td>
                <td>25</td>
            </tr>
        </tbody>
    </table>
    ```

- **`<thead>`**: Contiene l'intestazione della tabella.
- **`<tbody>`**: Contiene il corpo della tabella.
- **`<tfoot>`**: Contiene il piè di pagina della tabella.
- **`<th>`**: Intestazione di colonna.
- **`<tr>`**: Riga della tabella.
- **`<td>`**: Cella della tabella.

---

### Tipi di `<input>`

- **`type="email"`**: Campo per l'inserimento di un'email.
    ```html
    <input type="email" placeholder="nome@email.com">
    ```

- **`type="hidden"`**: Campo nascosto, utile per inviare dati aggiuntivi nei form.
    ```html
    <input type="hidden" name="nome" value="Denis">
    ```

- **`type="number"`**: Campo per l'inserimento di numeri.
    ```html
    <input type="number" min="1" max="100" step="1">
    ```

- **`type="password"`**: Campo per inserire una password (i caratteri inseriti saranno nascosti).
    ```html
    <input type="password" placeholder="Inserisci la tua password">
    ```

- **`type="radio"`**: Pulsante di selezione singola (radio button).
    ```html
    <input type="radio" name="sesso" value="maschio"> Maschio
    <input type="radio" name="sesso" value="femmina"> Femmina
    ```

- **`type="range"`**: Campo per selezionare un valore da un intervallo.
    ```html
    <input type="range" min="0" max="100" step="5">
    ```

- **`type="submit"`**: Pulsante per inviare il form.
    ```html
    <input type="submit" value="Invia">
    ```

- **`type="text"`**: Campo di input di testo generico.
    ```html
    <input type="text" placeholder="Scrivi qui">
    ```

- **`type="url"`**: Campo per l'inserimento di un URL.
    ```html
    <input type="url" placeholder="https://esempio.com">
    ```

- **`type="button"`**: Pulsante cliccabile che non invia il form.
    ```html
    <input type="button" value="Clicca qui">
    ```

- **`type="checkbox"`**: Casella di selezione multipla.
    ```html
    <input type="checkbox" name="accetto" value="si"> Accetto i termini e condizioni
    ```
### Altri Tag Comuni

- **`<div>`**: Contenitore generico.
    ```html
    <div class="box">Contenuto</div>
    ```

- **`<span>`**: Contenitore inline generico.
    ```html
    <span style="color: red;">Testo rosso</span>
    ```

- **`<script>`**: Inserisce codice JavaScript.
    ```html
    <script>
        console.log("Hello World!");
    </script>
    ```

- **`<section>`**: Raggruppa contenuti relativi.
    ```html
    <section>
        <h2>Sezione</h2>
        <p>Testo nella sezione.</p>
    </section>
    ```

- **`<center>`**: Allinea il contenuto al centro (deprecato, usa CSS).
    ```html
    <center>Contenuto centrato</center>
    ```

- **`<svg>`**: Per grafica vettoriale.
    ```html
    <svg width="100" height="100">
        <circle cx="50" cy="50" r="40" fill="blue" />
    </svg>
    ```

---


## Funzioni PHP

### Variabili
- **`$variabile`**: Crea una variabile.
    ```php
    $variabile = "valore";
    echo variabile; // Output: valore
    ```
- **`array`**: Crea un'array.
    ```php
    $array = array("elemento1", "elemento2", "elemento3");
    echo $array[0]; // Output: elemento1
    ```
- **`array associativo`**: Crea un'array associativo.
    ```php
    $persona = ["nome" => "Denis", "eta" => 19];
    echo $persona["nome"];  // Stampa "Denis"
    ```

### Iterazioni
- **`if`**: viene utilizzata per eseguire un blocco di codice se una condizione è vera.
    ```php
    $eta = 19;
    if ($eta >= 18) {
    echo "Sei maggiorenne";
    }
    ```
- **`foreach`**: viene utilizzata per eseguire un blocco di codice se una condizione è vera.
    ```php
    $frutti = ["Mela", "Banana", "Arancia"];
    foreach ($frutti as $frutto) {
    echo $frutto . "<br>";  // Stampa ogni frutto
    }
    ```
    
### Gestione Array
- **`array_push()`**: Aggiunge un elemento alla fine di un array.
    ```php
    $frutta = ["mela", "banana"];
    array_push($frutta, "arancia");
    ```
- **`count()`**: Restituisce il numero di elementi in un array.
    ```php
    echo count($frutta); // Output: 3
    ```

### Gestione Date e Ore
- **`date()`**: Restituisce la data e l'ora formattate.
    ```php
    echo date("Y-m-d"); // Output: 2024-11-27
    ```
    
### Altro
- **`echo`**: Stampa una stringa o variabile.
    ```php
    echo "Ciao, mondo!";
    ```
- **`form`**: Viene utilizzato per raccogliere dati da un utente e inviarli al server.
    ```php
    <form method="POST" action="processa.php">
    <input type="text" name="username">
    <input type="submit" value="Invia">
    </form>
    ```
- **`method`**: L'attributo method specifica il metodo (GET o POST) per inviare i dati.
- **`action`**: L'attributo action indica l'URL del server che riceverà i dati.
  
- **`isset()`**: Verifica se una variabile è definita.
    ```php
    $nome = "Mario";
    echo isset($nome); // Output: 1 (true)
    ```
    
- **`explode()`**: Divide una stringa in un array, utilizzando un delimitatore.
    ```php
    $stringa = "mela,banana,arancia";
    $array = explode(",", $stringa); // ["mela", "banana", "arancia"]
    ```
    
- **`implode()`**: Unisce gli elementi di un array in una stringa, utilizzando un delimitatore.
    ```php
    $array = ["mela", "banana", "arancia"];
    $stringa = implode(",", $array); // "mela,banana,arancia"
    ```
    
- **`$_POST`**: è una variabile globale che contiene i dati inviati tramite il metodo POST di un form HTML.
    ```php
    <form method="POST" action="output.php">
    <input type="text" name="username">
    <input type="submit" value="Invia">
    </form>

    // In output.php
    $username = $_POST['username'];
    ```
    
- **`$_GET`**: è una variabile globale che contiene i dati inviati tramite il metodo GET di un form HTML o nella URL.
    ```php
    <form method="GET" action="output.php">
    <input type="text" name="username">
    <input type="submit" value="Invia">
    </form>

    // In output.php
    $username = $_GET['username'];
    ```

- **`is_numeric()`**: verifica se una variabile è numerica (sia intero che decimale).
    ```php
    $numero = "123";
    if (is_numeric($numero)) {
    echo "È un numero.";
    } else {
    echo "Non è un numero.";
    }
    ```

- **`number_format()`**: formatta un numero con un numero specificato di decimali.
    ```php
    $numero = 1234.5678;
    echo number_format($numero, 2); // Output: 1,234.57
    ```

- **`htmlspecialchars()`**: converte i caratteri speciali in entità HTML per evitare vulnerabilità di tipo XSS (Cross-site Scripting).
    ```php
    $stringa = "<script>alert('Ciao!');</script>";
    echo htmlspecialchars($stringa); // Output: &lt;script&gt;alert('Ciao!');&lt;/script&gt;
    ```
---

