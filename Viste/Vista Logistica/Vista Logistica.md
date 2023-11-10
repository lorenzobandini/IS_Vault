Chiamata anche vista di deployment (di dislocazione) e descrive l'allocazione del software su ambienti di esecuzione e permette quindi di valutare prestazioni e affidabilità.

Gli elementi sono:
- Software: artefatti, un'informazione fisica che viene utilizzata o prodotta da un processo di sviluppo software o dal funzionamento di un sistema
- Dell'ambiente: hardware, ambiente di esecuzione

La relazione è un elemento software allocato a elemento dell'ambiente.

Serve per l'analisi delle prestazione e per la guida all'installazione.

La notazione [[UML]] per documentare la vista di dislocazione utilizziamo:
- Parallelepipedo per denominare un nodo hardware o, in generale, un ambiente di esecuzione
- Artefatti
- La relazione tra nodi hardware sono connessioni fisiche o protocolli di comunicazione

![[Pasted image 20231108183618.png]]

Normalmente si parla di deployment di componenti, mentre in realtà si disloca un artefatto. L'artefatto è una copia di un'implementazione di componente che è stata installata/rilasciata su un particolare computer/ambiente di esecuzione.
L'installazione avviene su un ambiente di esecuzione (nodo).
Un artefatto manifesta un componente, e un componente che esiste a run time è un'istanza creata a partire da un artefatto in un ambiente di esecuzione.