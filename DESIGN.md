# DESIGN.md — Scacchiera ∞

## Soggetto e persone
Gioco per imparare a leggere limiti e valori di una funzione. Studenti di quarta/quinta superiore,
su telefono o PC, in classe o a casa. Deve sembrare un foglio di lavoro, non un gadget.

## Regola del gioco
Scacchiera 9×9, coordinate −∞, −3 … +3, +∞ su entrambi gli assi (x verso destra, y verso l'alto).
Ogni condizione si traduce in un segno su una casella:
- f(a) = b → pallino pieno in (a, b)
- lim x→a f(x) = b → pallino vuoto in (a, b)
- lim x→a f(x) = ±∞ → tratteggio verticale in entrambe le metà della casella (a, ±∞)
- lim x→a⁻ / x→a⁺ f(x) = ±∞ → tratteggio verticale nella metà sinistra / destra di (a, ±∞).
  Le caselle a ±∞ con x finito sono divise da una linea sottile: è la retta x = a.
- lim x→±∞ f(x) = b → tratteggio orizzontale in entrambe le metà (sopra e sotto) della casella (±∞, b).
  Le caselle a x = ±∞ con y finito sono divise da una linea sottile: è la retta y = b.
  Il grafico si aggancia a una sola metà: quella di sopra se la funzione arriva o prosegue
  dall'alto (il primo punto a quota diversa è più in alto), altrimenti quella di sotto.
- lim x→+∞ f(x) = +∞ e lim x→−∞ f(x) = −∞ → tratteggio in salita nell'angolo
- lim x→+∞ f(x) = −∞ e lim x→−∞ f(x) = +∞ → tratteggio in discesa nell'angolo
Esercizio: 4-6 condizioni coerenti con una funzione. Al massimo un salto (limite ≠ valore)
o una coppia di limiti laterali per esercizio.

Esercizio risolto (o soluzione mostrata): compaiono gli asintoti tratteggiati, poi il grafico di una
funzione che rispetta le condizioni si disegna da sinistra a destra e ogni segno lampeggia quando
la traccia lo raggiunge. Il grafico resta nella parte finita e si aggancia all'estremo
interno di ogni tratteggio, con la sua direzione: il tratteggio resta visibile e continua la curva.
Assi sottili, così i tratteggi che cadono sugli assi si vedono. Senza condizioni a ±∞ il grafico si ferma al bordo della colonna ±∞.

## Livelli (3 esercizi risolti per passare al successivo, la soluzione mostrata non conta)
1 Valori · 2 Valori e limiti al finito · 3 Asintoti orizzontali · 4 Asintoti verticali ·
5 Limiti laterali e limiti infiniti all'infinito · 6 tutto, senza colori ·
7 senza scacchiera, solo assi · 8 tutto, solo assi.
Livelli 7-8: foglio uniforme, numeri e tacche sugli assi solo da −3 a +3 (sopra i segni, con alone);
±∞ fuori dal piano, oltre le estremità degli assi, perché indicano una direzione e non un punto; una linea
puntinata separa la fascia ±∞ dalla parte finita. Il tasto Prossimo livello compare a livello superato.
Ogni esercizio usa la meccanica che il suo livello introduce: 2 un salto (limite e valore diversi
nella stessa colonna), 3 un asintoto orizzontale, 4 un asintoto verticale, 5 una coppia di limiti
laterali e un limite infinito all'infinito, 6-8 almeno un asintoto verticale e una condizione a x→±∞.
Aiuto del livello: piccola finestra con le condizioni d'esempio, una scacchiera in miniatura animata
(una freccia legge la condizione, si accendono colonna e riga, sceglie lo strumento, piazza il segno, poi arriva il
grafico; in ciclo) e una frase. Si apre da sola nel Percorso la prima volta che si arriva a un livello; in
Allenamento mai da sola. Il tasto "? Aiuto" la richiama in entrambe le modalità. Senza movimento: scena finita, ferma.
I livelli spiegati si ricordano.
Trofeo: superato anche l'ultimo livello (3 esercizi risolti nel Percorso) si conquista una coppa
d'oro con ∞ inciso. Compare in una finestra dopo il grafico dell'esercizio che lo fa vincere, con
la data; poi resta come tasto "Trofeo" accanto alle modalità e la riapre.
Livelli 1-5: valori di x in blu, valori di y in rosso, su etichette e condizioni.
L'avanzamento resta nel browser (localStorage).
Orientamento: in verticale scacchiera sopra e pannello sotto; in orizzontale (telefono girato, tablet, PC)
scacchiera a sinistra alta quanto lo schermo, ferma mentre il pannello a destra scorre. Sugli schermi bassi
pannello e finestre più fitti (nella spiegazione figura, condizione e testo su una riga).
È anche un laboratorio di Compasso (iframe, argomento Continuità e asintoti).
Pagina di partenza a ogni apertura: piccola scacchiera disegnata, titolo, e due scelte, Percorso (con
"Si comincia dal livello 1" / "Riprendi dal livello n" / "Completato") e Allenamento; sotto, il tasto Trofeo
se conquistato. Il tutorial parte solo dopo la scelta del Percorso. Nel gioco "Pagina iniziale" ci riporta.
Due modalità: Percorso (livelli in ordine, si sbloccano) e Allenamento (qualunque livello, conta
solo gli esercizi della visita e non tocca il percorso). La modalità scelta si ricorda.

## Colori
- Carta #DCE3E8 / Ardesia #8FA3B3 — caselle
- Carta e ardesia schiarite — righe e colonne ±∞
- Inchiostro #1F2A33 — testo, assi, segni
- Evidenziatore #E0A526 — strumento scelto, focus
- Giusto #2F7D4F, Sbagliato #C2412D, Soluzione #B8660B — solo dopo il controllo
- Asse x #1F5FBF (blu), Asse y #C62D2D (rosso) — indizio nei livelli 1-5
- Funzione #0A6E6C — il grafico, con un alone chiaro per staccarsi dalle caselle

## Tipografia
Etichette e messaggi in monospace di sistema. Condizioni in font matematico di sistema
(Cambria Math): sono formule e devono somigliare a quelle del libro.

## Dettaglio caratterizzante
Assi cartesiani in inchiostro, frecce piccole verso +∞, che tagliano a metà la riga y = 0 e
la colonna x = 0. I segni stanno sopra gli assi.

## Glossario
"condizione", "segno", "casella", "esercizio". Segni: pallino pieno, pallino vuoto,
tratteggio verticale / orizzontale / in salita / in discesa.

## Tono
Inizio: "Piazza un segno per ogni condizione, poi premi Controlla."
Controllo: quante condizioni sono a posto, quanti segni in più. Successo: "Esercizio risolto".

## Default
Strumento iniziale: pallino pieno. Toccare una casella con lo stesso segno lo toglie.
