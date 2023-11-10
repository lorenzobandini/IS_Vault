Stile in cui si isola la logica di business del controllo sull''input e dalla presentazione, consentendo sviluppo indipendente, test e manutenzione di ciascuno.

Formato da:
- Modello: fornisce il nucleo funzionale di un'applicazione, ed è rappresentazione del modello dei dati su cui opera l'applicazione. Quando un modello cambia il suo stato, notifica le sue viste associate in modo che si possano aggiornare.
- Vista: rende il modello in una forma adatta all'interazione, in genere un elemento dell'interfaccia utente. Ci possono essere più viste per un singolo modello per scopi diversi.
- Controllore: riceve l'input e effettua chiamate agli oggetti del modello. I controllori traducono gli eventi in richieste per eseguire operazioni sugli elementi del modello.

L'interazione con il Model-View-Controller consiste in:
1. L'utente interagisce con la vista 
2. Il controller riceve le azioni dell'utente e le interpreta
3. Il controller chiede al modello di cambiare il suo stato
4. Il modello notifica la vista quando il suo stato è cambiato
5. La vista chiede lo stato al modello