Si usano per descrivere le interazioni come scambi di messaggi e dati tra oggetti che vengono organizzati in sequenza temporale.
Nello specifico, in fase di analisi formalizzano la sequenza principale degli eventi con casi d'uso tra attori e sistema mentre in fase di progettazione i messaggi scambiati tra componenti illustrano come l'architettura realizza i requisiti.

Gli oggetti partecipanti alle interazioni all'interno di un diagramma di sequenza vengono rappresentati con linee di vita formate da:
- **Un rettangolo** che indica ruolo nell'interazione e/o tipo dell'oggetto
- **Una linea verticale** chiamata linea di vita dell'oggetto che è:
	- **tratteggiata** quando l'oggetto è inattivo
	- **continua e doppia** quando l'oggetto è attiva

![[Schermata 2023-11-11 alle 19.12.35.png]]

I messaggi rappresentano l'invocazione di operazione o segnali e possono essere:
- Sincroni (1)
- di Return (1.1)
- Asincroni (2)
- Asincroni con esplicito consumo di tempo (3)

![[Schermata 2023-11-11 alle 19.14.59.png]]

La sintassi del messaggio é: ![[Schermata 2023-11-11 alle 19.16.05.png]]

Alcuni partecipanti possono essere aggiunti dinamicamente all'interazione o cancellati.
![[Schermata 2023-11-11 alle 19.17.17.png]]

Esistono anche i "Self Messages" che non sono altre che chiamate di metodo.
![[Schermata 2023-11-11 alle 19.18.45.png]]

Frammenti composti compongono dei frame nei quali troviamo:
- Frame condizionali![[Schermata 2023-11-11 alle 19.23.53.png]]
- Frame iterativi![[Schermata 2023-11-11 alle 19.25.44.png]]
- Frame opzionale![[Schermata 2023-11-11 alle 19.26.18.png]]
- Frame parallelo![[Schermata 2023-11-11 alle 19.26.44.png]]

Possiamo includere un interazione definita altrove attraverso `ref` che include il diagramma di sequenza indicato.
Inoltre esistono i vincoli di durata che stabiliscono dopo quanto deve finire un azione.

Un gate (cancello) è un punto sul bordo del programma in cui è collegato un messaggio, in ingresso o in uscita. Il gate ha un nome e sono utili quando si riferiscono con `ref` altri diagrammi.

![[Schermata 2023-11-11 alle 19.32.19.png]]
