Il sistema è formato da due componenti: il client e il server che spesso vengono eseguiti su macchine diverse collegate in rete.

![[Pasted image 20231108155353.png]]

Il server svolge le operazioni necessarie per realizzare un servizio e aspetta le richieste dai vari client ad un porto. I client invece inviano al server le richieste ed attende una risposta.

Per realizzare un'architettura client-server il lato server utilizza uno o più thread in ascolto delle richieste, più un gestore delle richieste. Quando riceve una richiesta, la elabora e invia una risposta al client. I server possono essere ulteriormente classificati come stateless oppure stateful.
I client di un server stateful possono fare richieste composite che consistono in più richieste atomiche. Ciò consente un'interazione più colloquiale o transazionale tra client e server. A tal fine, un server stateful conserva un record delle richieste di ciascun client corrente. Questo record è chiamato sessione.
