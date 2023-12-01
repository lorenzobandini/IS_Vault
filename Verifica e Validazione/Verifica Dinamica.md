Anche chiamata testing, si compone in più fasi:
1. [[Progettazione casi di test]]
2. [[Esecuzione del codice]]
3. Analisi dei risultati
4. Debugging

Il test viene effettuato a più livelli:
- Test di unità
- Test di integrazione
- Test sul sistema
- Test di accettazione o di collaudo

Le prove devono essere ripetute in una sessione di test con condizioni immutate cioè in un ambiente definito con casi di prova definiti e procedure definite.

I vari test di sistema sono:
- **Facility test (test delle funzionalità):** Il Facility test mira a controllare che ogni funzionalità del prodotto, stabilita nei requisiti, sia stata implementata correttamente. Si concentra sulla verifica delle singole funzioni del software per garantirne il corretto funzionamento.
- **Security test:** Questo test verifica l'efficacia dei meccanismi di sicurezza del sistema cercando di accedere a dati o funzionalità che dovrebbero essere riservate. Si focalizza sulla protezione del sistema da accessi non autorizzati e valuta la robustezza delle misure di sicurezza implementate.
- **Usability test:** Questo test valuta la facilità d'uso del prodotto da parte dell'utente finale. È un'analisi soggettiva che tiene conto di vari fattori, tra cui la documentazione, il livello di competenza dell'utenza, e le caratteristiche operative dell'ambiente d'uso del prodotto.
- **Performance test:** Il Performance test valuta l'efficienza del sistema rispetto ai tempi di elaborazione e di risposta. Viene eseguito a diversi livelli di carico per valutare le prestazioni del sistema in condizioni normali e di stress, particolarmente critico per i sistemi in tempo reale.
- **Volume test (o load test, test di carico):** Questo test sottopone il sistema al carico massimo previsto dai requisiti, verificando il comportamento delle funzionalità in condizioni di massimo carico. Identifica malfunzionamenti e assicura l'efficienza del sistema anche in situazioni di utilizzo intensivo.
- **Stress test:** Lo Stress test sottopone il sistema a carichi di lavoro superiori a quelli previsti, mettendolo in condizioni operative eccezionali. Serve a testare la capacità di "recovery" del sistema dopo un fallimento, superando esplicitamente i limiti operativi previsti dai requisiti.
- **Storage use test:** Questo test valuta l'efficienza di un sistema in termini di utilizzo delle risorse, in particolare della memoria, durante il funzionamento. Ha implicazioni sull'ambiente operativo richiesto per installare il sistema.
- **Configuration test:** Il Configuration test ha l'obiettivo di testare il sistema in tutte le configurazioni previste, comprese piattaforme di installazione diverse per sistema operativo o dispositivi hardware. Esamina anche insiemi di requisiti funzionali leggermente diversi.
- **Compatibility test:** Il Compatibility test valuta la compatibilità del sistema con altri prodotti software, inclusi versioni precedenti dello stesso prodotto, sistemi diversi ma funzionalmente equivalenti, e altri sistemi software con cui il prodotto deve interagire.
