# NeuroCrono

## Analisi delle funzionalità 

### 1. Cronometro intelligente

Questà sarà la funzionalità cardine del software con cui l'utente potrà direttamente interagire. Sostanzialmente sarà un cronometro programmabile sia per i momenti di concentrazione sia per i momenti di pausa, questo software si basa sulla teoria del pomodoro (25 +5).

Verrà stabilità una modalità di default, chiamate **NeuroFlow Session**, con:

- **NeuroBurst**: della durata di 25 minuti per la concentrazione
- **NeuroPause**: della durata di 5 minuti di pausa

Verra inoltre fornita la possibilità di **aggiungere e personalizzare** completamente le sessioni di concentrazioni e le sessioni di pausa, con la possibilità di decidere quanti stint dovrà avere un ciclo.

> Ad esempio voglio modificare gli stint con 20 minuti di concentrazione e 10 minuti di pausa e ogni 3 stint aumentare la pausa di altri 10 minuti.

> Oppure voglio che abbia un unico ciclo composto da 50 minuti per la concentrazione e 10 minuti di pausa.

- L'utente dovrà avere anche la possibilità di mettere in pausa o annullare sia le sessioni di concentrazione sia quelle di pausa.

> [!NOTE]
> Per **stint** intendiamo il tempo che comprende il periodo di concentrazione più il periodo di pausa (NeuroBurst + NeuroPause)
>
> Per **ciclo** intendiamo l'intero ciclo di sessione che comprende l'insieme degli stint.

Tutte queste personalizzazioni dovranno essere salvate in modo che l'utente possa avviarle, modificarle o eliminarle.

### 2. Analitiche per monitoraggio

Analizzare dati creando grafici giornalieri, settimanali e mensili con dei report che indichino:

- il tempo totale in concentrazione
- in pausa
- quanti stint sono stati completati
- quanti cicli sono stati completati
- quali sono i giorni in cui è stato utilizzato il software
- a che ora è stato utilizzato

L'aggiunta delle seguenti funzionalità per migliorare ulteriormente l'esperienza utente:

1. Avere la possibilità di taggare ogni ciclo con il tipo di attività svolta.
2. Fornire una timeline per vedere in quali giorni e orari hai completato più task o l'utente è riuscito a completare più stint o cicli.
3. Creare una lista di minacce per l'attenzione personalizzabili dall'utente con dei reminder all'inizio degli stint. Ad esempio "Ricordami di togliere il telefono dalla portata di mano"
4. L'utente potrà fermare la sessione di concentrazione o di pausa, saltare la pausa o prolungarla.

Ci sarà una ulteriore raccolta dati per i seguenti campi:
-  numero di minuti della sessione di concentrazione messa in pausa
-  numero di pause saltate e minuti relativi saltati
-  numero di minuti per le pause allungate

> [!TIP]
> Eventualmente pensare di integrare una semplice todo list, con elenco delle task da svolgere con relative scadenze (*implementare i reminder*) e l'insieme delle task di una stessa categoria
> rappresenta un obiettivo, qual'ora si completassero tutte le task l'obiettivo sarebbe portato a termine. Così da poter creare un manager per
> il tracciamento delle task svolte e obiettivi raggiunti.

**RIASSUNTO DEI DATI DA MEMORIZZARE**

| DATO  | TIPO |
|-------|------|
| Tempo totale di concentrazione  | Numerico intero 
| Tempo totale di pausa  | Numerico intero
| Numero totale di stint completati | Numerico intero 
| Numero totale di cicli completati | Numerico intero
| I relativi giorni in cui è stato completato uno (o più) stint/cicl* | Stringa + Contatore
| Gli orari in cui è stato *avviato* e *terminato* uno stint | Time format **hh:mm**
| Gli orari in cui è stato *avviato* e *terminato* un ciclo | Time format **hh:mm**
| Numero di minuti per la messa in pausa della sessione di concentrazione[^1] | Numerico intero
| Numero di pause saltate[^2] | Numerico intero
| Numero dei minuti delle pause saltate[^2] | Numerico intero
| Numeno di minuti per le pause allungate[^2] | Numerico intero
| Feedback da parte dell'utente. Per maggiori info vedi [Feedback e distrazione](#6-feedback-e-distrazione) | String + Contatore

[^1]: Questo dato verrà sommato per semplicità con il numero di minuti totale delle pause

[^2]: Questi dati saranno utili per capire quali pause sono state saltate o quali sono state allungate al fine di allenare [NeuroAdaptive](#7-neuroadaptive-ai) per fornire consigli sempre più veritieri e attendibili.

### 3. Smart break

Nella fase di pausa verranno implementati dei suggerimenti su tecniche di respirazione, metodi per il rilassamento mentale e muscolare, meditazione oppure delle frasi motivazoinali
e aforismi. 

### 4. Blocco distrazioni

Possibilità di bloccare notifiche da siti e app *solo* durante i periodi di concentrazione, ma con la possibilità di creare una whitelist per notifiche ritenute necessarie.

### 5. Sincronizzazione tra più device

Poter lanciare l'app su diversi dispositivi condividendo gli stessi dati e aggiornandoli separatamente.

### 6. Feedback e distrazione

Verranno poste delle domande all'utente per capire qual'è stato il suo grado di concentrazione, se si è distratto e se risponde affermativamente quante volte, se alla fine del ciclo è stanco oppure se prima della fine di un ciclo era già stanco.

In base alle risposte verrà allenata una mini AI per fornire consigli automatici in base alle risposte date e ai dati precendenti analizzati.

> Se ad esempio l'AI analizza e riscontra che il lunedì alla stessa ora con lo stesso meotodo l'utente avverte stanchezza informa l'utente e fornisce dei suggerimenti.

### 7. NeuroAdaptive AI

### 8. Task manager

Creando una sezione a parte per la creazione di tasks e goals fornendo la possibilità di:

> [!INFO]
> Per **task** intendiamo una singola azione da completare.
>
> Mentre per **goal** intendiamo l'insieme di delle task accomunate da un intento o fissate per il raggiungimento di un obiettivo.

> Facciamo un esempio: devo studiare più argomenti per una stessa materia, in questo caso il goal sarebbe "passare l'esame di matematica" e le task sarebbero gli argomenti da studiare "ricerca operativa" - "storia della ricerca operativa" - "eccetera".

L'utente sarà dunque in grado di:

- creare nuove task / goal
- modificarl*
- eliminarl*
- flaggarle le task completate
- deflaggare le task

Quando le task verranno completate verrà fatto in modo che l'utente capisca che quel goal è stati completato e può eliminarlo.

L'utente potrà iniziare un ciclo direttamnte dalla task scelta o dal goal, avendo la scelta di flaggare le task o il goal se è riuscito effettivamente a completarle. 

Verrano fornite ulteriori informazioni come ad esempio quante ore l'utente ha impiegato per completare una task e il tempo totale che ha impiegato per completare un goal che sarà la somma dei minuti delle varie task.