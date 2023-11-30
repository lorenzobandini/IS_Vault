Definisce la struttura del codice identificandone le parti e come sono collegate tra loro ed è ottenuta a partire dal codice.
I diagrammi a blocchi sono un linguaggio di modellazione grafico per rappresentare algoritmi.

![[Pasted image 20231130182012.png]]

Ci cercano i valori delle nostre variabili in modo da esercitare tutti i comandi.
La misura della copertura è data da $$\text {Misura di Copertura}=\frac{\text{Numero di Comandi Esercitati}}{\text{Numero di Comandi Totali}}$$
La copertura non è monotona rispetto alla dimensione dell'insieme di test e solitamente cerchiamo di minimizzare il numero di test a parità di copertura.

Un insieme di test $T$ per un programma $P$ copre tutte le condizioni semplici di $P$ se, per ogni condizione semplice $CS$ in $P$, $T$ contiene un test in cui $CS$ vale `true` e un test in cui $CS$ vale `false`.
La copertura delle condizioni semplici $CS$ viene calcolata con:$$\text{Copertura delle Condizioni Semplici}=\frac{\text{n° di valori di verità assunti nelle Condizioni Semplici}}{2\cdot \text{n° di Condizioni Semplici}}$$
La copertura dei cammini richiede di percorrere tutti i cammini, numero che cresce in modo esponenziale con le decisioni e può essere potenzialmente infinito con cammini ciclici.
Per limitare il numero di cammini da attraversare si richiedano casi di test che esercitino il ciclo 0 volte, esattamente una volta o più di una volta.