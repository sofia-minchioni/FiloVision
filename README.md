# FiloVision

## Indice 
-[Introduzione](#introduzione)
-[Tecniche adottate](#tecniche-adottate)
-[Strategie test](#strategie-test)

## Introduzione
FiloVision è un analizzatore di testi e concetti filosofici che coinvolge le discipline umanistiche di filosofia, italiano, storia all'interno dell'informatica. L'informatica è la disciplina che studia l'elaborazione, la rappresentazione, la gestione delle informazioni. La filosofia è la disciplina che studia e analizza il pensiero, la coscienza, l'etica. Unendo le due discipline rendiamo la loro comprensione più chiara e immediata. L'obbiettivo è quello di realizzare  un programma capace di leggere e analizzare testi filosofici o letterari per individuare le parole chiave e i concetti principali.

Abbiamo preso come riferimento il testo _Meraviglia_ di Aristotele, in cui afferma che la meraviglia è l'origine della filosofia. Gli uomini hanno iniziato a filosofare perchè provavano un senso di meraviglia di fronte a ciò che non conoscevano e sentivano il bisogno di comprenderlo. Per Aristotele, l'uomo ha una predisposizione naturale di stupirsi e questa lo spinge a cercare risposte. Chi non è capace di meravigliarsi non può essere un filosofo ma si deve considerare privo di sapienza e curioso di conoscere.

## Tecniche adottate 
Il programma ha il compito di leggere un testo; creare un dizionario delle frequenze delle parole; estrarre le cinque parole più frequenti; permettere di classificare manualmente i termini in categorie concettuali.

Il programma applica **import string** per accedere alla punteggiatura da eliminare; 
**from collections import Counter** per contare quante volte un elemento compare nella lista parole;
**stopwords=["il", "la", "lo", "i", "gli", "le", "un", "uno", "di", "a", "da", "in", "con","su", "per", "tra", "fra", "e", "o", "ma", "che", "non", "più", "come", "anche", "se"]** per creare la lista delle parole inutili; 
**with open ("testo meraviglia.txt", "r", encoding="utf-8")as file:** per leggere e codificare i caratteri speciali; 
**testo=file.read()** per leggere il file e metterlo nella variabile testo; 
**testo_pulito=testo. lower()** per rendere tutte le maiuscole in minuscole; 
**for carattere in string-punctuation:** e **testo_pulito=testo.replace(carattere,")** per rimuovere ogni segno di punteggiatura; 
**parole= [parola for parola in testo_pulito split() if parola not in stopwords]** per dividere il testo in singole parole e creare una lista con solo le parole significative;
﻿**conteggio=Counter(parole)** per contare quante volte ogni elemento compare nella lista parole;
﻿**top_5=conteggio.most_common(5)** per estrarre le tuple che contengono la parola e il numero di volte che compare; 
**print("Le 5 parole più frequenti:")** per stampare le tuple; 
**for parola, frequenza in top_5:** per scorrere le 5 parole più frequenti; 
**print(f"-{parola}:{frequenza}")** per creare una stringa, nella quale i valori delle variabili parola e frequenza vengono inseriti direttamente dentro il testo; 
**concetti={"filosofia": "conoscenza","meraviglia": "origine"; "sapere": "epistemologia", "desiderio": "motivazione", "conoscenza": "fine in se"}** per creare un dizionario che collega le parole ai concetti;
﻿**print("\nAssociazioni concettuali:")** per creare una nuova riga prima del testo; 
**for parola,﻿concetto in concetti.items ():** per scorrere tutte le coppie del dizionario concetti;
**print(f"-{parola}->{concetto}")** per creare una stringa, nella quale i valori delle variabili parola e concetto vengono inseriti dentro il testo. 

## Strategie test
Per testare il codice è necessario innanzitutto verificare che il file di testo si trovi effettivamente sul desktop del computer e che il percorso indicato nel codice corrisponda
esattamente al nome e alla posizione del file.

Per valutare il comportamento del programma, abbiamo creato un testo di prova contenente numerosi elementi utili per il testing: punteggiatura (come punti e virgole), articoli molto comuni (il, lo, la, ecc.) e parole scritte con lettere maiuscole e minuscole, per verificare correttamente la rimozione delle stopword, la pulizia del testo e la normalizzazione in minuscolo.

Il testo utilizzato per il test è il seguente: _La FILOSOFIA nasce, dalla meraviglia. Il desiderio di, sapere spinge l'uomo alla conoscenza.
La Meraviglia è l'origine della filosofia e la, conoscenza è il fine in sé._

il codice ha funzionato correttamente:

-le parole con punteggiatura sono state riconosciute e pulite;
-﻿﻿gli articoli e le stopword non sono stati conteggiati;
﻿﻿-parole scritte con maiuscole e minuscole sono state unificate;
-﻿﻿al termine sono state mostrate correttamente le associazioni concettuali e il calcolo delle parole più frequenti
[prima immagine](#Image.jpg)
[seconda immagine](#Image(1).jpg)


