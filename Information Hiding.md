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

