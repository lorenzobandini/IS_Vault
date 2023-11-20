Il pattern Decorator consente di aggiungere dinamicamente responsabilità aggiuntive a un oggetto. I Decorator offrono un'alternativa flessibile alla creazione di sottoclassi per espandere le funzionalità di un oggetto.

I partecipanti sono:
- Componente: Interfaccia degli oggetti decorati.
- ConcreteComponent: Classe di base degli oggetti che possono ricevere nuove responsabilità.
- Decorator: Definisce un'interfaccia conforme a quella comune e mantiene un riferimento a un oggetto di tipo componente (che può essere già decorato o meno).
- ConcreteDecorator: Definisce una nuova responsabilità.