# NeuroCrono

## Analisi delle funzionalità 

### 1. Modalità flusso

Stabilire la modalità di default secondo la teoria del pomodoro (ovvero 25 minuti di concentrazione seguiti da 5 minuti di pausa e ogni due ore ovvero 3 stint la pausa sarà di 20 minuti), avendo così la modalità **NeuroFlow Session** con:

- NeuroBurst: della durata di 25 minuti per la concentrazione
- NeuroPause: della durata di 5 minuti di pausa

Fornire la possibilità di personalizzare completamente le sessioni di concentrazioni e le sessioni di pausa, con la possibilità di decidere quanti stint dovrà avere un ciclo.

> Ad esempio voglio modificare gli stint con 20 minuti di concentrazione e 10 minuti di pausa e ogni 3 stint aumentare la pausa di altri 10 minuti.

> Oppure voglio che abbia un unico ciclo composto da 50 minuti per la concentrazione e 10 minuti di pausa.

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
| L'orario in cui è stato avviato uno stint | Time format **hh:mm**
| Numero di minuti per la messa in pausa della sessione di concentrazione | Numerico intero
| Numero di pause saltate | Numerico intero
| Numero dei minuti delle pause saltate | Numerico intero
| Numeno di minuti per le pause allungate | Numerico intero
| Feedback da parte dell'utente. Per maggiori info vedi [Feedback e distrazione](#6-feedback-e-distrazione) | String + Contatore

Per la relazione e l'incrocio di dati sarà necessario implementare un sistema di storaging maggiore.

### 3. Smart break

Nella fase di pausa verranno implementati dei suggerimenti su tecniche di respirazione, metodi per il rilassamento mentale e muscolare, meditazione oppure delle frasi motivazoinali
e aforismi. 

### 4. Blocco distrazioni

Possibilità di bloccare notifiche da siti e app *solo* durante i periodi di concentrazione, ma con la possibilità di creare una whitelist per notifiche ritenute necessarie.

### 5. Sincronizzazione tra più device

Poter lanciare l'app su diversi dispositivi condividendo gli stessi dati e aggiornandoli separatamente.

### 6. Feedback e distrazione

### 7. NeuroAdaptive AI
