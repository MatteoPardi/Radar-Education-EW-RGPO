# AGENTS.md - Guida per Agenti AI

## 📋 Contesto del Progetto

Questo progetto è una **presentazione interattiva HTML** progettata per spiegare a studenti di liceo (16 anni) il concetto di **inganno radar** e **guerra elettronica**, con particolare focus sulla tecnica **RGPO (Range Gate Pull-Off)**.

### Obiettivo Educativo

La presentazione mira a:
- Spiegare in modo semplice e intuitivo come funziona un radar
- Mostrare cosa vede un operatore radar quando un bersaglio viene rilevato
- Introdurre il concetto di **inganno radar**: come un bersaglio può simulare la presenza di un finto bersaglio trasmettendo opportunamente onde che imitano un eco radar
- Illustrare la tecnica **RGPO** come esempio classico di guerra elettronica

### Pubblico Target

- **Età**: 16 anni (studenti di liceo)
- **Conoscenze**: Non esperti di elettronica o radar
- **Linguaggio**: Italiano semplice, colloquiale, divulgativo
- **Approccio**: Metafore e visualizzazioni intuitive, niente formule matematiche

---

## 🎯 Struttura della Presentazione

La presentazione è composta da **5 slide** che seguono una progressione logica:

### Slide 1: "Come fa un radar a vedere gli aerei?"
**Obiettivo**: Introdurre il concetto base del radar come "occhio tecnologico"
- Il radar invia impulsi invisibili (onde radio)
- Gli impulsi rimbalzano sugli oggetti e tornano indietro
- Il radar misura il tempo di ritorno per calcolare la distanza

### Slide 2: "Un bersaglio: un pallino sullo schermo"
**Obiettivo**: Mostrare la rappresentazione visiva di un bersaglio
- Un aereo reale appare come un singolo pallino luminoso sullo schermo radar
- L'operatore non vede l'aereo fisico, ma solo un punto sullo schermo
- Questo concetto è fondamentale per capire l'inganno

### Slide 3: "Due aerei, due echi, due pallini"
**Obiettivo**: Mostrare lo scenario "onesto" con due bersagli reali
- Un'onda trasmessa può rimbalzare su più oggetti
- Ogni oggetto produce un eco separato
- Il radar mostra due pallini distinti sullo schermo

### Slide 4: "Inganno radar: un solo aereo che sembra due"
**Obiettivo**: Introdurre il concetto di inganno
- Un aereo nemico può essere equipaggiato con un sistema di guerra elettronica
- Quando viene illuminato dal radar, può trasmettere falsi echi
- Il radar riceve due segnali (uno vero, uno finto) e mostra due pallini
- **Il radar non può distinguere visivamente tra un eco vero e uno finto**

### Slide 5: "RGPO: far scappare un bersaglio fantasma"
**Obiettivo**: Spiegare la tecnica RGPO (Range Gate Pull-Off)
- Il pallino finto viene inizialmente posizionato vicino a quello vero
- Impulso dopo impulso, il pallino finto viene spostato sempre più lontano
- Il radar può "agganciare" e inseguire il bersaglio fantasma
- Nel frattempo, il bersaglio vero può cambiare rotta o fuggire

---

## 🎨 Specifiche Tecniche e Grafiche

### Stile Visivo
- **Tema**: Aeronautica / Guerra elettronica
- **Sfondo**: Scuro (blu notte / nero) - `#0a0e27`
- **Colori principali**:
  - **Ciano** (`#00ffff`): Impulsi radar in uscita, titoli
  - **Verde** (`#00ff88`): Echi radar, schermo radar, elementi positivi
  - **Arancione** (`#ffaa00`): Echi falsi/ingannatori
  - **Rosso** (`#ff4444`): Aerei nemici

### Elementi Visivi Ricorrenti
1. **Stazione radar**: Antenna rotante stilizzata in basso a sinistra
2. **Aerei militari**: Disegni semplici ma realistici visti dall'alto
3. **Schermo radar circolare**: Display tipo "film" con pallini luminosi, in basso a destra
4. **Onde radar**: Impulsi sferici che si espandono radialmente dal punto di origine

### Animazioni Chiave
- **Impulsi in movimento**: Onde che partono dal radar verso i bersagli e tornano indietro
- **Pallini che compaiono**: I blip appaiono sullo schermo radar quando gli echi vengono ricevuti
- **Sweep radar**: Linea rotante che passa sopra lo schermo radar
- **Movimento RGPO**: Pallino finto che si sposta progressivamente verso l'esterno dello schermo
- **Traccia del movimento**: Scia lasciata dal pallino in movimento

### Testo e Contenuti
- **Massimo 3 bullet point per slide**
- **Frasi brevi, poche parole**
- **Niente gergo specialistico**
- **Note oratore**: Spiegazioni dettagliate per il presentatore (non visibili al pubblico)

---

## 💻 Implementazione Tecnica

### File Principale
- **`presentazione_inganno_radar.html`**: File HTML completo con CSS e JavaScript inline
  - Presentazione a schermo intero
  - Navigazione tra slide con pulsanti e tastiera
  - Animazioni JavaScript per onde radar e blip
  - Sistema di note oratore (toggle con pulsante o tasto 'N')

### Funzionalità Implementate
1. **Sistema di navigazione**: Frecce, spazio, pulsanti per navigare tra slide
2. **Animazioni dinamiche**: Onde radar che si espandono, blip che appaiono, movimento RGPO
3. **Mappatura posizionale**: I blip sullo schermo radar sono posizionati in base alla posizione reale degli aerei
4. **Note oratore**: Sistema per mostrare/nascondere le spiegazioni dettagliate

### Struttura del Codice
- **CSS**: Stili per tutti gli elementi visivi, animazioni keyframe
- **HTML**: Struttura delle 5 slide con contenuti
- **JavaScript**: 
  - Gestione navigazione slide
  - Animazioni delle onde radar (`createWave()`)
  - Posizionamento blip (`positionBlipOnScreen()`)
  - Animazioni specifiche per ogni slide (`animateSlide()`)

---

## 🔧 Come Lavorare su Questo Progetto

### Per Agenti AI che Modificano il Codice

1. **Rispettare lo stile esistente**:
   - Mantenere la palette di colori (ciano, verde, arancione)
   - Conservare il tema scuro e l'estetica "aeronautica"
   - Usare le stesse convenzioni di naming per classi CSS

2. **Animazioni**:
   - Le onde radar devono espandersi radialmente dal punto di origine
   - La velocità delle onde deve essere costante e realistica
   - I blip devono apparire sincronizzati con la ricezione degli echi
   - Per l'RGPO, il movimento deve essere progressivo e visibile

3. **Posizionamento**:
   - Il radar è sempre in basso a sinistra
   - Lo schermo radar è sempre in basso a destra
   - Gli aerei sono posizionati nella parte superiore/destra
   - I blip sullo schermo devono riflettere la posizione reale degli aerei

4. **Testi e Contenuti**:
   - Mantenere il linguaggio semplice e divulgativo
   - Massimo 3 bullet point per slide
   - Le note oratore devono essere dettagliate ma accessibili

5. **Compatibilità**:
   - Il codice deve funzionare in browser moderni
   - Usare CSS3 e JavaScript ES6+
   - Nessuna dipendenza esterna (tutto inline)

### Aree di Possibile Miglioramento

- **Animazioni più fluide**: Ottimizzare le animazioni delle onde per performance migliori
- **Interattività**: Aggiungere possibilità di pausa/play delle animazioni
- **Responsive design**: Adattare la presentazione per schermi di dimensioni diverse
- **Accessibilità**: Migliorare supporto per screen reader e navigazione da tastiera
- **Effetti sonori**: Aggiungere suoni opzionali per impulsi radar (se richiesto)

### File di Riferimento

- **`prompt_inganno_v01.md`**: Contiene le specifiche originali e dettagliate per ogni slide
- **`presentazione_inganno_radar.html`**: Implementazione attuale della presentazione

---

## 📚 Concetti Chiave da Comprendere

### Radar (Radio Detection and Ranging)
- Sistema che invia onde radio e analizza gli echi riflessi
- Misura il tempo di andata e ritorno per calcolare la distanza
- L'operatore vede solo punti (blip) su uno schermo, non gli oggetti reali

### Eco Radar
- Segnale riflesso da un oggetto che torna al radar
- Il tempo di ritorno indica la distanza dell'oggetto
- Ogni oggetto produce un eco separato

### Inganno Radar
- Tecnica di guerra elettronica
- Un bersaglio trasmette falsi echi che imitano quelli di un bersaglio reale
- Il radar non può distinguere tra eco vero e finto basandosi solo sul segnale ricevuto

### RGPO (Range Gate Pull-Off)
- Tecnica specifica di inganno radar
- Il bersaglio crea un eco finto vicino a quello vero
- Progressivamente, l'eco finto viene ritardato, simulando un bersaglio che si allontana
- Il radar può "agganciare" il bersaglio fantasma e perdere quello vero

---

## 🎓 Obiettivi Educativi Finali

Dopo aver visto questa presentazione, gli studenti dovrebbero:
1. Capire come funziona un radar in modo intuitivo
2. Comprendere che l'operatore radar vede solo punti su uno schermo
3. Capire che un bersaglio può ingannare il radar trasmettendo falsi echi
4. Comprendere il concetto di RGPO come esempio di guerra elettronica
5. Apprezzare che la guerra elettronica non distrugge il radar, ma ne inganna la percezione

---

## ⚠️ Note Importanti per gli Agenti

- **Non usare formule matematiche** nelle spiegazioni visibili
- **Mantenere il linguaggio semplice** e accessibile a studenti di 16 anni
- **Le animazioni devono essere chiare e didattiche**, non solo decorative
- **Ogni slide deve costruire sul concetto precedente** in modo logico
- **Il focus è sulla comprensione intuitiva**, non sulla precisione tecnica
- **Tutti i testi devono essere in italiano**

---

## 📝 Convenzioni di Codice

- **Naming**: Usare nomi descrittivi in inglese per classi CSS e funzioni JavaScript
- **Commenti**: Commentare le sezioni complesse, specialmente le animazioni
- **Struttura**: Mantenere CSS, HTML e JavaScript ben organizzati e leggibili
- **Performance**: Ottimizzare le animazioni per evitare lag o jank

---

*Questo documento è stato creato per aiutare gli agenti AI a comprendere il contesto e gli obiettivi del progetto, permettendo loro di lavorare efficacemente sul codice della presentazione.*

