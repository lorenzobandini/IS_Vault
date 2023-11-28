Una macchina a stati è un grafo stati transizioni che descrive il comportamento delle istanze di una [[Classi|classe]], in generale di un classificatore
Occorre individuare gli strati significativi in cui si può trovare un oggetto durante la sua vita.
Inoltre dobbiamo descrivere come da ciascuno di questi stati l'oggetto può passare (transitare) in un altro.
Le [[Transizioni]] avvengono in risposta al verificarsi di un [[Evento]].

La sintassi è:

![[Pasted image 20231009092715.png]]

Tipi di azioni possibili:
- Azione di entrata: eseguita all'ingresso di uno stato
- Azione di uscita: eseguita all'uscita di uno stato
- Transizione interna: risposta ad un evento
- Attività interna: eseguita in modo continuato mentre l'oggetto si trova in quello stato senza la necessità di un evento scatenante. A differenza delle altre azioni, consuma tempo e può essere interrotta con un evento.

![[Pasted image 20231009094320.png]]

Gli stati composti possono essere:
- Sequenziali: un solo sottostato attivo in ogni istante![[Pasted image 20231009102257.png]]
- Parallelo: sottostanti attivi contemporaneamente, uno per regione ![[Immagine 2023-10-09 102401.png]]

Quando si vuole descrivere uno stato composito in un diagramma a parte per definirlo e riusarlo in più contesti, si usano delle sottomacchine che hanno il loro tipo.
Le sue istanze si indicano con `nomeIstanza: Tipo`

![[Pasted image 20231016113738.png]]

Una sottomacchina può definire entry and exit points che servono per collegare le transizioni della macchina principale.
Le [[Transizioni]] di completamento sono senza evento, ma scattano al raggiungimento:
- Della terminazione di un'attività composta
	- Dello stato finale in uno stato composito sequenziale
	- Degli stati finali di tutte le regioni ortogonali di uno stato composito parallelo
	- Di un exit point
- Alla terminazione di entry e/o di do activity
- Di uno pseudo-stato giunzione

Altri tipi di stato sono
- [[Giunzione]]
- [[Decisione]]
- [[Storia]]

La differenza tra giunzione e decisione sono che:
- Giunzione: è statica e le guardie sono calcolate prima di uscire dall'ultimo stato prima della giunzione
- Decisione: è dinamica e le guardie sono valutate nel momento in cui si entra nello stato di decisione