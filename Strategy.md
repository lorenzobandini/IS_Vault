Il design pattern comportamentale Strategy definisce una famiglia di algoritmi, incapsularne ognuno e renderlo intercambiabile. Ciò rende molto indipendente l'algoritmo dal client che lo usa.
Un programma potrebbe dover fornire diverse varianti di un algoritmo o di un comportamento.
La soluzione è incapsulare le diverse variazioni in classe separate e creare un accesso uniforme ad ognuno di esse.

La struttura quindi sarebbe:

![[Pasted image 20231113113957.png]]

Dove:
- Strategy: definisce un interfaccia comune che supporta tutti gli algoritmi
- ConcreteStrategy: ognuno delle concrete strategie implementate negli algoritmi
- Context: Contiene la referenza ad un oggetto strategia e può definire un interfaccia che consenta alla strategia di accedere ai propri dati invece di passarli come argomenti quando si richiama la strategia metodi

Il pattern Strategy è utile quando:
- Molti classi correlate differiscono solo nel loro comportamento.
- Hai bisogno di diverse varianti di un algoritmo.
- Un algoritmo utilizza dati di cui i client non dovrebbero essere a conoscenza.
- Si utilizza il pattern Strategy per evitare di esporre strutture dati complesse specifiche dell'algoritmo.
- Una classe definisce molti comportamenti e questi appaiono come molteplici istruzioni condizionali nelle sue operazioni. Invece di molti condizionali, sposta i rami condizionali correlati nella propria classe Strategy.

I benefici sono:
- Fornisce un'alternativa alla creazione di sottoclassi della classe Context per ottenere una varietà di algoritmi o comportamenti.
- Elimina grandi istruzioni condizionali.
- Offre una scelta di implementazioni per lo stesso comportamento.

Gli svantaggi sono:
- Aumenta il numero di oggetti.
- Tutti gli algoritmi devono utilizzare lo stesso Strategy.

Diverse ConcreteStrategy potrebbero aver bisogno di dati diversi. Molto probabilmente, alcune ConcreteStrategy non utilizzeranno tutti i dati passati attraverso l'interfaccia generica.
- Di conseguenza: il contesto crea e inizializza parametri che non verranno mai utilizzati da nessuno.
- Quando questo diventa un problema:
    - Accoppiamento più forte tra ConcreteStrategy e Context.
    - Il primo accede al secondo per chiedere i dati di cui ha bisogno.