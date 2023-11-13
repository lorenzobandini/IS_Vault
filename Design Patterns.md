Esistono una serie di regole pratiche che il progettiste può seguire per costruire ogni cosa. Queste regole pratiche sono i design patterns e sono state definite grazie a secoli di esperienza.

>"Ogni modello descrive un problema che si verifica ripetutamente nel nostro ambiente e quindi descrive il nucleo della soluzione a quel problema, in modo tale che tu possa utilizzare questa soluzione un milione di volte, senza mai farlo allo stesso modo due volte"

\- Christopher Alexander, 1977

I design pattern si applicano nella fase di design.
In tutto i Design Patterns, derivanti da  sono 23 e sono suddivisi in base al loro scopo:
- **Creazionali**: propongono soluzioni per creare oggetti
	- **Singleton:** Assicura che una classe abbia una sola istanza e fornisce un punto di accesso globale a tale istanza.
	- **Factory Method:** Definisce un'interfaccia per la creazione di un oggetto, ma delega la scelta del tipo specifico dell'oggetto alle sottoclassi.
	- **Abstract Factory:** Fornisce un'interfaccia per la creazione di famiglie di oggetti correlati o dipendenti senza specificare le classi concrete.
- **Comportamentali**: propongono soluzioni per gestire il modo in cui vengono suddivise le responsabilità delle classi e degli oggetti
	-  **Observer:** Consente a un oggetto, chiamato "soggetto", di notificare gli "osservatori" quando il suo stato cambia.
	- **Strategy:** Definisce una famiglia di algoritmi, incapsula ciascuno di essi e li rende interscambiabili.
	- **Template Method:** Come accennato in precedenza, definisce lo scheletro di un algoritmo in una classe base delegando alcune operazioni alle sottoclassi.
- **Strutturali**: propongono soluzioni per la composizione strutturale di classi e oggetti
	- **Adapter:** Converte l'interfaccia di una classe in un'altra interfaccia che il cliente si aspetta.
	- **Decorator:** Aggiunge funzionalità a oggetti esistenti dinamicamente, senza modificarne la struttura di base.
	- **Composite:** Tratta le singole istanze di oggetti e le collezioni di oggetti allo stesso modo, consentendo di trattare in modo uniforme le strutture ad albero.

I pattern nei software servono perché, anche se progettare software OO è ancora più difficile se si tenta di realizzarlo in maniere che sia riutilizzabile, i progettisti esperti riutilizzano le soluzioni che hanno funzionato in passato, i sistemi OO ben strutturati infatti hanno modelli ricorrenti di classi e oggetti.
La conoscenza degli schemi che hanno funzionato in passato consente al progettista di essere più produttivo e ai progetti risultanti di essere più flessibili e riutilizzabili.

Il modello del GoF