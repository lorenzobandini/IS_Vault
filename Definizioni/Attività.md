Un'attività ha un nome ed è contenuta in un rettangolo con gli angoli smussati.
Il contenuto di un'attività è un grafo diretto in cui:
- I nodi rappresentano le componenti dell'attività come le azioni o i nodi di controllo
- Gli archi rappresentano il control flow cioè i possibili path eseguibili per l'attività

![[Pasted image 20231127153815.png]]

Le azioni sono rappresentate anche esse da rettangoli con angoli smussati.

![[Pasted image 20231127153853.png]]
 Il nome deve descrivere un'azione, quindi tipicamente essere un verbo. Inoltre le azioni sono atomiche e quindi non interrompibili.
 La freccia di uscita è presa appena è terminata l'azione e ci può essere solo una freccia entrante e solo una uscente per ogni azione.

Quando un'azione ha terminato il proprio lavoro, scatta una transizione automatica in uscita all'azione che porta all'azione successiva.
La semantica è descritta con il token game: l'azione può essere eseguita quando riceve il token.

I nodi di controllo sono:

![[Pasted image 20231127154148.png]]

Ogni volta che l'azione si attiva riceve un token si attiva e quando finisce passa il token all'arco uscente. Questo meccanismo viene alterato dalla "choise" (scelta).

![[Pasted image 20231127154344.png]]

Il token deve prendere sempre uno dei cammini e non può bloccarsi per cui una scelta deve coprire tutti i casi possibili. Ugualmente per il "merge" (fusione).

Invece la fork moltiplica il token cioè che per ogni token in ingresso ne produce uno per ogni freccia uscente e invece la join le consuma ma non è necessaria una join per ogni fork.
Se un token raggiunge un nodo di fine attività, l'intera attività è terminata.
Permettiamo più archi entranti su un nodo di fine attività.

![[Pasted image 20231127155630.png]]

Ma esistono anche i nodi di fine flusso per terminare l'execution path ma non tutta l'attività.
![[Pasted image 20231127155732.png]]

Esistono anche i Segnali e gli Eventi, dei nodi specializzati che gestiscono l'invio e la ricezione di segnali. L'invio di segnali è asincrono e non blocca l'attività.
Per accettazione di un evento esterno:

![[Pasted image 20231127155857.png]]

Per l'invio di un segnale:

![[Pasted image 20231127155915.png]]

O per l'accettazione di evento temporale:

![[Pasted image 20231127155938.png]]

Per accettare evento esterno e per accettare eventi temporali, non c'è bisogno di un arco entrante.
Se assente, quando si verifica l’evento, si genera un token mentre se presente, l’azione è abilitata quando arriva il token e si attende l’evento esterno per farlo transitare.

Si usa un'azione quando è effettuata dall'entità o dall'insieme di entità in cui si sta descrivendo il comportamento.
Usare l'accettazione di eventi esterni o invio segnali quando si comunica con una entità esterna.

Un diagramma può contenere un riferimento a un'attività secondaria.

Le partizioni permettono di assegnare la responsabilità alle azioni.
Una partizione spesso corrisponde alla divisione in unità operative in un modello di business.
