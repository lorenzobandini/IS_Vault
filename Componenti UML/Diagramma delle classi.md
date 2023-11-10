Una [[Classi|Classe]] cattura un concetto nel [[Dominio]] del problema o della realizzazione.
Il diagramma delle classi descrive:
- Il tipo degli oggetti che fanno parte di un sistema software o del suo dominio
- Le relazioni statiche tra essi (gli elementi e le relazioni tra essi non cambiano nel tempo)

Sintassi:
![[Pasted image 20231004173015.png]]

I diagrammi delle classi mostrano anche le proprietà e le operazioni di una classe e può essere usato:
- per descrivere il dominio
- per la progettazione di dettaglio

Quando si usa il diagramma delle classi **per descrivere il dominio**:
- le operazioni, in particolare i setters e i getter, normalmente si omettono
- gli attributi utili per caratterizzare l'elemento del dominio si specificano, i dettagli implementativi no, soprattutto l'ID
- Le [[Visibilità]] si omettono

Scegliamo se un concetto va modellato con un attributo (specifichiamo solo il nome) o come una classe (può avere attributi e operazioni proprie) in base alle nostre esigenze.
Gli attributi e operazioni statici, cioè che non richiedono un'istanza per essere modellati, sono sottolineati.
Le classi possono rappresentare anche [[Enumerazioni]]

Strutture di classi utili sono:
- [[Classe Astratte]]
- [[Classe Interfaccia]]
- [[Classe Associazione]]

Per rappresentare e modellare le entità e i concetti rilevanti all'interno del dominio del problema o dell'ambito specifico che un sistema software deve affrontare usiamo le [[Classi di analisi del dominio]].

La differenza tra le Classi UML e le Entità in Basi di Dati sono che in BD le entità sono intese come collezioni sottointendendo che ci sono più istanze e operazioni per visitare tutte le istanze
