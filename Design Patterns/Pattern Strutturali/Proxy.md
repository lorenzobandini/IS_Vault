Lo scopo principale del pattern Proxy è fornire un sostituto o un rappresentante di un altro oggetto per controllarne l'accesso. Ciò può essere fatto per vari motivi, come il controllo dell'accesso, la gestione della creazione o l'inserimento di logica aggiuntiva prima o dopo l'accesso all'oggetto principale. Simile ad [[Adapter]] in quanto si introduce da intermediario ma sono diversi perché:
- Proxy e oggetto originale hanno la stessa interfaccia mentre Adapter e Adaptee no
- Il Proxy può eseguire pre- e post- elaborazioni

Il modello statico è:

![[Pasted image 20231120111330.png]]

Mentre il modello dinamico è:

![[Pasted image 20231120111347.png]]

I diversi usi e tipi di Proxy sono:
- Remote Proxy: il Proxy permette l'accesso a un oggetto remoto
- Protection Proxy: il Proxy implementa un controllo sugli accessi
- Cache Proxy: il Proxy mantiene coppie richiesta-risposta sgravando il server
- Synchronization Proxy: gestisce gli accessi concorrenti ad un servizio
- Virtual Proxy: il Proxy si comporta come l'originale mentre l'originale viene costruito, poi passa le richieste a quest'ultimo
