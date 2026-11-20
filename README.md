# GommeTracker — PWA 1.0

App installabile per iPhone, completamente in italiano. Gestisce più auto, treni pneumatici e chilometri percorsi in ogni intervallo di montaggio. Funziona offline dopo la prima visita, con dati in localStorage ed esportazione/importazione JSON.

## Pubblicazione gratuita con GitHub Pages

1. Su github.com crea un repository chiamato `GommeTracker` (pubblico).
2. Carica **tutti i file e la cartella `icons`** contenuti in questo ZIP nella radice del repository (non caricare soltanto lo ZIP).
3. Apri **Settings → Pages**; in **Build and deployment**, scegli **Deploy from a branch**, ramo **main**, cartella **/(root)** e premi **Save**.
4. Attendi il link pubblicato, solitamente `https://TUO-UTENTE.github.io/GommeTracker/`.
5. Aprilo su iPhone con Safari, tocca **Condividi → Aggiungi alla schermata Home → Aggiungi**.

## Uso

1. Aggiungi un'auto.
2. Aggiungi almeno un treno di pneumatici.
3. Premi **Primo montaggio** e inserisci il chilometraggio iniziale.
4. Aggiungi un altro treno, poi a ogni cambio premi **Cambio gomme** e registra il contachilometri. L'app attribuisce i km trascorsi al treno smontato.
5. Per i treni ancora montati il totale mostra solo i chilometri **completati**: la percorrenza attuale sarà conteggiata al prossimo cambio.
6. Esegui periodicamente **Dati → Esporta dati** e salva il JSON su iCloud Drive.

## Limiti v1

- I dati sono salvati solo sul dispositivo/browser, non sincronizzati tra dispositivi.
- Non è possibile modificare singoli eventi storici: se registri un cambio errato, ripristina un backup precedente (oppure correggi i dati in una versione futura).
- Il contachilometri deve aumentare tra i cambi; non sono gestiti reset o sostituzioni del quadro strumenti.
- La prima visita richiede Internet e HTTPS (GitHub Pages lo fornisce).
- L'app non è nativa SwiftUI e non viene pubblicata su App Store.


## Versione 1.1 — correzione delle registrazioni
Nello Storico o negli Ultimi cambi di un'auto, premi **Correggi data / km** sulla registrazione. Un cambio comprende smontaggio e montaggio: correggerne uno aggiorna entrambi. Il sistema controlla i cambi precedenti e successivi e ricalcola le distanze dei treni. I dati esistenti rimangono in localStorage con la stessa chiave `gommetracker.v1`. Prima di aggiornare, esporta un backup JSON dalla sezione Dati.
