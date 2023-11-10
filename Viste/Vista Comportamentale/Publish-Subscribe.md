I [[Componenti Software]] interagiscono annunciando eventi e un componente si abbona a classi di eventi rilevanti per il suo scopo. Ciascun componenti, volendo, può essere sia produttore che consumatore di eventi.

Disaccoppia produttori e consumatori di eventi e favorisce le modifiche dinamiche del sistema.

Vengono usati due diversi connettori:
- Uno per le richieste di pubblicazione
- Uno per diffondere i dati

![[Pasted image 20231108164327.png]]

In questo stile, mittenti e destinatari di messaggi dialogano attraverso un tramite che viene detto dispatcher o broker.
Il mittente di un messaggio, detto publisher, non deve essere consapevole dell'identità dei destinatari, detti subscriber; esso si limita a pubblicare il proprio messaggio al dispatcher.
I destinatari, cioè i subscribers, si rivolgono a loro volta al dispatcher abbonandosi alla ricezione di determinati tipi di messaggi.
Il dispatcher inoltra ogni messaggio ricevuto da un publisher a tutti i subscriber interessati a messaggi di quel tipo.

![[Immagine 2023-11-08 164731.png]]

La diffusione può avvenire sia con:
- Modello Push:
	- il broker invia attivamente i messaggi ai consumatori
	- è complicato per il broker trattare con diversi tipi di consumatori in quanto controlla la frequenza con cui i dati vengono trasferiti
	- deve decidere se inviare un messaggio immediatamente o se accumulare più dati e inviare
- Modello Pull:
	- il consumatore si assume la responsabilità di recuperare i messaggi dal broker
	- il consumatore deve mantenere un valore che identifica il prossimo messaggio successivo da trasmettere ed elaborare