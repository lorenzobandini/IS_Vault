Separazione tra interfaccia che è visibile e la sua implementazione che invece è privata e invisibile.

Così vengono rappresentati i componenti e i moduli come scatole nere trattate come fornitori e clienti di funzionalità ma di cui è nota solo l'interfaccia.

Sono quindi tenuti nascosti algoritmi usati e strutture dati interne tra cui variabili.

L'**interfaccia** di un'unità di progettazione esprime ciò che l'unità offre o richiede e ciò è visibile anche alle altre unità.
Il **corpo** contiene l'implementazione degli elementi dell'interfaccia ed è nascosto alle altre unità.

I vantaggi dell'Information Hiding sono:
- Comprensibilità: nessuna necessità di comprendere i dettagli implementativi di un’unità per usarla
- Manutenibilità: si può cambiare l'implementazione di una unità senza dover modificare le altre
- Lavoro in team: la separazione corpo-iterfaccia facilita lo sviluppo da parte di persone che lavorano in modo indipendente, il riuso, le riparazioni e le riconfigurazioni
- Sicurezza: I dati di una unità possono essere modificati solo da funzioni interne alla stessa, e non dall’esterno

L'incapsulamento è una proprietà del linguaggio di programmazione che permette agli oggetti di mantenere al loro interno sia gli attributi che i metodi cioè permette l'information hiding ma non lo garantisce, infatti se per errore di un programmatore dichiara una variabile senza esplicitare che sia privata, questa non sarà nascosta.

Le tecniche più note per l'information hiding sono i getters (get()) e i setters (set()), metodi standard per accedere agli attributi di una classe potendo nascondere i dati.
Più precisamente:
- La get() non deve deve modificare lo stato dell'oggetto ed è buona pratica che quello che restituisca sia un valore e non un riferimento
- La set() permette una modifica controllata delle proprietà di un oggetto cambiando il suo stato ma con possibili controlli