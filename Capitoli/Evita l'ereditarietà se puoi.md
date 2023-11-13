L'ereditarietà è un meccanismo attraverso il quale una classe può ereditare attributi e metodi da un'altra classe, chiamata classe genitore o superclasse. La classe che eredita i membri di un'altra classe è detta classe figlia o sottoclasse.

Questa relazione permette alle classi figlie di ereditare i membri della classe genitore e di estenderli o sovrascriverli per adattarli alle proprie esigenze, permettendo la condivisione di funzionalità comuni e la creazione di una gerarchia di classi.

L'ereditarietà da la possibilità di:
- Vari tipi di realizzazioni:
	- Certificare la conformità di un'implementazione a un'interfaccia
	- Astrazione/Polimorfismo
	- Da classe a interfaccia
- Estensioni:
	- Dichiarare pubblicamente la compatibilità covariante di due tipi 
	- Interfaccia verso interfaccia (ma anche classe, poiché le classi sono anch'esse interfacce)
- Riuso di codice:
	- Ereditare metodi dalle classi genitori
	- Classe a classe
- Documentazione:
	- Stabilisce un organizzazione di tipo
	- Crea una forte relazione concettuale tra tipi

Ma non ti permette di non averle tutte. Infatti certe volte una di queste può non essere necessario ma paghi lo stesso il costo di ognuna di esse rendendo il codice più difficile da modificare o leggere.
A volte una di queste non viene applicata ma siamo costretti a preservare la compatibilità di tipo anche se non è perfetta.

Quindi in conclusione:
- Implementare interfacce è corretto e necessario per l'inversione delle dipendenze e il polimorfismo per cui si utilizza la programmazione generica quando disponibile e il polimorfismo è parametrico.
- Estendere le interfacce può essere accettabile in alcuni casi per implicare la compatibilità ma bisogna fare attenzione a far crescere troppo le interfacce. L'ereditarietà non può essere interrotta in quanto fa parte dell'interfaccia pubblica.
- Non introdurre relazioni di sotto tipo solo perché qualcosa "dovrebbe essere" qualcos'altro. Aspetta una ragione pratica. Non implementare interfacce di cui non hai ancora bisogno.
- Evita l'ereditarietà come meccanismo di riuso del codice. Preferisci la composizione e dividi il comportamento in più piccole interfacce per consentire l'implementazione in più classi piccole non correlate.

I vantaggi della composizione sull'ereditarietà sono:
- La dipendenza tra classi può essere astratta con un'interfaccia, mentre l'ereditarietà richiede un'istanza specifica. Ciò aiuta, ad esempio, nei test, così come per altre ragioni in cui opera il DIP ([[Dependency Inversion Principle]]).
- Favorisce la suddivisione del codice e il riutilizzo poiché una classe può dipendere da diverse altre classi (ma può ereditarne solo una).
- Rende la dipendenza un dettaglio di implementazione piuttosto che parte dell'interfaccia pubblica (il che consente di cambiarla/rimuoverla in seguito).
- Consente di modificare le dipendenze in un secondo momento nel ciclo di vita dell'istanza, mentre l'istanza della classe base è fissata al momento della costruzione.