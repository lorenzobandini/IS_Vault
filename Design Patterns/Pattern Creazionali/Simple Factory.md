Detto anche Concrete Factory, non è un pattern GoF, ma una semplificazione molto diffusa di Abstract Factory.

Quando la logica di creazione è complessa e si vuole separare la logica di creazione dalle altre funzionalità di un oggetto si delega a un oggetto chiamato Factory che gestisce la creazione.

Questa factory class fornisce un metodo per creare istanze di diversi tipi di oggetti basati su uno specifico input o parametro. È un modo per astrarre la logica di creazione degli oggetti, offrendo un'interfaccia comune per la creazione di oggetti diversi senza esporre la complessità della loro inizializzazione.

![[Pasted image 20231113161941.png]]

