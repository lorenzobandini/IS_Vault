Quando i pattern di creazione di classi si concentrano sull'uso dell'ereditarietà per decidere l'oggetto da istanziare si parla di Factory Method.

Nella definizione ufficiale il metodo di fabbrica permette alle sottoclassi di decidere quale classe istanziare.
Decidono non perché le classi stesse decidano a tempo di esecuzione ma perché il creatore è scritto senza conoscenza dei prodotti effettivi che saranno creati, scelta determinata dalla sottoclasse che viene utilizzata.

Il suo pattern è:

![[Pasted image 20231113162826.png]]

I partecipanti sono:
- **Prodotto**: Definisce l'interfaccia per il tipo di oggetti che il metodo di fabbrica crea.
- **Prodotto Concreto**: Implementa l'interfaccia del Prodotto.
- **Creatore**: Dichiara il metodo di fabbrica, che restituisce un oggetto del tipo Prodotto.
- **Creatore Concreto**: Sovrascrive il metodo di fabbrica per restituire un'istanza di un Prodotto Concreto.

Utilizza il pattern del Factory Method in una delle seguenti **situazioni**:
- Una classe non può prevedere la classe degli oggetti che deve creare.
- Una classe desidera che le sue sottoclassi specifichino gli oggetti che crea.

I **vantaggi** sono:
- Il codice diventa più flessibile e riutilizzabile eliminando l'istanziazione di classi specifiche dell'applicazione.
- Il codice lavora solo con l'interfaccia della classe Prodotto e può funzionare con qualsiasi classe Prodotto Concreto che supporti questa interfaccia.

Gli **svantaggi** sono che i clienti potrebbero dover sottoclassare la classe Creatore solo per istanziare un particolare Prodotto Concreto.

Per le **questioni implementative**:
- Il Creatore può essere astratto o concreto.
- Ci chiediamo se il metodo fabbrica possa essere in grado di creare più tipi di prodotti e in tal caso abbiamo bisogno di un costrutto if-else per decidere quale oggetto creare.

Esistono anche le Pure Fabrication, un pattern [[GRASP]] che vuole risolvere il problema di non vi

Pattern GRASP
Problema:
◦ Non violare l'Alta Coesione e il Basso Accoppiamento
Soluzione:
◦ Assegnare un insieme altamente coeso di responsabilità a una
classe artificiale
◦ che non rappresenta nulla nel dominio del problema,
◦ al fine di supportare alta coesione, basso accoppiamento e
riutilizzo.