# Tecnoalarm TP/EV

Integrazione per Home Assistant delle centrali **Tecnoalarm serie TP/EV** via IP.

## Installazione
1. **Impostazioni → Add-on → Store → ⋮ → Repository** e incolla l'URL di questo repository.
2. Installa l'add-on **Tecnoalarm TP/EV**.
3. Assicurati di avere installato l'add-on **Mosquitto broker** (MQTT).
4. Apri la scheda **Configurazione** dell'add-on e compila:
   - `host` / `port` — IP e porta IP della centrale
   - `code` — codice utente
   - `passphrase` — (solo se la centrale la richiede)
   - `n_programs` / `n_zones` / `n_telecommands` — dimensioni impianto
5. **Avvia** l'add-on. Le entità compaiono da sole in Home Assistant (MQTT discovery).

## Cosa espone
- Stato impianto (allarme, rete/batteria, tamper, tensioni), segnale GSM
- Programmi (inserimento/disinserimento)
- Zone (aperta/chiusa, ed esclusione se abilitata)
- Pulsante PANICO — **solo se `enable_panic` è attivo** (attenzione: fa suonare le sirene)

## Manutenzione
Andrea

> Il motore è distribuito solo in forma compilata.
