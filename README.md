

<img width="1559" height="363" alt="Schermata del 2026-02-28 12-26-50" src="https://github.com/user-attachments/assets/b99d1c5c-f419-4bbe-a0f5-8aee03338c24" />

🇮🇹 Italiano: Descrizione del Progetto Cos'è questo script?

Questo tool è un JavaScript Bookmarklet progettato per i router 5G/4G Huawei (serie CPE Win, H352, B818, ecc.). Permette di visualizzare statistiche di segnale dettagliate e di forzare bande di frequenza specifiche che sono normalmente nascoste nell'interfaccia utente standard (WebUI). Come funziona "sotto il cofano"?

Intercettazione API: Il router comunica con il browser tramite richieste 
HTTP POST/GET verso endpoint specifici (es. /api/net/net-mode o /api/device/signal).
Lo script invia richieste dirette a questi endpoint bypassando i limiti grafici 
della WebUI.

Maschere di Bit (Bitmasking): Per selezionare le bande, Huawei utilizza
un sistema esadecimale.  Lo script converte le tue selezioni (es. B1, B3, n78)
in una stringa esadecimale complessa (Bitmask) che il modem può interpretare.

Sicurezza (CSRF Token): Per ogni comando inviato, lo script estrae
automaticamente il token di sicurezza (__RequestVerificationToken) dalla pagina corrente,
garantendo che il router accetti il comando di modifica.

Parsing XML: I dati del segnale (RSRP, SINR, PCI) vengono estratti analizzando
le risposte XML del router in tempo reale ogni 2 secondi.

🇺🇸 English: Project Description What is this script?

This tool is a JavaScript Bookmarklet tailored for Huawei 5G/4G routers (CPE Win series, H352, B818, etc.). It enables the visualization of detailed signal statistics and allows users to force specific frequency bands that are typically hidden in the standard WebUI. How it works "under the hood"

API Interception: The router communicates with the browser via HTTP POST/GET requests to specific endpoints
(e.g., /api/net/net-mode or /api/device/signal). This script sends direct requests to these endpoints,
bypassing the graphical limitations of the standard interface.

Bitmasking: To select bands, Huawei uses a hexadecimal system. The script converts your human-readable
selections (e.g., B1, B3, n78) into a complex hexadecimal string (Bitmask) that the modem's firmware
understands.

Security (CSRF Token): For every command sent, the script automatically extracts the security token
(__RequestVerificationToken) from the current page source, ensuring the router validates the modification
command.

XML Parsing: Signal data (RSRP, SINR, PCI) is extracted by parsing the router's XML responses in real-time
every 2 seconds.

🇮🇹 Come usare lo script (Bookmarklet)

Copia il codice: Copia tutto il codice JavaScript fornito (quello che inizia con javascript:).

Crea un preferito: Nel tuo browser (Chrome, Firefox, Edge), crea un nuovo preferito (segnalibro).

Modifica l'URL: Inserisci un nome a tua scelta (es. "Huawei Hack") e nel campo URL/Indirizzo
incolla il codice copiato.

Esecuzione: Accedi alla pagina di gestione del tuo router (es. 192.168.8.1 o 192.168.1.1), 
effettua il login e poi clicca sul preferito appena creato. Il menu apparirà istantaneamente in alto.

🇺🇸 How to use the script (Bookmarklet)

Copy the code: Copy the entire JavaScript code provided (the one starting with javascript:).

Create a bookmark: In your browser (Chrome, Firefox, Edge), create a new bookmark.

Edit the URL: Give it a name (e.g., "Huawei Hack") and in the URL/Address field, paste the copied code.

Execution: Log in to your router's web interface (e.g., 192.168.8.1 or 192.168.1.1) and then click on 
the bookmark you just created. The hack menu will instantly appear at the top of the page.
