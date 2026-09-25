# Franceschetta58 V10.2 — attivazione

1. Pubblica `index.html`, `manifest.webmanifest`, `service-worker.js` e cartella `icons/` nella radice del sito GitHub Pages (non il solo ZIP). Per GitHub Pages sotto /Franceschetta58/ abilita Settings > Pages > Deploy from a branch > main > /(root), oppure adatta il workflow esistente.
2. In Firebase Authentication > Settings > Authorized domains aggiungi `tommy0794.github.io` se assente.
3. In Firestore > Regole incolla `firestore.rules` e pubblica. Non utilizzare `allow read, write: if true`.
4. L'account Tommy già creato deve avere un documento `/users/019urR09uEeqxXdmrzcW4rKapIk1` con `name: "Tommy"`, `role: "admin"`, `disabled: false`.
5. Crea gli altri utenti in Authentication > Users > Add user con email individuali e password temporanee, poi crea `/users/<UID>` con `name` e `role`: Vins admin; Carlo, Rocco, T, Antonio user; Stagista intern. Comunica le password in privato, non inserirle nel repository.
6. Verifica con due dispositivi: un admin crea una preparazione, un utente la vede, uno stagista può solo confermarla. Verifica che un utente non possa modificare `/users`.
7. Il sito richiede HTTPS e connessione a Internet. Non sono stati migrati automaticamente eventuali dati demo locali. Prima di sostituire una versione usata, esporta o conserva i dati esistenti.

ATTENZIONE: la chiave Firebase web è un identificatore client, non una credenziale amministrativa; la protezione effettiva è affidata a Authentication e alle regole Firestore. L'APK richiede compilazione separata con il progetto Android originale e la firma appropriata. iPhone usa l'installazione PWA tramite Safari.
