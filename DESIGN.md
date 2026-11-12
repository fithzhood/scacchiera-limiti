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

Esercizio risolto (o soluzione mostrata): compaiono in rosso gli asintoti tratteggiati non ancora tracciati, poi il grafico di una
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
Livelli 7-8, asintoti: i segni sono gli stessi dei livelli precedenti (tratteggi nelle metà delle caselle
del bordo), ma le metà non sono separate da una linea. Al suo posto, se aiuta, si traccia l'asintoto: gli
strumenti "Asintoto verticale" e "Asintoto orizzontale" (in fondo alla fila, in rosso) mettono una retta
rossa tratteggiata su tutto il piano toccando un punto qualsiasi della colonna x = a o della riga y = b;
ritoccando si toglie. È un aiuto al disegno: il controllo non lo guarda (né giusto né segno in più) e
resta anche quando si mostra la soluzione.
Ogni esercizio usa la meccanica che il suo livello introduce: 2 un salto (limite e valore diversi
nella stessa colonna), 3 un asintoto orizzontale, 4 un asintoto verticale, 5 una coppia di limiti
laterali e un limite infinito all'infinito, 6-8 almeno un asintoto verticale e una condizione a x→±∞.
Aiuto del livello: piccola finestra con le condizioni d'esempio, una scacchiera in miniatura animata
(una freccia legge la condizione, si accendono colonna e riga, sceglie lo strumento, piazza il segno, poi arriva il
grafico; in ciclo) e una frase. Mostra solo la novità del livello (6: un valore letto senza colori;
7: i tratteggi nelle metà, ciascuno preceduto dalla sua retta rossa facoltativa; l'8 non ha segni nuovi e ripete la scena del 7).
Nel Percorso si apre da sola quando si arriva a un livello non ancora visto dall'ultimo azzeramento (anche
dopo il trofeo); in Allenamento mai da sola, e aprirla lì non conta come vista. Il tasto "?" la richiama in
entrambe le modalità. Senza movimento: scena finita, ferma.
Trofeo: superato anche l'ultimo livello (3 esercizi risolti nel Percorso) si conquista una coppa
d'oro con ∞ inciso. Compare in una finestra dopo il grafico dell'esercizio che lo fa vincere, con
la data; poi resta in bacheca come tasto "Trofeo ×N" (N = percorsi completati) sulla pagina di partenza.
Vinto il trofeo il percorso si azzera da solo e, chiusa la finestra, si riparte dal livello 1.
"Ricomincia il percorso" (pagina di partenza, se c'è qualcosa da azzerare) chiede conferma, riporta al
livello 1, azzera gli esercizi risolti e le spiegazioni viste; i trofei restano.
Livelli 1-5: valori di x in blu, valori di y in rosso, su etichette e condizioni.
L'avanzamento resta nel browser (localStorage).
Versione ("v1.NN", piccola e grigia) in ogni schermata: sotto la pagina iniziale, nell'angolo in basso a destra
della scacchiera, in alto a destra nella finestra d'aiuto. Si alza a ogni pubblicazione.
Tutto in uno schermo, senza scorrere, anche nell'iframe di Compasso (telefono: 360×535). La scacchiera è
quadrata e prende lo spazio che resta: in verticale sopra il pannello, in orizzontale a sinistra (il pannello
a destra è largo quanto avanza, da 270 a 420 px). Pannello compatto: riga dei livelli con "?" (aiuto) e
casetta (pagina iniziale), nome del livello e avanzamento su una riga, condizioni su due colonne, strumenti,
tasti Controlla / Soluzione / Nuovo / Prossimo, messaggio breve. Sotto i 600 px d'altezza tutto più fitto.
Numeri della scacchiera e degli assi in grassetto, proporzionati al lato.
Pedice dei limiti (x → a) grande (0,8 della formula) e seminero; il segno del lato (− sinistra, + destra)
in grassetto, grande quanto il pedice.
Lente: toccando una condizione del pannello compare grande al centro dello schermo (fino a 80 px, ridotta
se non ci sta), crescendo dal punto in cui stava; il bordo è verde o rosso se è già stata controllata.
Un altro tocco, dovunque, la chiude senza piazzare segni.
Tablet e schermi grandi (almeno 700×700): pannello, finestre e pagina iniziale ingranditi del 30% (zoom);
in orizzontale il pannello è più largo (420-520 px).
Finestra d'aiuto grande quanto lo schermo (12 px di margine, al massimo 640 px di larghezza in verticale):
la scacchiera animata si prende lo spazio che resta; in orizzontale sta a sinistra, alta quanto la finestra.
Nell'aiuto le condizioni sono grandi (23 px, 20 px sul telefono) e i valori di x e y in grassetto, perché
si legga quale colonna e quale riga cerca la freccia.
È anche un laboratorio di Compasso (iframe, argomento Continuità e asintoti).
Pagina di partenza a ogni apertura: piccola scacchiera disegnata, titolo, e due scelte, Percorso (con
"Si comincia dal livello 1" / "Riprendi dal livello n" / "Completato") e Allenamento; sotto, il tasto Trofeo
se conquistato, e "Ricomincia il percorso". Il tutorial parte solo dopo la scelta del Percorso. Nel gioco la
casetta ci riporta: è da lì che si cambia modalità.
Due modalità: Percorso (livelli in ordine, si sbloccano) e Allenamento (qualunque livello, conta
solo gli esercizi della visita e non tocca il percorso). La modalità scelta si ricorda.

## Colori
- Carta #DCE3E8 / Ardesia #8FA3B3 — caselle
- Carta e ardesia schiarite — righe e colonne ±∞
- Inchiostro #1F2A33 — testo, assi, segni
- Evidenziatore #E0A526 — strumento scelto, focus
- Giusto #2F7D4F, Sbagliato #C2412D, Soluzione #B8660B — solo dopo il controllo
- Asse x #1F5FBF (blu), Asse y #C62D2D (rosso) — indizio nei livelli 1-5
- Asintoti #C62D2D (rosso) — rette tratteggiate, piazzate a mano nei livelli 7-8 o mostrate col grafico
  (quelle già piazzate non si ripetono)
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
