Per analizzare i risultati si separano i dati in base all'ambiente in cui sono stati eseguiti e si standardizzano nella forma.
Per ogni tipo di parametro di input si individuano i valori da testare e per l'insieme dei parametri si usano tecniche che vanno sotto il nome di [[Testing Combinatorio]] per ridurre le combinazioni.

I casi di test sono selezionati in base alla distribuzione di probabilità dei dati di ingresso del programma.
Il test è quindi progettato per esercitare il programma sui valori di ingresso più probabili per il suo utilizzo a regime.
Il vantaggio è che, nota la distribuzione di probabilità, la generazione dei dati di test è facilmente automatizzabile.

I dati del dominio di ingresso vengono ripartiti in classi di equivalenza.
Due valori d'ingresso appartengono alla stessa classi di equivalenza se, in base ai requisiti, dovrebbero produrre lo stesso comportamento del programma.

I valori limite o di frontiera sono i valori estremi delle classi di equivalenza definite in base al comportamento del programma.
Per generare in modo automatico un insieme grande a piacere i valori si usa un metodo random.
Nel tempo, un organizzazione, può essersi costruita un'esperienza nel definire casi di test che se collezionata su un catalogo può rendere il processo più veloce e automatizzare alcune decisioni. I cataloghi catturano l'esperienza di coloro che definiscono i test elencando tutti i casi che devono essere considerati per ciascun possibile tipo di variabile.