Un test-case è una tripla \<input, output atteso, ambiente\>.
Il test obligation è una descrizione di casi di test che richiede di testare proprietà ritenute importanti.

Non possiamo dire che se il sistema supera un'adeguato insieme di test allora deve essere corretto perché la correttezza è indecidibile.
Un criterio di adeguatezza è un insieme di test obligation per verificare l'adeguatezza di un insieme di casi di test. Il fatto che il nostro insieme di test non verifichi un criterio ci suggerisce come modificarlo.
Un insieme di test soddisfa un criterio di adeguatezza se:
- Tutti i test hanno successo
- Ogni test obligation è soddisfatta da almeno un caso di test

Possiamo definire le test obligation:
- Dalle funzionalità (a scatola chiusa, [[Criteri Black Box]]) guardando la specifica del software
- Dalla struttura (a scatola aperta, [[Criteri White Box]]) guardando il codice
- Dal modello del programma
- Da [[Test su Fault Ipotetici]]
