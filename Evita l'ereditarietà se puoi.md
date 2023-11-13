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

Implementare interfacce è corretto e necessario per l'inversione delle dipendenze e il polimorfismo.
Utilizza la programmazione generica quando disponibile e il polimorfismo è parametrico (ad esempio, nei contenitori).
Estendere le interfacce può essere accettabile in alcuni casi per implicare la compatibilità (per esempio, se si desidera esprimere che la versione 2 di un'interfaccia è compatibile con la versione 1), ma fai attenzione a far crescere troppo le interfacce (in particolare, non sarai in grado di capire se i clienti della versione 100 hanno ancora bisogno dei metodi della versione 1). L'ereditarietà non può essere interrotta in quanto fa parte dell'interfaccia pubblica.
Non introdurre relazioni di sotto tipo solo perché qualcosa "dovrebbe essere" qualcos'altro. Aspetta una ragione pratica. Non implementare interfacce di cui non hai ancora bisogno.
Evita l'ereditarietà come meccanismo di riuso del codice.
Preferisci la composizione (vedi sotto).
Dividi il comportamento in più piccole interfacce per consentire l'implementazione in più classi piccole non correlate.