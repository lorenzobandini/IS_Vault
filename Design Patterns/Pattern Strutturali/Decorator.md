Il pattern Decorator consente di aggiungere dinamicamente responsabilità aggiuntive a un oggetto. I Decorator offrono un'alternativa flessibile alla creazione di sottoclassi per espandere le funzionalità di un oggetto. Conosciuto anche come Wrapper.

La struttura è: 

![[Pasted image 20231120103603.png]]

I partecipanti sono:
- Componente: Interfaccia degli oggetti decorati.
- ConcreteComponent: Classe di base degli oggetti che possono ricevere nuove responsabilità.
- Decorator: Definisce un'interfaccia conforme a quella comune e mantiene un riferimento a un oggetto di tipo componente (che può essere già decorato o meno).
- ConcreteDecorator: Definisce una nuova responsabilità.

Solitamente è possibile inserire i decorator in modo trasparente e il client non deve mai sapere che sta trattando con un decorator. Tuttavia, se scrivi del codice dipendente da tipi specifici, possono verificarsi problemi.

I vantaggi sono riguardante l'eredità statica:
- Molto più facile da utilizzare rispetto all'eredità multipla
- Può essere utilizzato per combinare e abbinare funzionalità
- È possibile aggiungere la stessa proprietà più volte
- Consente di aggiungere facilmente nuove funzionalità incrementalmente

Le cattive conseguenze però sono:
- Se il Decorator è complesso, diventa costoso utilizzarlo in grandi quantità.
- Un Decorator e il suo componente non sono identici
- Dal punto di vista dell'identità dell'oggetto, un componente decorato non è identico al componente stesso
- Non fare affidamento sull'identità dell'oggetto quando si utilizzano i decorator
- Molti oggetti piccoli che rendono il sistema molto denso e difficile da imparare e debuggare

Quando applichiamo il decorator pattern bisogna considerare:
- Conformità dell'interfaccia: L'interfaccia di un oggetto decoratore deve conformarsi all'interfaccia del componente che decora
- Omettere le classe astratta Decorator: Se è necessaria solo una responsabilità, evita di definire una classe astratta Decorator ma unisci la responsabilità del Decorator nella ConcreteDecorator
- Mantenere leggere le classi Component: La classe Component è ereditata da componenti e decoratori. La classe Component dovrebbe essere dedicata alla definizione di un'interfaccia, senza altre funzioni.
- Cambiare la superficie dell'oggetto rispetto alle sue parti interne: Le classi Decorator dovrebbero agire come uno strato superficiale su un oggetto. Se c'è la necessità di cambiare le parti interne dell'oggetto, utilizza il pattern [[Strategy]].
