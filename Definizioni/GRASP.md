GRASP è un'altra famiglia di principi di progettazione, acronimo di:
- **G**eneral
- **R**esponsability
- **A**ssignment
- **S**oftware
- **P**atterns

Durante la fase di analisi sono stati definiti casi d'uso e il dominio mentre nella fase di progettazione si devono assegnare i metodi alle classi e dire come gli oggetti collaborano per realizzare i casi d'uso.

Con realizzazione del caso d'uso si intende descrivere come un particolare caso d'uso è realizzato nel progetto in termini di oggetti collaborativi. Il lavoro di realizzazione del caso d'uso è un'attività di progettazione, il progetto cresce con ogni nuova realizzazione del caso d'uso.

Per realizzare i casi d'uso si usano diagrammi di interazione e pattern e si assegnano le responsabilità alle classi.

Le responsabilità sono legate al dominio del problema. Nel modello di progettazione, le responsabilità sono gli obblighi che un oggetto ha, definiti in termini di comportamento.
Esistono due tipi principali di responsabilità:
- Fare: 
	- fare qualcosa come creare un oggetto o fare un calcolo
	- iniziare l'azione di altri oggetti
	- controllare e coordinare le attività di altri oggetti
- Conoscere
	- i dati privati
	- gli oggetti correlati
	- dati che possono derivare o calcolare

La traduzione delle responsabilità del dominio del problema in classi e metodi è influenzata dalla granularità della responsabilità.
Una responsabilità non è un metodo ma i metodo sono implementati per soddisfare le responsabilità.

L'approccio GRASP si basa sull'assegnazione delle responsabilità; si definiscono così gli oggetti e i loro metodi guidati da pattern di assegnazione delle responsabilità.

I 9 pattern di GRASP sono:
- Creator
- Information Expert
- High Cohesion
- Low Coupling
- Controller
- Polymorphism
- Indirection
- Pure Fabrication
- Protected Variations

