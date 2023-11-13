Il Singleton è un Pattern Creazionale con l'intento di:
- Assicurare che una classe abbia solo un'istanza
- Fornire un punto di accesso globale ad essa

E le motivazioni sono che:
- A volte vogliamo che esista solo un'istanza di una classe nel sistema;
- Abbiamo bisogno di rendere facilmente accessibile quella singola istanza
- Vogliamo garantire che non possano essere create istanze aggiuntive della classe

Gli oggetti unici non sono rari.
La maggior parte degli oggetti in un'applicazione hanno una responsabilità unica.
Tuttavia, le classi Singleton sono relativamente rare.
Il fatto che un oggetto/classe sia unico non significa che il pattern Singleton sia in atto.

Per impedire ad altri sviluppatori di costruire nuove istanze della tua classe si crea un singolo costruttore con accesso privato e si rende l'istanza unica disponibile solo con un metodo "Get()"

Piuttosto che creare un'istanza singleton in anticipo, si attende finche l'istanza non è necessaria per la prima volta e i motivi sono che:
- Potrebbe non esserci abbastanza informazioni per istanziare un singleton durante il tempo di inizializzazione statica.
- Se il singleton richiede molte risorse e potrebbe non essere necessario.

La classe [[UML]] di Singleton si presenta così:

![[Pasted image 20231113170607.png]]

Si hanno problemi con Multi-threading poiché nel caso di più di un processore, il metodo `getInstance()` potrebbe essere chiamato più o meno contemporaneamente portando alla creazione di più di un'istanza.

Le possibili soluzioni sono
1. Passare a un'istanza creata in modo più diligente piuttosto che in modo pigro (Semplice, ma potrebbe essere allocata memoria non utilizzata)
2. Sincronizzare il metodo `getInstance()` (La sincronizzazione può ridurre le prestazioni del sistema)
3. Utilizzare il double-checked locking (L'idea è evitare la costosa sincronizzazione per tutte le invocazioni del metodo tranne la prima)

E se volessimo essere in grado di sottoclassare il Singleton e avere l'unica istanza essere un'istanza della sottoclasse possiamo fare in due modi diversi:
1. Fare in modo che il metodo statico `getInstance()` determini la particolare istanza della sottoclasse da istanziare. Questo potrebbe essere fatto tramite un argomento o una variabile d'ambiente. In questo caso, i costruttori delle sottoclassi non possono essere privati e quindi i clienti potrebbero istanziare altre istanze delle sottoclassi.
2. Fare in modo che ogni sottoclasse fornisca un metodo statico `getInstance()`. Ora i costruttori delle sottoclassi possono essere privati.

Ogni oggetto di una classe ha la propria copia di tutte le variabili di istanza di quella classe.
Tuttavia, in certi casi, tutti gli oggetti di una classe dovrebbero condividere una sola copia di una particolare variabile. Tali variabili sono chiamate variabili statiche. Un programma contiene solo una copia di ciascuna variabile statica di una classe in memoria, indipendentemente dal numero di oggetti della classe istanziati.
Una variabile statica rappresenta informazioni a livello di classe. Tutti gli oggetti della classe condividono lo stesso dato statico.
Gli attributi statici pubblici di una classe possono essere accessibili tramite il nome della classe e l'operatore punto al contrario degli attributi statici privati che possono essere accessibili solo attraverso i metodi e le proprietà di quella classe.

I **Vantaggi** nell'uso dei Singleton sono:
- Puoi passare l'oggetto come parametro a un altro metodo.
- Puoi derivare una classe di base.
- Puoi utilizzare un pattern factory per costruire la tua istanza (e/o scegliere quale classe istanziare).