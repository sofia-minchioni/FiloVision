# FiloVision
-[## Introduzione
Filovision è un analizzatore di testi e concetti filosofici che coinvolge le discipline
umanistiche di filosofia, italiano, storia all'interno dell'informatica. L'informatica è la disciplina che 
studia l'elaborazione, la rappresentazione, la gestione delle informazioni. La filosofia è la 
disciplina che studia e analizza il pensiero, la coscienza, l'etica. Unendo le due discipline 
rendiamo la loro comprensione più chiara e immediata. L'obbiettivo è quello di realizzare un
programma capace di leggere e analizzare testi filosofici per individuare le parole più
ricorrenti e individuare le parole chiave e i concetti principali.](#introduzione)
-[## Tecniche adottate
Il programma ha il compito di leggere un testo; creare un dizionario delle frequenze delle 
parole; estrarre le cinque parole più frequenti; permettere di classificare manualmente i termini
in categorie concettuali. Il programma applica **import string** per accedere alla punteggiatura
da eliminare; **from collections import Counter** per contare quante volte un elemento compare 
nella lista parole; ]**stopwords=["il", "la", "lo", "i", "gli", "le", "un", "uno", "di", "a",
"da", "in", "con", "su", "per", "tra", "fra", "e", "o", "ma", "che", "non", "più", "come",
"anche", "se"]** per creare la lista delle parole inutili; **with open("testo_meraviglia.txt", "
I", encoding="utf-8")as file:** per leggere e codificare i caratteri speciali;
**testo=file.read()** per leggere il file e metterlo nella variabile testo;
**testo_pulito=testo.lower()** per rendere tutte le maiuscole in minuscole; **for carattere in
string-punctuation:** e **testo_pulito=testo.replace(carattere,")** per rimuovere ogni segno di
punteggiatura; **parole=[parola for parola in testo_pulito.split() if parola not in stopwords]**
per dividere il testo in singole parole e creare una lista con solo le parole significative;
**conteggio=Counter(parole)** per contare quante volte ogni elemento compare nella lista parole;
**top_5=conteggio.most_common(5)** per estrarre le tuple che contengono la parola e il numero di
volte che compare; **print("Le 5 parole più frequenti:")** per stampare le tuple; **for parola,
frequenza in top_5:** per scorrere le 5 parole più frequenti; **print(f"-{parola}:
{frequenza}")** per creare una stringa, nella quale i valori delle variabili parola e frequenza 
vengono inseriti direttamente dentro il testo; **concetti={"filosofia": "conoscenza",
"meraviglia": "origine"; "sapere": "epistemologia", "desiderio": "motivazione", "conoscenza": "
fine in se"}** per creare un dizionario che collega le parole ai concetti;
**print("\nAssociazioni concettuali:")** per creare una nuova riga prima del testo; for parola,
**concetto in concetti.items():** per scorrere tutte le coppie del dizionario concetti;
**print (f"-{parola}->{concetto}")** per creare una stringa, nella quale i valori delle variabili 
parola e concetto vengono inseriti dentro il testo.] (#tecniche)
-[## Strategie dei test
Per verificare se il codice funziona abbiamo preso il codice a pezzi, e mano a mano ne abbiamo
aggiunto una parte. Durante i test abbiamo controllato che il programma leggesse correttamente il 
file di testo, eliminasse le parole inutili, contasse le parole più frequenti, mostrasse le
associazioni concettuali. In conclusione il file funziona correttamente e ha mostrato i risultati adatti.] (#srategie)
 
